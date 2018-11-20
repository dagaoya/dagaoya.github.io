---
layout: post
title: Python笔记
category: others
---
记录学习，记录容易忘的知识点

---

### 内置函数

'''
ord() #返回字符对应的 ASCII 数值
chr() #返回数字对应的 ASCII 码
round(arg,3) #四舍五入保留3位
range(0,100,1) #从零到100，步长1（除了100都能省略）
print(,end="") #默认输出结尾换行，使用end=可以设置结尾字符，前面加\r可以回退到行首（重写本行)
lambda #匿名函数，需要一个函数的时候，如果函数较短，不需要重新定义，就用lambda 参数/可以多个 :返回值
'''

---

### 组合数据类型（集合、序列、字典）

#### 集合
set() #定义集合，可以使用序列作为参数，转为字典


#### 序列

1.元组


2.列表
list() # 把字典、转成列表
list.sort(key=lambda x:x[1], reverse=True) #以第二列为关键字排序，reverse=True是倒序，默认正序

#### 字典
dict={} # 定义空字典，虽然集合也是使用{}，但是空集合只能使用set()
dict.items() #以列表返回可遍历的(键, 值) 元组数组，但不是标准列表，不能使用列表函数，需要使用list()转换
dict['key'] = "value" # 有键就更新值，没有就添加
dict.get(key,default_value) #返回key对应的value，没有的话就返回default_value



---

### 运算符

'''
% #取余
// #取整除
** #次方，等于pow()
* #数字之间使用是乘法，字符使用就是重复n个该字符


'''

---

### 字符串内置函数

'''
str.center('*',10) #以str为中心，两侧填充*符号，总长度为10
"{0:->20.2f}".format(a) #{}占位，里面参数有冒号前是索引（0）或关键字，冒号后依次是 填充（-）、对齐（>）、宽度（20)、精度（.2）、类型（f），a是变量，可以是各种（列表、元组都行）
str.split() # 使用参数（默认空）分割字符串，返回分割后的列表
'''


---
### 标准库

#### turtle画图库

'''

import turtle
turtle.setup(650, 350, 200, 200)
turtle.penup()
turtle.fd(-250)
turtle.pendown()
turtle.pensize(25)
turtle.pencolor("purple")
turtle.seth(-40)
for i in range(4):
    turtle.circle(40, 80)
    turtle.circle(-40, 80)
    print(i)
turtle.circle(40, 80/2)
turtle.fd(40)
turtle.circle(16, 180)
turtle.fd(40 * 2/3)
turtle.done()

'''

#### time时间库

'''

import time

time.perf_counter() #取精确时间，取多次相减，可以求耗时
time.sleep(0.1) #休眠0.1秒
time.time() #取现行时间戳
time.gmtime() #取现行结构化时间,参数为时间戳的话则转换时间戳为结构化时间
time.localtime() #取现行结构化时间,参数为时间戳的话则转换时间戳为结构化时间
time.strftime('%Y-%m-%d %H:%M:%S') #常用输出格式： 2018-11-16 23:53:38
time.strptime('2018-11-16 23:53:38','%Y-%m-%d %H:%M:%S') #把字符串时间转换成结构化时间，与strftime()反过来
time.mktime() #把结构化时间转换成时间戳
    %Y  完整的年份
    %m  月份(01-12)
    %d  一个月中的第几天(01-31)
    %H  一天中的第几个小时(24小时制，00-23)
    %M  分钟数(00-59)
    %S  秒(01-61)
    %z  用+HHMM或者-HHMM表示距离格林威治的时区偏移(H代表十进制的小时数，M代表十进制的分钟数)
    %a  本地(local)简化星期名称
    %A  本地简化月份名称
    %B  本地完整月份名称
    %c  本地相应的日期和时间表示
    %I  一天中的第几个小时(12小时制，01-12)
    %p  本地am或者pm的相应符


'''


---
### 第三方库
#### pyinstaller
'''
#打包成exe
'''

#### jieba 
'''
#中文分词

jieba.lcut(txt) #常用就这一条，直接返回列表
'''

#### 