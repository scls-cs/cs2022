OpenCV安装
**********

1. 在命令行配置python
------
在PyCharm下方点击Terminal,输入

.. code-block:: text

        python3 --version

按下回车。这个命令可以用来判断Terminal所使用的python版本，也经常用来判断Terminal是否已经安装了python命令。如果你看到的是Python 3.10.4（如下图所示），那么说明你已经安装成功。如果出现的是python command not found，那么说明你的Python没有安装成功，请重新回顾上次作业的步骤。

.. image:: terminal.png
   :scale: 30%


**For Windows User**: 输入

.. code-block:: text

        python -V

按下回车。如果显示python版本，说明python命令安装成功。


如果没有任何结果，说明终端没有安装python命令。你需要重新安装一遍python。

安装完毕之后，在命令行中再次输入python -V，则会出现python的版本。


2. 下载并安装pip命令
--------------

下载并安装pip命令。pip是Python的包管理工具，可以通过pip方便的下载并安装Python的函数包。

输入curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py，按下回车并等待下载pip脚本（可能会持续2-10分钟左右）。

输入

.. code-block:: text

    python3 get-pip.py -i https://pypi.tuna.tsinghua.edu.cn/simple/  --trusted-host pypi.tuna.tsinghua.edu.cn

(Windows的同学将python3换成python即可）


3. 下载并安装OpenCV函数库
---------

OpenCV是一个跨平台计算机视觉库，可以运行在Linux, Windows和MacOS操作系统上。它实现了图像处理和计算机视觉方面的很多通用算法，例如图像特征提取、人脸识别、手势识别、人机交互等。我们在这次作业中，需要用到OpenCV的部分函数来进行实验。

输入下面命令：

.. code-block:: text

        pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ numpy

再输入下面命令：

.. code-block:: text

        pip install -i https://pypi.tuna.tsinghua.edu.cn/simple/ opencv-python


4. 新建一个文件
--------------

我们已经成功安装好OpenCV函数库，接下来我们要开始完成图像滤镜的实验了。运行PyCharm，打开上周的Project（也可以新建一个Project)，新建一个python文件，取名image.py。

.. image:: new_file.png
   :scale: 30%

现在我们的工程中有两个python文件。第一个loop.py是我们之前创建的，image.py是我们刚刚新建的。所以接下来我们需要让PyCharm知道我们要运行image.py，而不是loop.py。到这一步你其实应该知道怎么做了。

5. 配置运行的python文件
--------------

点击右上角edit configuration（现在可能显示的是loop), 在script path中选择image.py，点击open，然后apply。现在我们已经让PyCharm知道，接下来运行image.py这个程序，而不是其它的文件。

.. image:: script.png
   :scale: 30%

6. 开始编写程序
-------------

在image.py中的第一行输入：

.. code-block:: text

       import cv2

这一行的作用是导入OpenCV的函数包。如果你发现这一行的下面出现了一根红线，将鼠标移到这一行上，旁边会出现一个"install opencv-python"的提示，点击它，等待它安装好就可以了。安装过程可能会持续1，2分钟的时间。安装完毕之后，红线会自动消失，说明我们已经成功将OpenCV函数包导入进PyCharm了。


到这一步，我们就完成了所有的配置工作。我们接下来就可以开始完成作业了。

7. 图像处理步骤
------------
首先将要处理的图片放入项目中。这个步骤非常简单，你可以直接将图片文件用鼠标拖到项目中。**图片需要和python文件在同一个目录下。**

.. image:: img.png
   :scale: 40%

.. note::

    图片一定要与python文件放在同一个文件夹下，否则可能会无法加载图片。不要把图片放在一个单独的文件夹中。

接下来大家可以按照网站的要求来编写代码。
