.. _hw4:

Problem Set 4
======================
1. Try it out
------------
Given the following programs, first try to predict the results. Then write the programs to your editor. Run it, observe the results, and see if it matches your prediction.

Typing by yourself if highly recommended, but copy and paste it is also fine as well.

.. code-block:: python
    regularPrice = 100;
    onClearance = True;
    hasCoupon = False;
    finalPrice = regularPrice
    if(onClearance):
        finalPrice = finalPrice - finalPrice * 0.25
    if(hasCoupon):
        finalPrice = finalPrice - 5.0
    print(finalPrice)

.. code-block:: python
    x = 7
    if (x < 7):
        x = 2 * x
    if (x % 3 == 1):
        x = x + 2;
    print(3 * x);

2. Function with if statement
----------------
Write the following functions to your editor. Describe what each of the functions does, which you will add it besides the function as comment using #.

.. code-block:: python

    def getGPA(grade):
        if(grade > 90):
            return 'A'
        if(grade > 80):
            return 'B'
        if(grade > 70):
            return 'C'
         return 'D'

.. code-block:: python

    def magic_string(s):
        s1 = s[0:len(s)//2]
        s2 = s[len(s)//2:]
        return s1 == s2

3. Write your own function
----------------------
Distance II
+++++++++++
In :ref:`distance`, if the line of two points is vertical, the program will crash since the slope would be infinity. Modify your program so that it could print the correct output without crashing.

Solve II
+++++++++++
In :ref:`solve equation`, it is not required to check the delta, as well as the first coefficient. Modify the program so that if could print the correct output even if the a==0, or delta<0.

Narcissistic Number
+++++++++++++++++++
**Narcissistic Numbers** are defined as follows: An n-digit number is narcissistic if the sum of its digits to the nth power equal the original number. For example with 3 digits, say I choose the number 153: :math:`153 = 1^{3} + 5^{3} + 3^{3}`. So 153 is a Narcissistic Number.

Write a function called check(), to determine if a 3-digit number which user input is a Narcissistic Number. For example:

* input: 153
* output: "153 is a Narcissistic Number"

* input: 165
* output: "165 is not a Narcissistic Number"


Submit:
-----------

Put all your work into one python file, and share your project link via 钉钉作业本。Please submit by Oct 23th, 22PM.

