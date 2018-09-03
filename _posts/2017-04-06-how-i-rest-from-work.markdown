---
layout: post
title: Python集合数据类型简洁总结-List、Tuple、Dict、Set
date: 2018-09-03 14:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: i-rest.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [python]
---
## Plaid ramps kitsch woke pork belly
使用python版本：python3.6

一、List

1）list的创建

字符串类型：L = [‘Tom’,'Bob','Tim','Tracy']

整数类型：L = [50,100,200,500]

不同种类型：L = ['Tom',20,'Bob',300,'Tim']

空list：L = []

2）list的访问

L =  [‘Tom’,'Bob','Tim','Tracy']

索引访问：print (L[0])

print (L[1])

print (L[2])

print (L[3])

**print (L[4]) 会出现越界错误**

倒序访问：print (L[-1])

print (L[-2])

print (L[-3])

print (L[-4])

**print (L[-5]) 会出现越界错误**

3）list的元素操作

L =  [‘Tom’,'Bob','Tim','Tracy']

元素增加：L.append('Baby')--使用append()将'Baby'追加到list的尾部

L.insert(0,'Baby')--使用insert将'Baby'添加到索引为0的位置

元素删除：L.pop()--使用pop()将list的最后一个元素删掉

L.pop(2)--使用pop()将list索引为2的元素删掉

元素替换：L[2] = 'YoYo'--直接将list索引为2的元素'Bob'替换成YoYo

L[-1] = ‘HuHu’--直接将list最后一个元素‘Tracy’替换成‘HuHu’

二、Tuple

1）tuple的创建

t = (‘Tom’,'Bob','Tim','Tracy')

**

对比list，

相同点：访问方式一样

不同点：tuple无法对元素操作、集合用（）表示

**

2）单元素tuple创建

t = (1,)

t = ('Bob',)

3）"可变"tuple创建

t = ('a','b',['A','B'])

三、Dict

d = {'Adam':95,'Lisa':85,'Bart':59}

1）dict的访问

print (d['Adam']) --95

print (d['Lisa']) --85

print (d['Bart']) --59

**如果访问的key不存在，会报错**

防止报错方法：

(一)

if 'Paull' in d:

print (d['Paul'] )

(二)

print (d.get('Bart')) --59

print (d.get('Paul')) --None

2）dict的特点

(一)查找速度快，占用内存大，key不可重复；

(二)key-value序对没有顺序，不同的机器打印的顺序可能不同，不能使用dict存储有序集合；

(三)key必须不可变，list不能作为dict的key

3）dict的更新

d['Paul'] =72 --直接将‘Paul’：72加入到了dict中

如果key已经存在，则赋值会用新的value的值替换掉原来的value

4）dict的遍历

d = {'Adam':95,'Lisa':85,'Bart':59}

for key in d:

print (key)

print (key + ':',d[key])

四、Set

创建set的方式是调用set（）并传入一个list，list的元素将作为set的元素

s = set(['A','B','C'])

无序打印，不能包含重复的元素

1）set的访问

set存储是无序集合，无法通过索引访问

s = set(['Adam', 'Lisa', 'Bart', 'Paul'])

‘Bart’ in s

2）set的特点

不存储value，存储对象不可变化，set存储元素是无序的

3）set的更新

添加元素时，用set的add()方法：

>>> s = set([1, 2, 3])

>>> s.add(4)

>>> print (s)

set([1, 2, 3, 4])

如果添加的元素已经存在于set中，add()不会报错，但是不会加进去了：

>>> s = set([1, 2, 3])

>>> s.add(3)

>>> print (s)

set([1, 2, 3])

删除set中的元素时，用set的remove()方法：

>>> s = set([1, 2, 3, 4])

>>> s.remove(4)

>>> print (s)

set([1, 2, 3])

如果删除的元素不存在set中，remove()会报错：

>>> s = set([1, 2, 3])

>>> s.remove(4)

Traceback (most recent call last):

  File "", line 1, in

KeyError: 4

所以用add()可以直接添加，而remove()前需要判断。

4）set的遍历

s = set(['Adam', 'Lisa', 'Bart'])

for name in s:

print (name)
![I and My friends]({{site.baseurl}}/assets/img/we-in-rest.jpg)


