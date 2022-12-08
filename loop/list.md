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

# 列表 #

上一章我们学习了控制结构的第一种：分支结构。这一章我们会见到控制结构的第二种，也是最后一种结构：循环结构。不管程序有多么复杂，它都可以分解为顺序结构、分支结构和循环结构。

也就是说学完这章后，你就可以开始写更复杂的程序了。

在 Python 中，列表是一种可以通过索引/下标(index)访问的元素的集合。索引是一个数字值，表示元素在列表中的位置。

列表是可变的，也就是说它们在创建后可以修改。

## 创建列表 ##

要创建一个列表，可以使用方括号 [] 并用逗号将列表中的元素隔开。例如：

```python
colors = ['red', 'green', 'blue']
```

要访问列表中的一个元素，可以在列表名称后面使用方括号，并指定元素的索引。在 Python 中，列表的索引从0开始，因此列表中的第一个元素的索引为 0，第二个元素的索引为 1，依此类推。例如，下面的代码访问了列表中的第一个和第三个元素：

```python
first_color = colors[0]
third_color = colors[2]
```

你还可以修改列表元素：

```{code-cell} python3
colors = ['red', 'green', 'blue']
colors[1] = 'purple'
print(colors)
```

## 列表方法 ##

Python中列表还有许多其他有用的方法，可以使用这些方法来修改和处理列表中的元素。例如，可以使用append()在列表末尾插入新的元素，使用**insert()** 方法在列表中插入一个元素，使用 **remove()** 方法从列表中删除一个元素，使用 **sort()** 方法对列表中的元素进行排序，以及使用 **len()** 函数来获取列表中元素的数量。

```{code-cell} python3
# Create an empty list
my_list = []

# Add an item to the list
my_list.append('hello')

# Insert an item at a specific index
my_list.insert(1, 'world')

# Remove an item from the list
my_list.remove('hello')

# Sort the items in the list
my_list.sort()

# Get the number of items in the list
list_length = len(my_list)
```

## 作业 ##

1. Write a function which use while loop that iterates over a list of numbers and prints each number on a new line.

```{code-cell} python3
def printAll(x):
	#your code


l = [1,2,3,4,5,6]
printAll(l) #should print each number on a new line
```

2. Modify the while loop from the first question so that it only prints numbers that are even.

```{code-cell} python3
def printAllEven(x):
	#your code


l = [1,2,3,4,5,6]
printAll(l) #should print 2,4,6
```

3. Write a function using while loop that adds up all the numbers in the list and prints the total at the end.

```{code-cell} python3
def addAll(x):
	#your code
	return 0


l = [1,2,3,4,5,6]
print(addAll(l)) #should get 21
```

4. Modify the while loop from the third question so that it only adds up numbers that are odd.

```{code-cell} python3
def addAll(x):
	#your code
	return 0


l = [1,2,3,4,5,6]
print(addAll(l)) #should get 9
```






