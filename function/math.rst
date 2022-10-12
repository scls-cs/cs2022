数学函数
=======

数值处理
------

数值处理Python最典型的应用之一。除了前面见过的四则运算和模运算以外，Python还可以进行更为复杂的运算。这些复杂运算没有对应的运算符，而是通过函数来实现。这些函数叫做标准库函数，是Python已经设计好的函数，我们只需要直接调用即可。

标准库是Python为我们提供的一份巨大宝藏，里面有成千上万个函数等待我们去使用。这些函数功能包罗万象，除了我们马上要见到的数值处理以外，还有操作系统、数据库、图像处理、电子邮件、网页设计......

为了更方便的维护标准库，Python根据这些函数的功能特点，将它们打包成了一个个模块（module）。

.. code-block:: python

    import math
    print(math.pow(2,4))    #output:16.0

* import math：导入math这个模块。
* math.pow(x, y)是math模块中的函数，作用是计算x的y次幂并返回。调用方法是模块名加函数名，中间用点分开。

.. note::

    import是Python里的关键字，表示导入其他模块，这样可以使用该模块的函数。

math模块的函数
------------

* math.pow(x,y)    #返回x的y次幂
* math.fabs(x)     #返回x的绝对值
* math.sin(x)      #返回x的正弦值
* math.cos(x)      #返回x的余弦值
* math.sqrt(x)     #返回x的算术平方根
* math.factorial(x)#返回x的阶乘

课件
------
:download:`数学函数 <数学函数.pptx>`

作业
---
:ref:`hw3`

