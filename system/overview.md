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


# 计算机网络概论 #

* 互联网的所有设备都有一个IP地址。


* IP地址的格式：x.x.x.x，每个x都是一个8位二进制数。所以IP地址由32位二进制数组成。


* 域名是IP地址的别称，为了方便人类记忆。比如Google主页的IP地址之一172.217.25.14，域名是google.com。


* DNS服务器里存储域名和IP地址的对应关系。


* 可以通过nslookup命令来查找域名对应的IP地址。如果你用Mac，在Launchpad里面搜索"Terminal"。如果你用的是Windows，在开始菜单中搜索"cmd"进入终端。输入"nslookup google.com"，显示类似如下结果：（返回的IP地址可能不同，与电脑配置的DNS服务器有关）

```
  nslookup google.com
  
  Server:     10.10.0.215
  Address:    10.10.0.215#53

  Non-authoritative answer:
  Name:       google.com
  Address:    172.217.25.14
```

* 路由器的作用是对数据进行转发，类似物流公司根据目的地对包裹进行中转。

* 可以通过traceroute命令来观察数据的路径。如果你用Mac，在终端里面输入"traceroute google.com"; 如果你用Windows，在终端里面输入"tracert google.com"。

##  作业 ##

完成作业：

1. 请查找自己计算机的IP地址，在本题下方放上屏幕截图。

2. 打开终端（Windows是cmd），用nslookup命令查找下列域名对应的IP地址，并在下方放上屏幕截图。
    a. UCLA大学官网：www.ucla.edu
    
	  b. 任意至少两个其它网站

4. 请用traceroute(Mac)或者tracert(Windows)命令来追踪从你的电脑到UCLA服务器的网络路径，放上屏幕截图并回答下列问题：

    a.	请描述路径经过的地理位置，以及传输所需要的时间

    b.	第一个路由器的ip地址是多少？你认为第一个路由器在哪里？

    c.	为什么UCLA的服务器不在LA？

5. IPV4和IPV6都是互联网协议，用于在网络上标识不同的设备。请查询资料，描述IPV4和IPV6的区别。描述中至少需要对比两种协议的地址长度，地址表示方式，可分配地址数量等方面的区别。

6. 【选做】第一题中，如果我们通过计算机的设置来查找IP，显示的IP地址通常是以192.168开头。但在百度中搜索IP，显示的结果又不一样。为什么会有这样的差异？

提交方式：Word文档，截止本周日晚10点。


