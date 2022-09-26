字符串
=======

文本
-------
字符串是一种重要的数据类型。在编程语言中，我们通常用**字符串**来表示文本数据，例如一个句子、一个段落、一首诗......字符串用单引号或者双引号括起来。

.. code-block:: python

        word = "Bye"

        sentence = "Good morning!"

        paragraph = "It was the best of times, it was the worst of times, it was the age of wisdom, it was the age of foolishness, it was the epoch of belief, it was the epoch of incredulity, it was the season of Light, it was the season of Darkness, it was the spring of hope, it was the winter of despair, we had everything before us, we had nothing before us, we were all going direct to Heaven, we were all going direct the other way--in short, the period was so far like the present period that some of its noisiest authorities insisted on its being received, for good or for evil, in the superlative degree of comparison only."

连接两个字符串(String Concatenation)
--------
可以使用+将两个字符串连接起来：

.. code-block:: python

    start = "Python "
    middle = "Rules "
    print(start + middle + "The World! ")

Python中不支持将字符串和数字直接进行连接。如果你想要这么做，你需要先将数字转化为字符串。

.. code-block:: python

    first = "This year is "
    year = 2022
    result = first + str(year)    #将数字转化为字符串
    print(result)

字符串函数
--------

你可以把字符串想象成排成一列的字符。每个字符有各自对应的编号：第一个字符编号为0，第二个字符编号为1.... 最后一个字符的编号最大。

.. image:: str.png
  :width: 400

从0开始编号可能会让有些同学不太舒服，毕竟我们习惯从1开始计数。但在99%的程序语言里，元素的位置，或者索引(index)都是从0开始的。

Python为字符串提供了很多函数，例如``code`` ``len(x)``负责返回字符串x所包含的字符个数，包含空格和各类标点符号：

.. code-block:: python

    x = "Cat"
    y = "Hi there!"

    print(len(x))    #output: 3
    print(len(y))    #output: 9