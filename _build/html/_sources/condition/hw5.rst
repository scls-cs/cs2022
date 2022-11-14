.. _hw5:

Problem Set 5
======================
1. Rock, Paper, Scissors
------------

Create a function which takes two strings(P1 and P2), as arguments and returns a string stating the winner in a game of Rock, Paper, Scissors.

Each argument will contain a single string: "Rock", "Paper", or "Scissors". Return the winner according to the following rules:

* Rock beats Scissors
* Scissors beats Paper
* Paper beats Rock

The parameters and return value of the function should be like:

.. code-block:: python

    rps(“Rock”, “Paper”) -> “The winner is P2”

    rps(“Scissors”, “Paper”) -> “The winner is P1”

    rps(“Paper”, “Paper”) -> “It’s a draw”

Part of the method might be like this:

.. code-block:: python

    def rps(s1, s2):
        if(s1==s2):
            print("It is a draw")
        else:
            if(s1 == "Rock"):
                if(s2 == "Scissors"):
                    print("First player wins")
                else:
                    print("Second player wins")

2. Leap Year
------------
Write a function checkLeapYear(year) to determine is the year is a leap year or not. The definition of the leap year is this:

https://blog.csdn.net/shaier/article/details/2034196

注："世纪年"就是能被100整除的年份。

The parameters and return value of the function should be like:

.. code-block:: python

    checkLeapYear(1000) -> True

    checkLeapYear(1600) -> True

    checkLeapYear(1900) -> False

    checkLeapYear(2008) -> True

    checkLeapYear(2013) -> False



Submit:
-----------

Put all your work into one python file, and share your project link via 钉钉作业本。Please submit by Oct 30th, 22PM.

