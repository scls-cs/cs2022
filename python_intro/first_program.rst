走近Python
========

为什么要学习Python?
-----------------

为什么要学习编程？为什么要学习Python?
微信、百度、知乎、豆瓣、B站、小红书...这些APP的名字你都听说过吗？它们有一个共同特点：都使用Python进行开发！根据TIOBE编程社区指数显示，Python是目前全世界最受欢迎的语言。

第一个Python程序
---------------
.. code-block:: python

  a = 1   #定义变量a并初始化

  b = 2   #定义变量b并初始化

  a = (a+1)*(b+2) #将表达式结果赋给变量a

  print(a)  #打印变量a的值

名词解释
+++++++

.. glossary::

  变量（Variable)

    用来保存程序数据。使用使用变量前需要对变量进行定义。

  赋值符（Assignment operator)

    作用是将符号右边的值赋给左边的变量。

  print()

    Python的命令，作用是打印括号中的值。

  注释（Comment）

    对代码的解释与说明。注释不会被执行。


计算机是如何运行程序的？
+++++++++++++++++

实际上，计算机并不能直接执行Python语言。程序在运行前，需要先翻译成计算机能懂的语言（也就是二进制），这一步是靠解释器（Python interpreter)来实现的。

在运行程序时，解释器是从上到下依次执行语句的。注释会被跳过。

编程工具
-------

编程工具是我们编写并运行Python代码的工具。前几节课我们会使用OnlineGDB编程，它使用起来很方便，很适合我们初学者快速上手。

编程工具又被称作编程环境，实际上后面这种说法更为常见。

.. note::

  **问：既然注释不会被运行，那为什么我要写注释呢？**

  答：注释的目的是让人们（包括你自己）能够更加轻松地了解代码。虽然不会被解释器执行，但注释是一个非常好的习惯，它相当于帮助你做笔记。如果有人想学习如何使用你的代码，看到注释就会更容易理解你的程序。

  **问：我可以用word来写程序吗？**

  答：不可以，因为word里没有Python解释器。

.. _get2022:

作业：get2022
---------------

定义变量a并将其初始化为1，如何仅仅通过对变量a进行运算操作，将其自身的值变为2022？

**注意：只可以使用四则运算，只可以使用一个变量。不可以使用循环。**

.. code-block:: python

  a = 1

  #write your code here

  print(a)

作业要求：请在onlinegdb上进行编程，将程序窗口（包含运行结果）进行截图。请计算运算符的使用个数。将截图和运算符个数在钉钉上进行提交。

**截止时间：本周日（9月11日）晚上8点。可以反复提交，但切勿错过截止时间。**

课件
----

:download:`信息技术第一讲课件 <认识Python程序.pptx>`.

.. _good_hw1:


优秀作业
-------
10次运算
+++++++
.. code-block:: python

    a=1     #liyuzhou
    a=a+a
    a=a*a*a+a
    a=a*a*a+a+a/a
    a=a+a
    print(a)


12次运算
++++

.. code-block:: python

    a=1   #dingchengtian
    a=a+a
    a=a+a+a
    a=((a+a)/a+a)*(a/a+a)*a*a+a



13次运算
++++

.. code-block:: python

    a = 1 #yuanzihao

    a=a+a
    a=a*a*a+a
    a=(a*a*a+a+a/a)*(a/a+a/a)
    print(a)

.. code-block:: python

    a = 1 #zhangyiyao

    a=a+a+a+a+a
    a=(a+a-a/a)*a
    a=a*a
    a=a-(a+a+a)/a
    print(a)

.. code-block:: python

    a = 1 #liyue

    a=a+a
    a=a*a+a/a
    a=a*a+a*a-a
    a=a*a-(a+a+a)/a
    print(a)

