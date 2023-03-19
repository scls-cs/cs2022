---
jupytext:
	formats: md:myst
	text_representation:
		extension: .md
		format_name: myst
rise:
	start_slideshow_at: beginning

kernelspec:
	display_name: Python 3
	language: python
	name: python3
---

# 计算机网络大作业 #

在本次作业中，你将设计一个自动回复邮件程序，程序可以接收并回复邮箱中的未读邮件。你需要自己定义自动回复的模版，并支持对不同类型邮件进行特定回复。

此外，你还需要实现邮件过滤的功能，这样某些重要邮件则不会进行自动回复。



## 任务一：注册replit并加入班级群 ##

Replit跟OnlineGDB都是在线编程工具，但功能比OnlineGDB更强大。你可以根据这个链接来注册并加入班级群：

https://replit.com/teams/join/rxqkdwolonvsuvmtubogfyqlfjfxxmpq-SCLS-CS2022

## 任务二：理解并运行示例程序 ##

1. 获取最新的未读邮件

获取最新的未读邮件包括以下几个步骤：

* 通过imaplib库的IMAP4_SSL()建立与outlook邮箱的IMAP服务器的连接
* 使用login()登陆IMAP服务器
* select()函数选择要操作的文件夹，这里选择收件箱
* 使用 mail.search() 方法搜索收件箱中的未读邮件（标记为 'UNSEEN'）。该方法返回两个值，其中第一个值（用 _ 忽略）表示操作状态，第二个值（data）包含搜索结果。
* 用split()将搜索结果（data[0]）分割成一个包含未读邮件编号的列表。
* 如果没有未读邮件，则返回none，否则获取未读邮件编号列表中的最后一个元素，即最新的未读邮件编号。unread_msg_nums[-1]表示返回列表中最后一个元素。
* 使用 mail.fetch() 方法获取指定编号的邮件。参数 '(RFC822)' 表示我们需要获取邮件的完整原始数据。该方法同样返回两个值，第一个值（用 _ 忽略）表示操作状态，第二个值（msg_data）包含邮件数据。
* 使用message_from_bytes将邮件数据转换为一个Message 对象，以便我们能够更方便地访问邮件的各个部分（如发件人、主题等）。
* 登出IMAP服务器，并返回获取到的邮件

```{code-cell} python3
def get_newest_unread_email(your_email, your_password):
    # 使用 IMAP 协议连接到 Outlook 邮箱
    mail = imaplib.IMAP4_SSL('partner.outlook.cn')
    # 使用邮箱地址和密码登录
    mail.login(your_email, your_password)
    #选择收件箱
    mail.select('inbox')
    # 搜索未读邮件
    _, data = mail.search(None, 'UNSEEN')
    unread_msg_nums = data[0].split()

    # 如果没有未读邮件，返回 None
    if not unread_msg_nums:
        return None

		# 获取最新的未读邮件，unread_msg_nums[-1]表示获得未读邮件中的最后一封
    newest_msg_num = unread_msg_nums[-1]
    
    #用 fetch 方法从邮件服务器获取最新未读邮件的详细信息。(RFC822) 是一种邮件标准格式，表示我们想要获取整封邮件的原始信息。
    _, msg_data = mail.fetch(newest_msg_num, '(RFC822)')
        
    #将二进制数据转换为Message类型的对象，这样我们可以更方便地处理邮件的各个部分，如发件人地址、主题等。
    msg = email.message_from_bytes(msg_data[0][1])

    mail.logout()

    return msg
```

2. 回复邮件
回复邮件是SMTP协议来进行，主要包括以下几个步骤：
* 通过SMTP协议建立连接
* 通过ehlo()函数向SMTP服务器发送一个"hello"消息。这是SMTP协议的一个要求，用于初始化与服务器的会话。
* 通过starttls()函数启动TLS加密，这是加密电子邮件传输的一种方法。使用TLS加密可以确保您的邮件和凭据在传输过程中不被窃取或截获。
* 通过login()函数使用账号和密码登录SMTP服务器。
* 通过sendmail()函数发送邮件。它接受三个参数：发件人地址、收件人地址和邮件内容。我们使用格式化字符串（f-string）构建邮件内容，包括主题（subject）和回复内容（reply）。
* 通过quit()函数关闭与SMTP服务器的连接。

```{code-cell} python3
def send_reply(your_email, your_password, reply_to_email, subject, reply):
    smtp_server = smtplib.SMTP('smtp.partner.outlook.cn', 587)
    smtp_server.ehlo()
    smtp_server.starttls()
    smtp_server.login(your_email, your_password)
    smtp_server.sendmail(your_email, reply_to_email, f"Subject: {subject}\n\n{reply}")
    smtp_server.quit()
```

3. main函数

其中一个重要的步骤是定义你的模版reply_template，用三个双引号用来表示多行的字符串。

```{code-cell} python3
def main():
    your_email = input("Enter your email address: ")
    your_password = input("Enter your email password: ")

    # Fetch the newest unread email
    newest_unread_email = get_newest_unread_email(your_email, your_password)

    if newest_unread_email is None:
        print("No new unread emails.")
        return

    # Define reply template
    reply_template = """
    Hello,

    Thank you for your email. This is an automatic reply.

    Best regards,
    [Your Name]
    """

    # Send automatic reply to the newest unread email
    # 获得发件人的地址
    from_email = email.utils.parseaddr(newest_unread_email['From'])[1]
    subject = newest_unread_email['Subject']
    print(f"Sending reply to: {from_email}, Subject: {subject}")
    send_reply(your_email, your_password, from_email, subject, reply_template)

    print("Automatic reply has been sent to the newest unread email.")


if __name__ == "__main__":
    main()


这行程序表示只有当该文件直接被运行时，才会执行main()函数；当它被当作模块被其他文件调用时，main()函数不会被执行。我们直接照写即可。

```{code-cell} python3
if __name__ == "__main__":
	main()
```

4. 测试

测试之前，请先用自己的**学校邮箱**给自己**学校邮箱**发送一封邮件，并且不要打开它。让它处于未读状态。

在Replit中点击运行按钮，在右边分别输入你的邮箱和密码。运行完毕后，你会看到自己的邮箱中多了一封自动回复的邮件。这就说明你的程序运行成功了。

## 任务三 ##

1. 自动回复的邮件中，最后落款是[Your Name]，请修改成你的名字。

2. 将模版变得更有个性化，你可以加入你的风格。Be creative!

3. 创建邮件过滤器功能：使自动回复只对非自己的邮箱有效。也就是说，如果你给自己发送邮件，你不会收到自动回复；其他人给你发送的依然会收到自动回复。

4. 统计收到邮件的发件人: 在程序中添加一个功能，统计你收到最多邮件的前5个发件人，并显示他们的电子邮件地址和邮件数量。这样你就可以知道与谁的互动最为频繁。

## 附加任务 ##

关键词自动回复: 修改自动回复功能，使得程序根据邮件正文中的特定关键词来选择不同的回复模板。例如，如果邮件内容包含 "homework"，则使用相应的模版，例如"I will submit the homework on time"；如果邮件内容包含"Emergency"，则使用其它模版。

模版请自己设计。

为了完成这个任务，你需要读取邮件正文。

## 提交 ##

你提交的代码需要完成任务三的所有功能。提交之前请先自己运行。