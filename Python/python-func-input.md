Python input() 函数
=================

 [![Python 内置函数](../images/up.gif)
 Python 内置函数](python-built-in-functions.html)


 Python3.x 中 input() 函数接受一个标准输入数据，返回为 string 类型。

 Python2.x 中 input() 相等于 eval(raw\_input(prompt)) ，用来获取控制台的输入。

 raw\_input() 将所有输入作为字符串看待，返回字符串类型。而 input() 在对待纯数字输入时具有自己的特性，它返回所输入的数字的类型（ int, float ）。

 
>  **注意：**input() 和 raw\_input() 这两个函数均能接收 字符串 ，但 raw\_input() 直接读取控制台的输入（任何类型的输入它都可以接收）。而对于 input() ，它希望能够读取一个合法的 python 表达式，即你输入字符串的时候必须使用引号将它括起来，否则它会引发一个 SyntaxError 。
> 
>  除非对 input() 有特别需要，否则一般情况下我们都是推荐使用 raw\_input() 来与用户交互。
> 
>  **注意：**python3 里 input() 默认接收到的是 str 类型。
> 
>  ### 函数语法

 
```

input([prompt])

```

  参数说明：

 * prompt: 提示信息
  ### 实例

  input() 需要输入 python 表达式
-----------------------

 <pre>

>>>a = input("input:")
input:123 # 输入整数
>>> type(a)
<type 'int'>               # 整型
>>> a = input("input:")
input:"runoob" # 正确，字符串表达式
>>> type(a)
<type 'str'>             # 字符串
>>> a = input("input:")
input:runoob # 报错，不是表达式
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<string>", line 1, in <module>
NameError: name 'runoob' is not defined
<type 'str'>
</pre>

  raw\_input() 将所有输入作为字符串看待
-------------------------

 <pre>

>>>a = raw_input("input:")
input:123
>>> type(a)
<type 'str'>              # 字符串
>>> a = raw_input("input:")
input:runoob
>>> type(a)
<type 'str'>              # 字符串
>>>
</pre>

 [![Python 内置函数](../images/up.gif)
 Python 内置函数](python-built-in-functions.html)

