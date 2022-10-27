if-else
=======

双分支语句
-------
条件判断语句（或if语句）可以让程序根据条件是否满足来做判断/决策。有时候你会希望程序可以做更多的决策，如果条件满足，就去做事情A；但如果条件不满足，就不去做事情A而去做事情B。Python中这种类型的决策用if-else语句来实现。

.. code-block:: python

    if(expression):
        A
    else:
        B

如果条件成立，Python解释器会执行A，而会跳过B不执行；反之条件不成立，就会跳过A而只执行B。

罗伯特.弗罗斯特有一首诗，“黄色的树林里分出两条路，可惜我不能同时去涉足。”这首诗浪漫而深刻的揭示了if-else语句的特点：A和B有且只有一个会被执行。if-else语句又被称为双分支语句。条件就是岔路口，程序根据条件的真假来决定走哪个方向。是不是很形象呢？

.. note::

    和if语句一样，if-else语句也需要遵守缩进规则。

if嵌套
-------

if语句可以嵌套在另一个if语句中。这个时候else与哪一个if进行匹配呢？else与同一层次中，最近的那个if进行匹配。

.. code-block:: python

    if(num>0):
        if(num%2==0):
            print("A")
        else:
            print("B")

.. code-block:: python

    def message(a, b, c):
        if(a < 10):
            if (b < 10):
                print("X")
            print("Y")
        if (c < 10):
            if (b > 10):
                print("Y")
            else:
                print("Z")

    message(5,15,5) #print two lines of "Y"

解一元二次方程

.. code-block:: python

    import math
    def solve():
        a = float(input("Enter coefficient a: "))
        b = float(input("Enter coefficient b: "))
        c = float(input("Enter coefficient c: "))

        delta = b*b-4*a*c
        if(a!=0):
            if(delta >= 0):
                x1 = (-b+math.sqrt(delta))/(2*a)
                x2 = (-b-math.sqrt(delta))/(2*a)
                print(x1, x2)
            else:
                print("No real roots")
        else:
            print(-c/b)

    solve()

课件
----
:download:`if-else <双分支结构.pptx>`.

作业
---------
完成 :ref:`hw5`