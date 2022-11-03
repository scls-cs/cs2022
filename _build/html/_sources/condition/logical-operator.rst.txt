逻辑运算符
=======

布尔运算
-------
乔治.布尔在提出布尔代数的同时，还规定了布尔代数的运算方式，也就是布尔运算（boolean operation)。布尔运算包含三种基本运算符：and，or，not。


and
++++
先来看and运算。这里P和Q都是布尔值。将P、Q的所有组合对应的结果表示出来，如下表所示：

.. list-table::
   :widths: 25 25 50
   :header-rows: 1

   * - P
     - Q
     - P and Q
   * - True
     - True
     - True
   * - True
     - False
     - False
   * - False
     - True
     - False
   * - False
     - False
     - False

and运算又称为逻辑与运算：当且仅当P和Q同时为真的时候，P and Q为真；否则P and Q为假。

上表叫做真值表（Truth Table），它列出了所有可能的运算组合。真值表和逻辑运算一一对应。

or
+++
同样，我们可以写出or的真值表：

.. list-table::
   :widths: 25 25 50
   :header-rows: 1

   * - P
     - Q
     - P or Q
   * - True
     - True
     - True
   * - True
     - False
     - True
   * - False
     - True
     - True
   * - False
     - False
     - False

or运算又称为逻辑或运算：P和Q至少有一个为真的时候，P or Q为真；否则P or Q为假。

not
++++
not的真值表：

.. list-table::
   :widths: 25 50
   :header-rows: 1

   * - P
     - not P
   * - True
     - False
   * - False
     - True

示例代码
+++++++
.. code-block:: python

    a = 10
    b = 10
    c = -10

    if a > 0 and b > 0:
        print("The numbers are greater than 0")

    if a > 0 and b > 0 and c > 0:
        print("The numbers are greater than 0")
    else:
        print("At least one number is not greater than 0")

    #output: "The numbers are greater than 0"
    # "At least one number is not greater than 0"

.. code-block:: python

    a = 10
    b = -10
    c = 0

    if a > 0 or b > 0:
        print("Either of the number is greater than 0")
    else:
        print("No number is greater than 0")

    if b > 0 or c > 0:
        print("Either of the number is greater than 0")
    else:
        print("No number is greater than 0")


    #output: "Either of the number is greater than 0"
    # "No number is greater than 0"

.. code-block:: python

    x = 50

    if not (x>10):
        print("x is no greater than 10")

    if not (20 <= x < 40):
        print("x is outside")

    #output: "x is outside"


.. code-block:: python

    def leapYear(year):
    if(year<1582):
        return year%4==0
    else:
        return (year%400==0) or (year%100!=0 and year%4==0)



课件
----
:download:`logical operators <逻辑与多分支结构.pptx>`.

作业
---------
完成 :ref:`hw6`