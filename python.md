# Python



## 数据类型

### 基础数据类型

#### int类型

定义一个整型，并不一定非要使用int声明

```python
# int
#定义一个整型，并不一定非要使用int声明

count_100_01 = int(100)
count_100_02 = 100    # 自带int
```

#### float类型

```python
# float
#同上

pi_01 = float(3.14)
pi_02 = 3.14
```

#### type 内置函数

```python
# 返回变量的类型   type(已经被赋值的变量名或变量)

count = 1050
print(type(count))
print(type(3.1457))
```

#### boolean类型

```python
# 布尔类型 true false
# bool 代表布尔类型 也可以对于结果进行真假的判断

res = bool('name' in 'my name is xiaomu')

print(res) #true
# int 0 -> false ,非0 -> true 浮点数相同 0.0=false
# str '' -> false,非空字符串->True
```

#### None类型

```python
# 不属于任何数据类型 就是 空类型
# 固定值 : None
# 空类型 属于 False 的范畴
# 如果不确定类型的时候，可以使用空类型
test = None
print(type(test))
print(test) 

test = 1
print(type(test))
print(bool(test))
```

#### Dict类型

```python
# dict
# 字典是由多个键（key）以及对应的值（value）所组成的一种数据类型
# 通过{}将一个个 key 与 value 存入字典中

a = dict()
b = {}

person = {'name': 'dewei', 'age': 23}

# key支持字符串，数字和元组类型，但列表不支持
# value支持所有python的数据类型

a = {'name': 'dewei', 'age': 23}
b = {1: 'one', 2: 'two', 3: 'three'}
c = {(1,2,3): [1,2,3], (4,5,6): [4,5,6]}

# 列表与元组中的字典
dict_array = [{1:1,2:2},{'one':1,'two':2}]
dict_tuple = ({1:1,2:2},{'one':1,'two':2})

# python3.7与之前字典的区别
#有序
# 字典中每一个key一定是唯一的

user_info = {'name': 'dewei', 'age': 10}

result = 'name' in user_info

print(result) # true
print(len(user_info)) # 2

empty_dict = {}
print(bool(empty_dict)) #false
print(type(empty_dict)) #<class 'dict'>

print(max(user_info)) # 返回name
print(min(user_info)) # 返回age
```

#### list类型

```python
# list
# 列表就是队列，各种数据的集合，是一种数据结构
# list代表这种类型，可以用于定义一个列表
# 列表中的元素存在一个[]中 , 是一个无限制长度的数据结构

name_01 = list(['dewei','xiao','deiwei'])
name_02 = ['dewei','xiao','deiwei']
print(type(name_01))

# 列表中的类型
str_array = ['dewei','haha',',']
int_array = [1,2,3,0,10,110]
float_array = [1.1,2.2,0.0,4.4,5.5]
bool_array = [True,False,True,False]



none_array = [None,None,None]
print(none_array)
print(bool(none_array)) # true 因为none_array=3,不为0因此不为false
print([])
print(bool([]))


list_array = [[1,2,3],[1.2,3.1]]
mix_array = ['dewei',1,3.14,None,True]

# in max min 在列表中的使用

res_1 = 1 in [1,2,3,4] #true
res_2 = 1 in [2,3,4] #false

# 不同类型不能相互比较
max([1,2,3,4]) #->4
min([1,2,3,4]) #->1
```

#### String类型

```python
#  ''  "" 包裹的信息就是字符串
# str来代表字符串类型 并且可以通过该函数定义字符串

safe = str('健康的体温是36.5')
name = '小木'

type(name)

# 字符串不可改变！！！！

# 内置函数id  返回变量的内存地址
# 数字地址 = id(变量)

name = 'dewei'
print(id(name))

name = 'xiaomi'

print(id(name))
# 2121134593008
# 2121136279664

# 内置函数len
# 返回字符串的长度，无法返回数字类型的长度，数字类型没有长度
# 返回值 = len(字符串)

i=len('1010101')
print(i)

# 内置成员运算符in   not in 反向判断
# 用来判断你的数据是否成为你想要的成员
# 'x' in 'xxxxxx' 判断x是否在xxxxx中

res1 = '1' in '34455'
print(res1) #false
res2 = '1' not in '34455'
print(res2) #true

# max函数返回数据中最大的成员
#中文字符 > 字母 > 数字 > 英文符号

# min函数返回数据的最小成员

#字符串的累加
#字符串的拼接，用"+"这个符号
a = '123'
b = '456'
c = a + b
print(c)

a = b+c #内存地址改变
```

#### tuple类型

```python
# tuple
# 元组和列表一样，都是一种可以存储多种数据结构的队列
# 元组也是一个有序的，且元素可以重复的集合
# tuple代表着元组这种类型，也可以用它定义一个元组
# 元组中的元素存在与一个()小括号中 无限制数据结构

name_01 = tuple(('dewei','小慕'))
name_02 = ('dewei','小慕')
name_03 = ('dewei',) #单个元素的时候，必须+,  不然编译器不认为是个元组 括号中是什么类型就是什么类型 (1) -> int
tuple_01 = () # type(tuple_01) -> tuple类型

print(bool()) # false

# 区别
# 元组比列表占用资源更小
# 列表是可变的，元组是不可变的 列表定义后可以添加数据，元组不行

# 元组中的类型
str_tuple = ('dewei','haha',',')
int_tuple = (1,2,3,0,10,110)
float_tuple = (1.1,2.2,0.0,4.4,5.5)
bool_tuple = (True,False,True,False)
none_tuple = (None,None,None,None)
tuple_tuple = ((1,2,3),(1.2,3.1))
list_tuple = ([123,456],[6789,1234]) # 列表元组，其中的列表无法修改
mix_tuple = ('dewei',1,3,14,None,True)

# in max min 在元组中的使用

res_1 = 1 in (1,2,3,4)  #true
res_2 = 10 in (1,2,3,4)  #false

max((1,2,3,4))
min((1,2,3,4))

# max和min在元组中使用的时候，元组中得元素不能是多种类型
```

#### number_count方法

```python
# 赋值运算符
# = 等于运算符  c = a+b
# += 加法运算符 c += a  c = c+a
# -= 减法运算符 c -= a  c = c-a
# *= 乘法运算符 c *= a  c = c*a
# /= 除法运算符 c /= a  c = c/a
# %= 取模运算符 c %= a  c = c%a
# **= 幂运算 c **= a  c = c**a
# //= 整除运算符 c //= a  c = c//a

a = 2
b = 10
c = 38

print(a**b)

# b kb mb gb 的转换

# 字符串与数字的乘法
# 字符串无法与字符串做乘法，字符串只可以和数字作乘法
name = 'xiaomu'
print(name*3)  #xiaomuxiaomuxiaomu

list_01 = [1,2,3]
print(list_01*2)  #[1,2,3,1,2,3]

tuple_01 = (1,2,3)
print(tuple_01*2)  #(1,2,3,1,2,3)

# dict字典不支持

# 比较运算符
# ==    判断是否等于
# !=    判断是否不等于
# >     判断是否大于
# <     判断是否小于
# >=    判断是否大于等于
# <=    判断是否小于等于
# is    判断两个对象存储单元是否相同  a is b
# is not    判断两个对象存储单元是否不同  a is not b
```



## 数据类型方法

### Dict方法



## 类

#### 定义

##### 类的关键字

  + class声明一个类，类的名称首字母大写，多单词情况下每个单词首字母大写

```python
# class Name(object):
#     attr = something
#     def func(self):
#         do
class Person(object):
    name = '小慕'
    def dump(self):
        print(f'{self.name}')

xiaomu = Person()   # 类的实例化
print(xiaomu.name)  # 调用属性
xiaomu.dump()       # 调用函数
```

##### 类的参数self
  + self是类函数中必传参数，且必须放在第一个参数位置
  + self是一个对象，他代表实例化的变量自身
  + self中的变量与含有self参数的函数可以在类中任意一个函数内随意调用

```python
class Person1(object):

    def __init__(self, name,age=None):
        self.name = name
        self.age = age

    def run(self):
        print(f'{self.name} 在奔跑')

    def jump(self):
        print(f'{self.name} 在跳跃')

    def work(self):
        self.run()
        self.jump()
        xiaomu = Person1('小慕',32)
xiaomu.run()
xiaomu.jump()
# 每个实例化对象定义的不同
xiaomu.top = 174
print(xiaomu.top)
xiaomu.work()
```

##### 构造函数的创建

```python
# def _init_(self,a,b):
#     self.a = a
#     self.b = b

# 对象的生命周期
```

##### 私有函数和私有变量

```python
# 无法被实例化后的对象调用的类中的函数与变量
# 类内部可以调用私有函数与变量
# 只希望类内部业务调用使用，不希望被使用者调用

# 在变量或函数前添加__(两个下横线)，变量或函数名后变无需添加
class Cat(object):
    def __init__(self, name):
        self.name = name

    def run(self):
        result = self.__run()
        print(result)# 占位符
    def __run(self):
        return f'小猫{self.name} 开心的奔跑着'
    def jump(self):
        result = self.__jump()
        print(result)
    def __jump(self):
        return f'小猫{self.name} 开心的跳着'

cat = Cat(name='米粒儿')
cat.run()
cat.jump()
```

#### 装饰器

##### 定义
+ 也是一种函数
+ 可以接收函数作为参数,可以返回函数
+ 接收一个函数，内部对其处理，然后返回一个新函数，动态的增强函数功能
+ 将c函数在a函数中执行，在a函数中可以选择执行或不执行c函数，也可以对c函数的结果进行二次加工处理

 ```python
 def out(func_args):     外围函数
    def inter(*args,**kwargs):      内嵌函数
        return func_argc(*args,**kwargs)
    return inter        外为函数返回内嵌函数
 ```

##### 装饰器用法

+ 将被调用的函数直接作为参数传入装饰器的外围函数括弧
+ 将装饰器与被调用函数绑定在一起
+ @符号+装饰器函数放在被调用函数的上一行，被调用的函数正常定义，只需要直接调用被执行函数即可

```python
def check_str(func):
    print('func:',func)
    def inner(*args, **kwargs):
        print('args:',args,kwargs)
        result = func(*args, **kwargs)
        if result == 'ok':
            return 'result is %s' % result
        else:
            return 'result is failed:%s' % result
    return inner

@check_str
def test(data):
    return data

result = test('no')
print(result)
```

##### classmethod功能 and staticmethod的功能

```python
# 将类函数可以不经过实例化而直接被调用
# 用法:
#   @classmethod
#   def func(cls,...):
#       do
# 参数介绍: cls替代普通类函数中的self，变为cls，代表当前操作的是类

class Test(object):
    def __init__(self,a):
        self.a=a

    def run(self):
        print('run')
    @classmethod
    def dump(cls):
        print('dump')
        # cls.run()  # 不能调用
    @staticmethod
    def sleep():
        print('i want sleep')
t = Test('a')
t.run()
Test.dump()
Test.sleep()
t.sleep()
t.dump()

# staticmethod的功能
# 该类函数可以不经过实例化而直接被调用，，被该装饰器调用的函数不许传递self或cls参数，且无法再该函数内调用其他类函数或类变量
```

##### property 功能

+ 把函数当作变量
+ 将类函数的执行免区括弧，类似与调用属性(变量)

```python
# @property
# def func(self)
#   do

class Test1(object):
    def __init__(self,name):
        self.__name=name

    @property
    def name(self):
        return self.__name
    @name.setter
    def name(self,value):
        self.__name=value
t1 = Test1(name='dewei')
print(t1.name)
t1.name='小慕'
print(t1.name)
```

#### 继承

##### 定义

+ 通过继承基类来得到基类的功能
+ 所以我们把被继承的类称作父类，继承者为子类
+ 子类拥有父类的所有属性和方法
+ 父类不具备子类自有的属性和方法

~~~python
class Parent(object):
    def talk(self):
        print('talk')
    def think(self):
        print('think')
class Child(Parent):
    def swimming(self):
        print('child can swimming')
# 定义子类时，将父类传入子类参数内
# 子类实例化可以调用自己与父类的函数与变量
# 父类无法调用子类的函数与变量

~~~

##### super函数的作用

+ 子类继承父类的方法而使用的关键字，当子类继承父类后，就可以使用父类的方法

  ```python
  class Parent(object):
      def __init__(self):
          print('hello i am parent')
  class Child(Parent):
      def __init__(self):
          print('hello i am child')
          super(Child,self).__init__  #改写后使用Parent类的函数
      
  ```

##### 多重继承

+ 可以继承多个父类

  ```python
  class Child(Parent1,Parent2,Parent3)
  # 将被继承的类放入子类的参数位中，用逗号隔开
  # 从左向右一次继承
  ```

  

#### 多态

+ 子类中重写父类的方法

```python
# 1 书写一个父类
class Parent(object):
    def talk(self):
        print('小慕的爸爸说了一句话')
# 2 书写一个子类，并继承一个父类
class XiaomuBrother(Parent):
    def run(self):
        print('小慕哥哥在奔跑着....')
    def talk(self):
        print('小慕哥哥在说话')

if __name__ == '__main__':
    xiaomu_brother = XiaomuBrother()
    xiaomu_brother.run()
    father = Parent()
    father.talk()
    xiaomu_brother.talk()
```

#### 类的高级函数

```python
#_str_的功能
#如果定义了该函数，当print当前实例化对象的时候，会返回该函数的return信息
#用法:
	def _str_(self):
        return str_type
# 返回值: 返回对于该类的描述信息
class Test(object):
    def _str_(self):
        return '这是关于这个类的描述'
test = Test()
print(test)

#_getattr_的功能
#当调用的属性或者方法不存在时，会返回该方法定义的信息
#用法:
	def _getattr_(self):
        print(something...)
#参数:
#	key:调用任意不存在的属性名
#	返回值: 可以任意类型也可以不返回

#__setattr_的功能
#拦截当前类中不存在的属性与值
#用法:
	def _setattr_(self):
        self._dict_[key] = value
#参数:
#	key:当前属性名
#	value:当前的参数对应的值
#	返回值: 无



# _call_的功能
# 本质是将一个类变成一个函数
#用法:
	def _call_(self，*args，**kwargs):
        print(something...)
#参数: 可传任何参数
#返回值: 与函数情况相同可有可无



```



#### 异常与异常处理

+ 异常就是错误，会导致程序崩溃并停止运行
+ 能监控并捕获到异常，将异常部位的程序进行修理使得程序继续正常进行

```python
try:
    <代码块1> 被try关键字检查并保护的业务代码
except <异常的类型>:
    <代码块2> 代码块1出现错误后执行的代码块
    
def upper(str_data):
    new_str_data = ''
    try:
        new_str_data = str_data.upper()
    except:
        print('不是字符串类型')
    return new_str_data

result = upper('dewei')
print(result)

result = upper(1)
print(result)
```

##### 捕获通用异常

+ 无法确定时那种异常情况下使用的捕获方法

  ```python
  try:
      <代码块>
  except Exception as e:
      <异常代码块>
  ```

+ 确定是那种异常的情况下使用的捕获方法

  ```python
  except Exception as e:<异常代码块> 
  def test():
      try:
  		1/0
          print('hello')
      except ZeroDivisionError as e:
          print(e)
  test()
  ```

+ 捕获多个异常

  ```python
  #多个except
  try:
      <代码块>
  except (ZeroDivisionError,Exception) as e:
      <异常代码块>
  ```

  

##### 异常类型

```python
Exception			通用异常类型(基类)
ZeroDivisionError	不能整除0
AttributeError		对象没有这个属性
IOError				输入输出操作失败
IndexError			没有当前的索引
KeyError			没有这个键值（key）
NameError			没有这个变量（未初始化对象）
SyntaxError			Python语法错误
SystemError			解释器的系统错误
ValueError			传入的参数错误
```

##### finally的功能

+ 无论是否发送异常，一定会执行的代码块

+ 在函数中，即便在try或except中进行了return也依然会执行finally语法块

+ try语法至少要伴随except或finally中的一个

  ```python
  try:
      <代码块1>
  except:
      <代码块2>
  finally:
      <代码块3>
  ```

##### 自定义异常与抛出异常

+ 自定义抛出异常函数-raise
+ 将信息以报错的形式抛出

 ```python
 # 用法:
 #	raise 异常类型(message)
 #	message: 错误信息
 def test(number):
     if number == 100
     	raise ValueError('number 不可以是100')
     return number
 
 result = test(50)
 print(result)
 # result = test(100)
 
 def test2(number):
     try:
         return test(number)
     except ValueError as e:
         return e
 result = test2(100)
 print(result)
 ```

+ 自定义异常类型   继承基类 — Exception

+ 在构造函数中定义错误信息

  ```python
  class NumberLimitError(Exception):
      def __init__(self,message):
          self.message = message
          
  class NameLimitError(Exception):
      def __init__(self,message):
  		self.message = message
  def test5(name)
  	if name == 'dewei':
  		raise NameLimitError('deiwei不可以填写')
      return name
  def test6(number)
  	if number > 100:
          raise NumberLimitError('数字不可以大于100')
      return number
  
  try:
      test5('dewei')
  except NameLimitError as e:
      print(e)
  
  try:
      test6(100)
  except NumberLimitError as e:
      print(e)
  ```

#### 断言的功能 assert

+ 用于判断一个表达式，在表达式条件为false的时候触发异常

```python
# 用法:
# 	assert expression,message
# 参数:
#	expression: 表达式，一般是判断相等，或者判断某种数据类型的bool判断的语句
#	message: 具体的错误信息
```

### 包与模块

#### 包

+ 包就是文件夹，包中还可以有包，也就是子文件夹
+ 一个个python文件就是模块

##### 包的身份证

+ _ init _.py 是每一个python包里必须存在的文件

##### 如何创建一个包

+ 要有一个主题，明确功能，方便使用
+ 层次分明，调用清晰

##### 包的导入import

+ 将python中的某个包（或模块），导入到当前的py文件中

  ```python
  # 用法:
  	import package
  # 参数:
  	package: 被导入包的名字
  # 要求:
  	只会拿到对应包下__init__中的功能或当前模块下的功能
  ```

  

 ##### 模块的导入 from... import..

+ 通过某个包中找到对应的模块

  ```python
  # 用法:
  	from package import module
  # 参数:
  	package: 来源的包名
      module: 包中的目的模块
  # 要求:
  	只会拿到对应包下__init__中的功能或当前模块下的功能
      
  from animal import
  dog.run()
  ```

#### 第三方包

+ 第三包是其他写好功能封装成包
+ 利用pip与easy_install获取第三方包
+ pip install 包名

+ 第一个三方包  -ipython
  + ipython是一个python的交互式shell，比默认python shell好用，支持变量自动补全，自动缩进

##### datetime包

+ 日期与时间的集合体 date and time

+ 获取当前时间

+ 获取时间间隔

+ 将时间对象转成时间字符串

+ 将字符串转成时间类型

  ```python
  
  #导入包
  from datetime import datetime
  import datetime
  
  #获取当前时间使用方法
  datetime.now()
  datetime.datetime.now()
  
  #获取时间间隔
  from datetime import datetime
  from datetime import timedelta
  # 使用
  timeobj = timedelta(days=0,seconds=0,microseconds=0,milliseconds=0,minutes=0,hours=0,week=0)
  
  now = datetime.now()
  print(now)
  
  # 获取三天以后
  three_days = timedelta(days=3)
  
  after_three_days = now+three_days
  print(after_three_days)
  ```

##### 时间对象转字符串

  ```python
  from datetime import datetime
  date = datetime.now()
  str_date = date.strftime('%Y-%m-%d %H:%M:%S')
  ```

  ##### 时间字符串转时间

```python
#获取时间模块:
	from datetime import datetime
#时间字符串转时间类型
	datetime.strptime(tt,format)
#参数介绍:
		tt: 符合时间格式的字符串
    	format: tt时间字符串匹配规则
str_date = '2021-10-10 13:12:13'
date_obj = datetime.strptime(str_date, '%Y-%m-%d %H:%M:%S')
print(date_obj)
```

##### Python中Time模块

+ 时间戳 （timestamp）1970年1月1日00时00秒至今的总毫秒数

+ float

+ 暂停函数sleep

  ```python
  # 导入包:
  	import time
  # 使用方法:
  	time.sleep(second) 
  # 参数介绍:
  	second: 希望程序被暂停的秒数
  for i in range(10):
      print(i)
      time.sleep(1)
  ```

  

+ time函数

  + 时间处理，转换时间格式

  + 生成时间戳函数time

  + 获取本地时间函数localtime

  + localtime对应字段介绍

  + 暂停函数sleep

  + time中的strftime与strptime

    ```python
    # 导入包:
    	import time
    # 使用方法:
    	time.time() #当前的时间戳
    # 返回值:
    	秒级别的浮点类型
        
    # 获取本地时间函数localtime
    	t = time.localtime(obj)  #可传入参数，也可以不传（当前时间）
    
    # time中的strftime
    # 使用方法:
    	time.strftime(format,t)
    # 参数介绍:
    	format: 格式化规范
        t: time.localtime对应的时间类型
        str_time = time.strftime('%Y-%m-%d %H:%M:%S',time.localtime())
        
    # time中的strptime
    # 使用方法:
    	time.strptime(time.str,format)
    # 参数介绍:
    	time_str: 符合时间格式的字符串 
        format: 确保与time_str一致的格式化标准
        
    time_obj = time.strptime('2020-12-12','%Y-%m-%d')
    
    #datetime中生成时间戳函数
    # 使用方法:
    	now = datetime.datetime.now()
        datetime.datetime.timestamp(now)
    # 参数介绍:
    	now: datetime 时间对象
        
    # datetime时间戳转时间对象
    # 使用方法:
    	datetime.datetime.fromtimestamp(timestamp)
    # 参数介绍
    	timestamp: 时间戳
    ```

##### OS包

+ os的文件与目录函数介绍

+ ![image-20240825154118502](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825154118502.png)

+ ![image-20240825154043807](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825154043807.png)

  ```python
  import os
  
  current_path = os.getcwd()
  print(current_path)
  
  new_path = '%s/test1' % current_path
  os.makedirs(new_path)
  
  data = os.listdir(current_path)
  print(data)
  
  ```

  + os.path模块常用方法

    ![image-20240825154701356](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825154701356.png)

    ![image-20240825154615649](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825154615649.png)

### 文件



### 常用函数和高阶函数

#### Python中的加密工具

##### hashlib包介绍

+ 难破解 不可逆

  ![image-20240825163047920](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825163047920.png)

 ```python
 import hashlib
 import time
 
 base_sign = 'muke'
 a_timestamp = int(time.time())
 _token = '%s%s' % (base_sign,a_timestamp)
 hashobj = hashlib.sha1(_token.encode('utf-8'))
 a_token = hashobj.hexdigest()
 print(a_token)
 ```

##### base64包

![image-20240825163732830](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825163732830.png)

   ```python
   def encode(data):
       if isinstance(data, str):
           data = data.encode('utf-8')
       elif isinstance(data, bytes):
           data =data
       else:
           raise TypeError('data must be str or bytes')
   
       return base64.encodestring(data).decode('utf-8')
   
   if __name__ == '__main__':
       result = encode('hello world')
       print(result)
   ```

#### 日志模块

+ 日志的等级：debug info warnning error crtical

+ ![image-20240825213740916](C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825213740916.png)

  <img src="C:\Users\cycy\AppData\Roaming\Typora\typora-user-images\image-20240825213955732.png" alt="image-20240825213955732" style="zoom: 80%;" />

```python
format='%(asctime)s %(filename)s[line:%(lineno)d] %(levelname)s %(message)s'

logging.info('_______')
import logging

logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s %(filename)s[line:%(lineno)d] %(levelname)s %(message)s',
    filename='bage.log',
    filemode='w',
)

```

