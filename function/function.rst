引入函数
===========

函数模版
-------

.. code-block:: python

    def function_name(arguments):
        """A docomentation string. """
        # Your function's code goes here.
        # Your function's code goes here.
        # Your function's code goes here.
        return some_value

1. **函数引入了两个新关键字：def和return**

这两个单词在解释器里会自动高亮显示。def指定函数名称，并列出函数的所有参数。return的作用是向调用这个函数的代码返回一个值。

2. **函数可以接收参数**

参数是传递给函数的值，放在函数名后面的括号中。不过无论括号里是否有参数，函数名后面都要加一个括号。

3. 函数包括代码，（通常）还有文档

代码在def下要锁进一层。

.. note::

    Python使用“函数”这个词描述一个可重用的代码块。其他编程语言也可能使用“过程”、“方法”等名字，这些词语它们指代的是同样一个事物。

函数示例
------
计算小狗的年龄
++++++++++++
.. code-block:: python

    def dog_age():
        birth_year = input("你家小狗的出生年份是？")
        current_year = input("今年是几几年？")
        age = int(current_year) - int(birth_year)
        print(age)

我们将4行代码转换了一个函数：dog_age()。下面我们来调用这个函数：

.. code-block:: python

   def dog_age():
        birth_year = input("你家小狗的出生年份是？")
        current_year = input("今年是几几年？")
        age = int(current_year) - int(birth_year)
        print(age)

   dog_age()    #调用函数


调用函数也就是执行函数。可以把函数理解成一台"电风扇"。每次打开电风扇的开关，就是一次"电风扇"的调用。如果没有函数调用，那么函数就不会被执行。

调用函数的方式就是提供函数名和参数值，参数值用括号括起来。如果没有传递参数，那么括号里面为空。

.. _geo:

Geometry Formulas
+++++++
.. code-block:: python

        def get_circle_area():
            r = float(input("Please enter the radius: "))
            print(3.14*r*r)

        def get_rec_area():
            a = float(input("Please enter side a: "))
            b = float(input("Please enter side b: "))
            print(a*b)

        def get_square_area():
            a = float(input("Please enter side a: "))
            print(a*a)

        get_circle_area()
        get_rec_area()
        get_square_area()

函数调用过程
---------
函数的执行过程分为三步：

1. 函数的调用
2. 函数体执行
3. 返回

解释器遇到函数调用语句后，会跳转到函数体内部。函数体语句执行完毕后，解释器会跳回到调用处，开始执行接下来的语句。

函数如果只定义，但是不被调用的话，函数体是不会被执行的。

作业
---------
完成 :ref:`hw1`