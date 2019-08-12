---
layout: post
title: design mode
date: 2018-10-20
author: deng liuyan
header-img: "img/design_mode.jpg"
catalog: true
published: True
tags:
    - Skill
    - Experience
---

最近学习了下设计模式，收获颇多，好像有了诀窍去写高端大气上档次代码一样。所谓设计模式，大概就是有一个功能你在纠结如何布局时，应该静下心来思考的事情，再大一点，扩展到项目，亦是如此。

先简单上一个图。

![design_mode](/img/In_post/design_mode.png)

##### 工厂模式

写点简单的代码来理解下，可看代码中的注释帮助理解。

个人对这个模式理解是，一个工厂里有各种对象产品，产品功能大致相同，但是功能表现不一致。

```python
class nameA:
  def gender():
    return 'male'
class nameB:
  def gender():
    return 'female'
  
#工厂方法,后续需新增class，即可添加在此方法中。无需改变下面的流程代码。
def name_factory(name):
  if name == 'nameA':
    	return nameA()
  else if name == 'nameB':
    return nameB()
  
#流程与class解耦
ttA = name_factory('nameA')
ttB = name_factory('nameB') 
```

##### 构造模式

这个模式针对一些复杂功能构造代码，就好比一台电脑有很多配置一样。

##### 单例模式

核心是一个class只有一个实例，每次创建实例时，如果已经创建过，将使用之前的实例，改写创建实例的__new__函数。

```python
class singleMd:
  def __new__(cls,*args,**kwargs):
    if not hasattr(cls,'_instance'):
      _instance = super().__new__(cls,*args,**kwargs)
      cls._instance = _instance
    return cls._instance

@singleMd
class test:
  pass

c1 = test()
c2 = test()
#is比较时，要求内存一致，而等于只要求值一致。
asset c1 is c2
```
##### 装饰器模式

装饰器有很多介绍，在此不赘述了。

##### 适配器模式

增加一个class，可以通过统一的接口调用不同实例里的不同方法。

```python
class adapter:
  def __init__(self,obj,**adapter_functions):
    self.obj = obj
    self.__dict__.update(adapter_functions)
  def __getattr__(self,attr):
    return getattr(self.obj,attr)
```

##### 迭代模式

迭代模式可以改写或者新加__iter__ 方法。





