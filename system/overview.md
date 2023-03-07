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


# 计算机网络概论 #

* 互联网的所有设备都有一个IP地址。


* IP地址的格式：x.x.x.x，每个x都是一个8位二进制数。所以IP地址由32位二进制数组成。


* 域名是IP地址的别称，为了方便人类记忆。比如Google主页的IP地址之一172.217.25.14，域名是google.com。


* DNS服务器里存储域名和IP地址的对应关系。


* 可以通过nslookup命令来查找域名对应的IP地址。如果你用Mac，在Launchpad里面搜索"Terminal"。如果你用的是Windows，在开始菜单中搜索"cmd"进入终端。输入"nslookup google.com"，显示类似如下结果：（返回的IP地址可能不同，与电脑配置的DNS服务器有关）

```python
	
	  nslookup google.com

    Server:     10.10.0.215
    Address:    10.10.0.215#53

    Non-authoritative answer:
    Name:       google.com
    Address:    172.217.25.14
```

* 路由器的作用是对数据进行转发，类似物流公司根据目的地对包裹进行中转。

* 可以通过traceroute命令来观察数据的路径。如果你用Mac，在终端里面输入"traceroute google.com"; 如果你用Windows，在终端里面输入"tracert google.com"。



```python

    traceroute ucla.edu
    traceroute to ucla.edu (128.97.27.37), 64 hops max, 52 byte packets
    1  *
    2  172.172.172.1 (172.172.172.1)  4.035 ms
    3  100.64.1.1 (100.64.1.1)  4.793 ms
    4  172.16.4.177 (172.16.4.177)  6.179 ms
    5  172.29.5.15 (172.29.5.15)  32.837 ms
    6  10.16.16.2 (10.16.16.2)  33.144 ms
    7  10ge1-5.core1.hkg1.he.net (27.50.36.61)  35.638 ms
    8  100ge11-1.core1.lax2.he.net (184.105.64.125)  189.996 ms
    9  100ge2-2.core1.lax1.he.net (72.52.92.121)  188.386 ms
    10  198.32.251.85 (198.32.251.85)  311.201 ms
    11  dc-lax-agg8--lax-agg6-100ge-2.cenic.net (137.164.11.7)  192.113 ms
    12  *
    13  bd11f1.anderson--cr001.anderson.ucla.net (169.232.4.6)  193.419 ms
    14  cr00f1.anderson--sr02fb.jsei.ucla.net (169.232.8.53)  182.159 ms
    15  128.97.27.37 (128.97.27.37)  288.196 ms
```

##  作业 ##

完成作业：

1. 请查找自己计算机的IP地址，在本题下方放上屏幕截图。

2. 打开终端（Windows是cmd），用nslookup命令查找下列域名对应的IP地址，并在下方放上屏幕截图。
    •	UCLA大学官网：www.ucla.edu
    •	任意至少两个网站

3. 请用traceroute(Mac)或者tracert(Windows)命令来追踪从你的电脑到UCLA服务器的网络路径，放上屏幕截图并回答下列问题：
    a.	请描述路径经过的地理位置，以及传输所需要的时间
    b.	第一个路由器的ip地址是多少？你认为第一个路由器在哪里？
    c.	为什么UCLA的服务器不在LA？

4. IPV4和IPV6都是互联网协议，用于在网络上标识不同的设备。请查询资料，描述IPV4和IPV6的区别。描述中至少需要对比两种协议的地址长度，地址表示方式，可分配地址数量等方面的区别。

5. 【选做】第一题中，如果我们通过计算机的设置来查找IP，显示的IP地址通常是以192.168开头。但在百度中搜索IP，显示的结果又不一样。为什么会有这样的差异？

提交方式：Word文档，截止本周日晚10点。


