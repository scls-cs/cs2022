if
=======

逻辑代数
-------
1854年，英国数学家乔治.布尔（George Boole）出版了The Laws of Thought，这本书中他提出了逻辑代数的概念。逻辑代数只包含两个数值：

* False
* True

逻辑代数的提出诞生了一门新的学科：数理逻辑。这门学科对现代计算机的发展具有决定性的意义。人们为了纪念布尔，逻辑代数又被称作布尔代数，也就是我们已经在前面学过的的布尔值。

布尔表达式（boolean expression）是值为布尔类型（True和False）的表达式。关于数据类型，你可以回顾 :ref:`variable` 这一节。

比较运算符
--------

.. code-block:: python

    age = 18
    print(age == 18)    #True
    print(age+1 == 18)  #False


上一段代码中，age == 18就是一个布尔表达式。翻译成普通话就是：age变量的值等于18吗？这个问题只有两种答案：真或者假。

.. note::

    ==是判断符号两边是否相等，=是将右边的值赋给左边变量。

除了==以外，还有一些运算符也用来构成布尔表达式，例如>，<，>=, <=，这些符号叫做比较运算符（comparison operator），负责比较符号两边值的大小。运算结果也是布尔值。

.. code-block:: python
    age = 15
    year = 14
    print(age < year)
    print(age > year)
    print(age <= year+1)
    print(age-1 >= year)

用!=来判断符号两边的值是否不相等。

.. code-block:: python

    grade = 59
    print(grade != 60)    #True

数学运算与函数
------------
.. code-block:: python

    base = 2
    print(math.pow(base, 9) > 1000)
    print(math.pow(base, 10) > 1000)

    print(10%3 == 1)

字符串函数
--------
除了数值外，字符串也可以比较大小。字符串是按字符逐个进行比较的。如果两个字符串含有完全相同的字符，那么这两个字符串的值相等。

.. code-block:: python

    str1 = "Hi"
    str2 = "Hi"
    print(str1 == str2)    #True

如果逐个字符比较的过程中，发现两个字符不一样，那么就会比较字符的Unicode。哪个字符的Unicode大，该字符所对应的字符串的值就更大。

.. code-block:: python

    s1 = "cat"
    s2 = "cup"

    print(s1 < s2)    #True, since the unicode of a is less than u

课件
----
:download:`条件判断 <条件判断.pptx>`.

作业
---------
完成 :ref:`hw4`