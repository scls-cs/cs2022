---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
rise:
  start_slideshow_at: beginning

kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Problem Set 7 #

## Warming Up ##
Python has a built-in module that you can use to make random numbers: **random**, which you will use in the next problem.

Run the following code 3 times and observe the results.

```{code-cell} python3

import random

print( random.randint(1,10) )        # 产生 1 到 10（包含）的一个整数型随机数  
print( random.random() )             # 产生 0 到 1 之间的随机浮点数

```

## Quiz ##

Teachers often use quizzes to evaluate students. Now it's time to create your own quiz.

**This is the list of features your quiz needs to have:**

1. Contain **FIVE OR MORE** questions. 
2. Include a question which use a number as an answer(e.g., what is 1+1?)
3. Include a multiple-choice question(e.g., Which of these choices are correct?A, B, C or D?)
4. Include a question which use text as answer(e.g., Which country is ranked first in women's football?)

You need to keep track of how many questions they get correct.
At the end of the program print the percentage of questions the user gets right.

The output should be like this:
```python
Quiz time!

How many books are there in the Harry Potter series? 7
Correct!

What is 3*(2-1)? 3
Correct!


小明从A班转到了B班，两个班级的平均智商都提高了，这可能么？
A. 可能
B. 不可能
C. 不确定
? A
Correct!

Who is on the front of a one dollar bill?
1. George Washington
2. Abraham Lincoln
3. John Adams
4. Thomas Jefferson
? 2
No.

Congratulations, you got 3 answers right.
That is a score of 75.0 percent.
```
## Guessing Game ##

You are going to make a simple guessing game where the computer will generate a random number between x and y, and the user has to guess it in certain attempts.

Based on the user's guess computer will give various hints if the number is high or low. When the user guess matches the number computer will print the answer along with the number of attempts.

The output should be like this:
```python
GAME LOADING...

What is the lower bond of the number? 
3
What is the upper bond of the number?
50
Generating random numbers between 3-50....

How many tries for the player to win?
5

GAME READY. Now let's play!

Hello, What's your name?
Derek

Hi Derek, you are going to guess a number between 3 and 50.
You have 5 tries to win the game. 

Your first guess is: 2
Your guess is too low

Your next guess is: 4
Your guess is too low

Your next guess is: 6
You win the game in 3 tries!
```

If the player failed to guess the number within 5 times, give a reasonable output accordingly. 

:::{important}
In order to design the game, you have to use a control structure called **loop**, so that the player could guess repetitively. 

Also, you want to quit the game when player guessed the number. You need to use another command called **break**, which terminates the loop in advance.

You can check the links below, or search online how to use loop and break:

https://www.runoob.com/python/python-while-loop.html
https://www.runoob.com/python/python-break-statement.html

The part of the loop is provided.
:::

```{code-cell} python3

import random

i=0
while(i<5):   #change the number 5 to the actual tries
  #add code here
  if(when user make a correct guess): 
    break  
    
  i=i+1 #do not change this line
    
```

## Submission ##

Submit the homework via 钉钉作业本 by Sunday 22PM. 
