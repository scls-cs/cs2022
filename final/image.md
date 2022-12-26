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

# 图像处理 #

## 任务一：描述图片 ##

打开https://pixspy.com/，上传任意一张照片。鼠标在图片上移动，观察鼠标旁的数字，回答以下问题：

![motor](motorcycle.png)

1. 鼠标旁的五个数字分别代表图片的什么信息？
2. 图片的分辨率是多少？
3. 图片左上角的行下标和列下标分别是多少？
4. 图片最右处的列下标是多少？
5. 图片最底部的行下标是多少？
6. 行下标是从左往右增大，还是从上到下增大？
7. 用鼠标滚轮放大图片，直到看到一个个"马赛克"为止。它们其实是像素，当像素放大到一定程度，看起来就像是小色块。这叫做图像的像素化（pixelation）。

## 任务二：图像处理 ##

即使一张图片由上百万个像素点组成，计算机仍然能够在你喝一口水的时间内，对它们全部进行处理。这个任务中你将要编写三个函数，来实现一些神奇的效果。


```{code-cell} python3
import cv2
img = cv2.imread('beach.jpeg') 

totalCol= img.shape[1]  #image width
totalRow= img.shape[0] #image height

print(totalCol, totalRow) #print image width and height

for i in [0]:
  for j in range(10):
    print(img[i,j])
```
1. 鼠标旁的五个数字分别代表图片的什么信息？
2. 图片的分辨率是多少？
3. 图片左上角的行下标和列下标分别是多少？
4. 图片最右处的列下标是多少？
5. 图片最底部的行下标是多少？
6. 行下标是从左往右增大，还是从上到下增大？
7. 用鼠标滚轮放大图片，直到看到一个个"马赛克"为止。它们其实是像素，当像素放大到一定程度，看起来就像是小色块。这叫做图像的像素化（pixelation）。