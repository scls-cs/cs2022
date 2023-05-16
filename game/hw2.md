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

# 作业 #

作业一：在上次作业的基础上，完成小球的斜线碰撞模拟。不考虑重力和能量损耗。

作业二：在作业一中引入重力因素（重力加速度自行指定），完成小球的碰撞模拟。不考虑能量损耗。
[gravity](gravity.gif)

作业三：运行示例程序，并回答如下问题：

1. 结合[move](move.md)中按键操纵的内容，指出白色边框，以及球拍初始位置的四个顶点的坐标。

2. 假如球拍的初始位置如图所示，请问paddle_x和paddle_y应该如何修改？[paddle_pos](paddle_pos.png)？要求写成Square properties和Paddle properties的函数形式。

3. 哪些指令实现了键盘操纵球拍水平运动？

4. 目前球拍移动会超出白色边框。请指出原因，并说明应该如何修改代码使得球拍只在白色边框内部移动。

5. 如果希望球拍除了水平运动以外，还可以上下移动，应该如何修改代码？

作业四：

设计游戏：

球拍初始位置：球拍中心位于白色边框中轴线上，球拍下方离白色边框为10个像素距离。

球拍运动范围：如蓝色部分所示。[range](range.png)

小球在白色边框内部做斜线碰撞，碰到球拍后会反弹。不考虑重力和能量损耗。小球如果碰到白色边框底部，游戏失败。

[bounce](bounce.gif)

【附加题】
有一个小恶魔在白色边框中随机出现，你的任务是尽可能多的击中它。如果小球击中它，游戏加一分。游戏如图所示：

[score](score.gif)


## 提交 ##

其中作业一、二、四提交在main.py中，作业二和作业五提交在homework.txt里。

提交链接：https://replit.com/team/SCLS-CS2022/Game-II
