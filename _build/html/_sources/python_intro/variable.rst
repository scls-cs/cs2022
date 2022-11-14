.. _variable:

变量与数据类型
============

数据类型
-------

Python提供了可以广泛应用的数据类型。在前面一节我们已经见过字符串，字符串是一种数据类型。Python共提供了六种数据类型：数字、字符串、列表、元组、集合、字典。后面四个我们通常称为数据结构，它们应用非常广泛，我们会在后面详细介绍它们。这一节我们先看看前两种数据类型：

数字类型数据包括：

.. glossary::

      整数（int)：

        比如5，-81，19452

      浮点数（float):

        比如0.5，-5.2，2016.1453

      布尔值（boolean)：

        True和False

      复数（complex)：

        比如3+5j

字符串类型数据需要由单引号或双引号括起，例如"Good morning!"，或者‘hello world’。

虽然单引号和双引号都可以表示字符串，在实际编写代码过程中，最好遵循统一的标准，不要将单引号和双引号混合使用。
可以使用type()命令查看数据类型:

.. code-block:: python

    print(type(12))    #int
    print(type(5.0))   #float
    print(type(True))  #bool
    print(type(4+3j))  #complex

变量
----
我们可以直接使用数据，也可以将数据保存到变量中，方便以后使用。但是请你先记住一条规则：**变量必须有名字**。

下面两个代码实现同样的功能：

.. code-block:: python

    print("Good morning!")   #不使用变量

    a = "Good morning!"      #使用变量a来存储字符串
    print(a)

在Python中，变量无须声明类型，并且变量类型可以随时改变。例如，同一个变量可以一会儿被赋值为字符串，一会儿被赋值为整数。所以Python又被称作“弱类型语言”(Strongly-typed language)。

.. note::

  注意，弱类型并不等于没有类型！弱类型是说在书写代码时不用刻意关注类型，但是在编程语言的内部仍然是有类型的。



.. code-block:: python
    a = "Good morning!"    #a是字符串
    a = 1                  #a是整数

变量命名规则
----------

* 名称只能由数字、字母（包括大写字母和小写字母）和下划线组成。
* 第一个字符不能用数字。
* 只要符合上述两条规则，你就可以随意地命名，但还要避开Python的关键字。

变量命名规范
----------

* 可以自我描述。
* 全小写，单词用下划线连接
* 不要过长

类型转换
---------

将一种数据类型（整数，字符串，浮点数等）的值转换为另一种数据类型的过程称为类型转换。

我们已经学习了三种数据类型：
* 整型（int）
* 浮点型（float）
* 字符串型（str）
Python中提供了几组类型转换的函数，可以将一个类型的变量转换为另外一种类型。
* int()：将浮点数或者字符串转化为整数。浮点数去掉小数点后的数值，仅保留整数部分。
* float()：将整型或者字符串转换为浮点数。
* str()：将整型或者浮点数转化为字符串。

.. code-block:: python

        a = 1
        print("The type of a is", a)     #output:int
        b = float(a)                     #将整型数据转换为浮点型
        c = str(a)                       #将整型数据转换为字符串型

        print("The value of b is", b)      #output: 1.0
        print("The type of b is", type(b)) #output: float

        print("The value of c is", c)      #output: "1"
        print("The type of c is", type(c)) #output: str

课件
----

:download:`变量与数据类型 <变量与数据类型.pptx>`.

作业
-------

:download:`类型转换编程作业 <类型转换编程作业.pdf>`.

有三点需要注意：

1. input()函数是将键盘输入结果保存到变量里，所以需要你输入数据；如果没有键盘输入，程序会停留在input()等待；

2. 执行input()时，屏幕上会先打印括号里的内容，例如"What is your name?"

3. 变量命名要符合相应的规则，不可以出现空格。

大家可以参考下面的程序，关注程序是如何打印结果的，以及倒数第二行int()的作用。

.. code-block:: python

    name1 = input("Enter name : ")
    print("Your name:", name1)

    num = int(input ("Enter number :"))
    print("Your number:",num)

    # Printing type of input value
    print ("type of number", type(num))
    print ("type of name", type(name1))

    new_num = int(num)
    print ("type of new number", type(new_num))


如果你想了解类型转换更多的细节，可以参考：https://www.w3school.com.cn/python/ref_func_int.asp


