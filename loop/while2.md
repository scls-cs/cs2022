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

# while循环 II #

## Ex0 ##
指出下面程序的bug:

```{code-cell} python3
def test():
    counter = 0;
    while counter > 100
        if (counter % 2 == 1):
            cout << counter << " is odd." << endl;
        else
            cout << counter << " is odd." << endl;
            count = count + 1
#test()
```

while循环又称为"当型循环"：当条件为真时，循环执行某段程序。

我们写while循环的时候，确定循环条件是最关键的步骤之一。

## Ex1 ##

下面程序的循环条件是什么？最后打印的值代表什么含义？

```{code-cell} python3
i = 1
sum = 0
while(sum<1000):
    i=i+1
    sum = sum + i

print(i-1)
```

## Ex2 ##
下列程序的循环条件是什么？最后的count代表什么含义？

```{code-cell} python3
def f(str):
    count = 0
    i = 0
    while(i < len(str)):
        if(str[i] == 'a'):
            count = count+1
        i = i+1     
    return count
```

## Ex3 ##

Print the square roots of the first 25 odd positive integers.

```{code-cell} python3
import math
def print():
    #add your code here
    
print()
```

## Ex4 ##

2019年年末中国人均GDP为10276美金，也是首次超过10000美金。一般来说，如果人均GDP超过2万美金，则说明该国家称为了中等发达国家。

假设中国人均GDP年平均增长率为3.5%，请问中国成为中等发达国家的时间是？

```{code-cell} python3
def calculate():
    year = 2019
    gdp = 10276
    while():
        
    
print(calculate())
```