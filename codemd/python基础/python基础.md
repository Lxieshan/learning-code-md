



[TOC]





# 一 、Python简介

## 1.1 特性

​											完全面向对象

​											标准库丰富

​											三方接口丰富			

## 1.2 优点

​											开源 

​											面向对象

​											库多

​											可扩展

## 1.3 缺点 

​											运行速度慢





##  1.4  数据类型总结

| 数据类型 |                     优点                      |                缺点                 | 修改与否 |                使用场景                |
| :------: | :-------------------------------------------: | :---------------------------------: | :------: | :------------------------------------: |
|   str    |      文本处理功能强大，<br/>内置方法丰富      |   不可变性<br/>频繁拷贝，影响性能   | 不可修改 |      文本处理、格式化、字符匹配等      |
|   list   |    常用数据结构，可变，<br/>支持增删改操作    | 查找操作效率<br/>时间复杂度为 O(n)  |  可修改  |   存储有序元素、频繁修改的数据集合等   |
|  tuple   | 元素不可更改，<br/>适用于字典的键和集合的元素 | 需要修改时<br/>创建新元组，影响性能 | 不可修改 |   字典键、集合元素、函数返回多个值等   |
|   set    |    元素唯一性，<br/>自动去重，支持集合运算    |   无序，<br/>不能通过下标索引访问   |  可修改  | 去重数据、集合运算、判断元素是否存在等 |
|   dict   |    键值对存储，<br/>快速查找，支持增删改查    | 内存占用较大，<br/>查找速度可能较慢 |  可修改  |  存储键值对信息、数据映射、缓存数据等  |

| 数据类型 | 优点                                                         | 缺点                                                         | 修改 |                       使用场景                       |
| :------: | :----------------------------------------------------------- | :----------------------------------------------------------- | :--: | :--------------------------------------------------: |
|   int    | - 整数运算效率高，适用于整数的加减乘除等数值计算。<br>- 精度无限制，可表示任意大小的整数。<br/>- 内置函数丰富，支持各种进制表示。 | - 不能表示无理数和小数，只能表示整数。  - 在某些情况下可能会导致溢出。<br>- 不适用于需要高精度计算的场景。 |  是  |      用于表示整数值，<br/>如计数、索引等场景。       |
|  float   | - 可以表示小数和科学计数法，适用于实数的计算。<br>- 可以表示很大或很小的数值，支持无限大和无限小。 | - 浮点数运算有误差，可能出现精度问题。   - 不适用于要求高精度计算的场景。 |  是  |     用于表示实数值，<br>如浮点数运算、科学计算。     |
|   bool   | - 占用内存小，只有True和False两个值，节省存储空间。<br>- 支持逻辑运算，便于表达条件判断。<br>- 用于控制程序流程，进行条件判断。 | - 仅表示两种状态，<br/>  不适用于需要多个状态的场景<br/>- 不能直接进行数值计算。<br>- 只适用于表示逻辑值的场景。 |  否  | 用于表示布尔值，如判断条件是否成立、开关状态等场景。 |
| complex  | - 可以表示复数，方便进行复数运算。<br>- 支持复数的实部和虚部表示，用于数学和科学计算。 | - 复数运算涉及实部和虚部的计算，  <br/>  性能相对较低。<br>- 不适用于不涉及复数运算的场景。 |  是  |       表示复数值，<br/>如复数运算、信号处理。        |

## 1.5 Python 报错和异常

### 1.5.1 异常分类

当然，请见以下表格，它按照异常类型对常见的Python异常进行了总结：

|       异常类型        |              描述              |                             示例                             |
| :-------------------: | :----------------------------: | :----------------------------------------------------------: |
|  语法错误和命名错误   |                                |                                                              |
|     `SyntaxError`     |           语法错误。           |                     `print("Hello World`                     |
|  `IndentationError`   |           缩进错误。           |                `if True:\nprint("Indented")`                 |
|      `NameError`      |     未定义的变量或函数名。     |                     `x = undefined_var`                      |
|   类型错误和值错误    |                                |                                                              |
|      `TypeError`      |         对象类型错误。         |                          `len(123)`                          |
|     `ValueError`      |            值错误。            |                         `int("abc")`                         |
|     容器相关错误      |                                |                                                              |
|      `KeyError`       |       字典中的键不存在。       | `my_dict = {"key": "value"}\nvalue = my_dict["nonexistent_key"]` |
|     `IndexError`      |  列表或字符串的索引超出范围。  |          `my_list = [1, 2, 3]\nitem = my_list[10]`           |
|     文件和I/O错误     |                                |                                                              |
|  `FileNotFoundError`  |          文件不存在。          |          `with open("nonexistent.txt", "r") as f:`           |
|       `OSError`       |    涉及操作系统问题的错误。    |             `os.remove("nonexistent_file.txt")`              |
|   `PermissionError`   |    尝试执行没有权限的操作。    |        `with open("/etc/sensitive_file", "w") as f:`         |
|    数值和断言错误     |                                |                                                              |
|  `ZeroDivisionError`  |            除以零。            |                       `result = 1 / 0`                       |
|   `AssertionError`    |         断言条件失败。         |                  `assert len(my_list) > 10`                  |
|   异常层次结构基类    |                                |                                                              |
|      `Exception`      |      所有内置异常的基类。      |        `try:\n  # some code\nexcept Exception as e:`         |
|     其他错误类型      |                                |                                                              |
|     `SystemError`     |     Python解释器内部错误。     |                                                              |
|    `RuntimeError`     |        程序状态不正确。        |                                                              |
| `NotImplementedError` |      功能未在子类中实现。      |                                                              |
|    `StopIteration`    |     没有更多的元素可迭代。     |                                                              |
|    `UnicodeError`     | 与Unicode编码/解码相关的错误。 |                                                              |
| `DeprecationWarning`  |      功能已被弃用的警告。      |                                                              |
|     `UserWarning`     |        用户定义的警告。        |                                                              |
|   `ResourceWarning`   | 表示资源可能未正确关闭的警告。 |                                                              |

|         异常名称          |                         描述                         |
| :-----------------------: | :--------------------------------------------------: |
|                           |                                                      |
|       BaseException       |                    所有异常的基类                    |
|        SystemExit         |                    解释器请求退出                    |
|     KeyboardInterrupt     |              用户中断执行(通常是输入^C)              |
|         Exception         |                    常规错误的基类                    |
|       StopIteration       |                  迭代器没有更多的值                  |
|       GeneratorExit       |        生成器 (generator) 发生异常来通知退出         |
|       StandardError       |               所有的内建标准异常的基类               |
|      ArithmeticError      |                所有数值计算错误的基类                |
|    FloatingPointError     |                     浮点计算错误                     |
|       OverflowError       |                 数值运算超出最大限制                 |
|     ZeroDivisionError     |             除(或取模)零 (所有数据类型)              |
|      AssertionError       |                     断言语句失败                     |
|      AttributeError       |                   对象没有这个属性                   |
|         EOFError          |              没有内建输入,到达 EOF 标记              |
|     EnvironmentError      |                  操作系统错误的基类                  |
|          IOError          |                  输入/输出操作失败                   |
|          OSError          |                     操作系统错误                     |
|       WindowsError        |                     系统调用失败                     |
|        ImportError        |                  导入模块/对象失败                   |
|        LookupError        |                  无效数据查询的基类                  |
|        IndexError         |               序列中没有此索引(index)                |
|         KeyError          |                   映射中没有这个键                   |
|        MemoryError        |      内存溢出错误(对于 Python 解释器不是致命的)      |
|         NameError         |             未声明/初始化对象 (没有属性)             |
|     UnboundLocalError     |                访问未初始化的本地变量                |
|      ReferenceError       | 弱引用 (Weak reference) 试图访问已经垃圾回收了的对象 |
|       RuntimeError        |                   一般的运行时错误                   |
|    NotImplementedError    |                    尚未实现的方法                    |
|        SyntaxError        |                   Python 语法错误                    |
|     IndentationError      |                       缩进错误                       |
|         TabError          |                    Tab 和空格混用                    |
|        SystemError        |                 一般的解释器系统错误                 |
|         TypeError         |                   对类型无效的操作                   |
|        ValueError         |                    传入无效的参数                    |
|       UnicodeError        |                  Unicode 相关的错误                  |
|    UnicodeDecodeError     |                 Unicode 解码时的错误                 |
|    UnicodeEncodeError     |                  Unicode 编码时错误                  |
|   UnicodeTranslateError   |                  Unicode 转换时错误                  |
|          Warning          |                      警告的基类                      |
|    DeprecationWarning     |                关于被弃用的特征的警告                |
|       FutureWarning       |            关于构造将来语义会有改变的警告            |
|      OverflowWarning      |        旧的关于自动提升为长整型 (long) 的警告        |
| PendingDeprecationWarning |               关于特性将会被废弃的警告               |
|      RuntimeWarning       |      可疑的运行时行为 (runtime behavior) 的警告      |
|       SyntaxWarning       |                   可疑的语法的警告                   |
|        UserWarning        |                  用户代码生成的警告                  |

### 1.5.2 异常语法

`try`, `except`, `finally`, 和 `raise` 是 Python 中用于异常处理的关键字和语句。以下是它们的作用和用法：

- `try`：用于包裹可能引发异常的代码块。如果在 `try` 块中的代码引发了异常，程序会跳转到相应的 `except` 块。通常，您可以在 `try` 块中放置可能出现问题的代码。
- `except`：用于捕获异常并提供处理代码。可以根据需要提供一个或多个 `except` 块，每个块可以捕获不同类型的异常。当发生匹配的异常时，对应的 `except` 块中的代码将被执行。
- `finally`：用于指定无论是否发生异常都必须执行的代码块。无论是否发生异常，`finally` 块中的代码都会被执行。通常用于资源释放或清理。
- `raise`：用于手动引发异常。您可以使用 `raise` 语句来显式地引发特定类型的异常，也可以传递异常信息。这在某些情况下是有用的，比如在自定义函数中检查条件并引发异常。

​		Python中的异常处理语法使用`try`和`except`来捕获和处理异常。基本的语法结构如下：

```python
try:
    # 代码块，可能会出现异常的部分
    # ...
except SomeExceptionType:
    # 处理特定类型的异常
    # ...
except AnotherExceptionType:
    # 处理另一种类型的异常
    # ...
except:
    # 处理其他未指定的异常
    # ...
else:
    # 如果没有异常发生，则执行这里的代码
    # ...
finally:
    # 无论是否发生异常，最终都会执行这里的代码
    # ...
```

以下是对上述语法的解释：

- `try` 块：包含可能会引发异常的代码。如果在这个块中出现了异常，程序会跳转到相应的`except`块。
- `except` 块：用于捕获特定类型的异常。您可以根据需要提供一个或多个`except`块。当发生对应类型的异常时，这些块中的代码会被执行。
- `else` 块（可选）：如果在`try`块中的代码没有引发异常，那么`else`块中的代码将被执行。
- `finally` 块（可选）：无论是否发生异常，`finally`块中的代码都将被执行。通常用于释放资源或清理工作。

以下是一个简单的例子，演示了如何使用异常处理语法：

```python
try:
    num = int(input("请输入一个数字："))
    result = 10 / num
    print("结果是:", result)
except ZeroDivisionError:
    print("除以零错误！")
except ValueError:
    print("请输入一个有效的数字！")
except Exception as e:
    print("发生了一个未知的异常:", e)
else:
    print("没有发生异常。")
finally:
    print("无论如何都会执行这里的代码。")
```



以下是一个使用这些关键字和语句的简单示例：

```python
def divide(x, y):
    try:
        result = x / y
    except ZeroDivisionError:
        print("除以零错误")
    else:
        print("结果是:", result)
    finally:
        print("无论如何都会执行这里的代码")

divide(10, 2)
divide(10, 0)

try:
    age = int(input("请输入您的年龄："))
    if age < 0:
        raise ValueError("年龄不能为负数")
except ValueError as ve:
    print("发生了 ValueError:", ve)
```

在第一个示例中，我们定义了一个 `divide` 函数，它尝试计算两个数字的除法。如果除数为零，将引发 `ZeroDivisionError` 异常。无论如何，`finally` 块中的代码都会执行。

在第二个示例中，我们演示了如何使用 `raise` 语句手动引发异常，并提供异常信息。当输入的年龄为负数时，将引发一个 `ValueError` 异常并打印出异常信息。



**开发者检测用**



`assert` 是 Python 中的一个关键字，用于在代码中进行断言，以确保条件为真。它通常用于调试和测试阶段，用于检查代码中的假设是否满足。如果断言的条件为假，Python 会引发一个 `AssertionError` 异常。

`assert` 的语法如下：

```python
assert condition, message
```

其中：
- `condition` 是一个布尔表达式，表示需要检查的条件。
- `message` 是一个可选的参数，用于在断言失败时显示错误消息。

示例：

```python
def divide(a, b):
    assert b != 0, "除数不能为零"
    return a / b

result = divide(10, 2)  # 正常情况，没有断言异常
print(result)

result = divide(10, 0)  # 引发 AssertionError，除数为零
```

在第一个示例中，调用 `divide(10, 2)` 不会触发断言异常，因为除数不为零。而在第二个示例中，调用 `divide(10, 0)` 会触发断言异常，因为除数为零，与断言条件 `b != 0` 不符。

需要注意的是，一般情况下，`assert` 不应该用于处理预期可能出现的错误，而应该用于检查开发者认为是绝对正确的假设。在生产环境中，可以通过关闭断言来禁用它们。





### 1.5.3 异常自定义 `通过raise触发`





在Python中，您可以通过创建自定义的异常类来处理特定的错误情况。自定义异常类通常继承自内置的 `Exception` 类或其子类。通过自定义异常，您可以在程序中引发和捕获特定类型的错误，以便更好地组织和处理代码逻辑。

**以下是创建自定义异常的一般步骤**：

1. 创建一个继承自 `Exception` 或其子类的新类。
2. 可以为新类添加额外的属性和方法，以便在处理异常时提供更多的信息和功能。
3. 在适当的情况下，使用 `raise` 语句引发自定义异常。



当您使用 `try`, `except`, `finally`, 和 `raise` 时，您可以创建一个自定义的异常函数。下面是一个示例，演示了如何使用这些关键字来处理自定义异常：

```python
class CustomError(Exception):
    """自定义异常类"""
    def __init__(self, message):
        super().__init__(message)
        self.error_code = 1001

def custom_function(value):
    try:
        if value < 0:
            raise CustomError("值不能为负数")
        result = 10 / value
    except CustomError as e:
        print(f"捕获自定义异常：{e}")
        print(f"错误码：{e.error_code}")
    except ZeroDivisionError:
        print("除数不能为零")
    else:
        print("结果：", result)
    finally:
        print("无论如何都会执行的代码块")

# 测试自定义异常函数
custom_function(5)
custom_function(-2)
custom_function(0)
```

在这个示例中，我们定义了一个名为 `CustomError` 的自定义异常类，然后创建了一个 `custom_function` 函数来演示异常处理。在函数中，我们使用 `try` 来包裹可能引发异常的代码。如果值小于零，我们通过 `raise` 语句引发自定义异常；如果值为零，会引发内置的 `ZeroDivisionError` 异常。

在 `except` 块中，我们捕获自定义异常和零除异常，并根据情况进行处理。然后，在 `else` 块中，如果没有发生异常，我们打印出结果。无论异常是否发生，`finally` 块都会被执行，这里我们打印一条信息。

您可以通过运行上述代码来观察程序的执行情况，了解在不同情况下如何使用 `try`, `except`, `finally`, 和 `raise` 处理自定义异常。



## 







# 二、中文编码



```python
# coding=utf-8              # 注意： “ = ”之间不能有空格
```



# 三、 历代版本

## 3.1 版本切换

- 创建 conda create --name '环境名字' python = 'python版本'

  - ```python
    conda create --name Python2.7 python=2.7
    ```

    

- 激活  conda activate ‘环境名字’

  - ```python
    conda activate Python2.7
    ```

    

- 删除 conda env remove --name ‘’环境名字

  - ```
    conda env remove --name Python2.7
    ```

    

- 查看 conda env list

  - ```python
    conda env list
    $ conda env list                        
    # conda environments:
    #
    base                  *  /Users/xieshan/env/Python_env/anaconda3
    Python2.7                /Users/xieshan/env/Python_env/anaconda3/envs/Python2.7
    Python3.10               /Users/xieshan/env/Python_env/anaconda3/envs/Python3.10
    ```

    



## 3.2 Python 2

### 3.2.1 2兼容3 

​			_ _ future_ _ 库保证 python2 的兼容性

### 3.2.2  2与3的区别

- print 函数	

```python
									1. print 1       # python 2 
  
                  2. from __future__ import print_function  # python2 兼容3 
                     print ( 1 )
    
  								3. print ( 1 )   # python 3 
                   
```

- unicode                  

```python
									# python 3 编码格式默认 为 utf-8
```

- 运算符  '/' '//'

<img src="python基础md配图/image-20230721210805626.png" alt="image-20230721210805626" style="zoom:50%;" />

- 运算符 不等式

​               不等于 只能使用    `！=`    表示

- 异常

![image-20230721211230325](python基础md配图/image-20230721211230325.png)

- xrange 与 range

<img src="python基础md配图/image-20230721211512382.png" alt="image-20230721211512382" style="zoom:50%;" />

-  进制问题

<img src="python基础md配图/image-20230721211639387.png" alt="image-20230721211639387" style="zoom:50%;" />

- 去掉 `reper` 的表达式 `''`

- 去除数据类型 `long` 增加 `bytes`

- 打开文件

![image-20230721212136093](python基础md配图/image-20230721212136093.png)

-  输入字符串

![image-20230721212151596](python基础md配图/image-20230721212151596.png)

# 四 、 符号 （标识、运算、转义）

## 4.1 标识符

![image-20230721212329804](python基础md配图/image-20230721212329804.png)

## 4.2 运算符

<img src="python基础md配图/image-20230723194527382.png" alt="image-20230723194527382" style="zoom:50%;" />

### 4.2.1 算术运算符 `+ ; - ;  * ;  / ; % ; ** ; //;`

| 运算符 | 描述                                            |                  实例                  |
| :----: | :---------------------------------------------- | :------------------------------------: |
|   +    | 加 - 两个对象相加                               |                 a + b                  |
|   -    | 减 - 得到负数或是一个数减去另一个数             |                 a - b                  |
|   *    | 乘 - 两个数相乘或是返回一个被重复若干次的字符串 |                 a * b                  |
|   /    | 除 - x 除以 y                                   |                 a / b                  |
|   %    | 取模 - 返回除法的余数                           |                3% 2 =1                 |
|   **   | 幂 - 返回 x 的 y 次幂                           |                 a ** b                 |
|   //   | 地板除，同floor( )   向下取整                   | 9//2 输出结果 4 , 9.0//2.0 输出结果4.0 |

### 4.2.2 比较（关系）运算符 `== ； ！=；> ;  < ; >= ;  <= ; ` 返回`bool`值

 a 为 10，变量 b 为 20

| 运算符 |                描述                 |         实例          |
| :----: | :---------------------------------: | :-------------------: |
|   ==   |      等于 -- 比较对象是否相等       | (a == b) 返回 False。 |
|   !=   |  不等于 -- 比较两个对象是否不相等   |  (a != b) 返回 True.  |
|   >    |      大于 -- 返回 x 是否大于 y      | (a > b) 返回 False。  |
|   <    |     小于 -- 返回 x 是否小于 y。     |  (a < b) 返回 True。  |
|   >=   | 大于等于 -- 返回 x 是否大于等于 y。 | (a >= b) 返回 False。 |
|   <=   | 小于等于 -- 返回 x 是否小于等于 y。 | (a <= b) 返回 True。  |

### 4.2.3 赋值运算符 `= ;+= ;-=;  *=; /=; %=; **=; //=;`

| 运算符 | 描述             | 实例                                  |
| :----- | :--------------- | :------------------------------------ |
| =      | 简单的赋值运算符 | c = a + b 将 a + b 的运算结果赋值为 c |
| +=     | 加法赋值运算符   | c += a 等效于 c = c + a               |
| -=     | 减法赋值运算符   | c -= a 等效于 c = c - a               |
| *=     | 乘法赋值运算符   | c *= a 等效于 c = c * a               |
| /=     | 除法赋值运算符   | c /= a 等效于 c = c / a               |
| %=     | 取模赋值运算符   | c %= a 等效于 c = c % a               |
| **=    | 幂赋值运算符     | c **= a 等效于 c = c ** a             |
| //=    | 取整除赋值运算符 | c //= a 等效于 c = c // a             |

```python
a = 1
b = 2
c = 3

# print("c值为", c)
# c = c + a
# print("c+=a，一次后c值", c)

c = c ** b  # 3的2次方
print(c) # 9

c = c // b
print(c) # 1
print(3//2) # 1
```

### 4.2.4 位运算符 与 或 异或 反 左移 右移 `& ; ｜ ; ^ ; ~ ; << ; >>`

|                     | 按位与运算（a&b） | 按位或运算(a\|b) | 按位异或（a^b） |
| :-----------------: | :---------------: | :--------------: | :-------------: |
| a（60）的二进制表示 |     0011 1100     |    0011 1100     |    0011 1100    |
| b（13）的二进制表示 |     0000 1101     |    0000 1101     |    0000 1101    |
|      运算结果       |     0000 1100     |    0011 1101     |    0011 0001    |
|  结果的十进制表示   |        12         |        61        |       49        |

|                      | 按位取反（~a） | 左移（a<<2） | 右移(a>>2) |
| :------------------: | :------------: | :----------: | :--------: |
| a（60）的二进制表示  |   0011 1100    |  0011 1100   | 0011 1100  |
|       运算结果       |   1100 0011    |  1111 0000   | 0000 1111  |
| 运算结果的十进制表示 |      -61       |     240      |     15     |

**要点补充**

- 原码，补码，反码

  - 原码

    假设机器字长为n，原码就是用一个**n位的二进制数**，

    其中最高位为符号位：正数是0，负数是1。剩下的表示概数的绝对值，位数如果不够就用0补全。

  - 补码

    在原码的基础上，**符号位不变**其他位取反。

    也就是就是0变1，1变0。

  - 反码

    在反码的基础上加1

- 总结

  - 与 &  **`全1为1，否则为0`**

    按位与运算符：参与运算的两个值,如果两个相应位都为 1,则该位的结果为 1,否则为 0

    

  - 或 ｜**`有1为1，全0为0`**

    按位或运算符：只要对应的二个二进位有一个为 1 时，结果位就为 1。

    

  - 异或 ^ **`不同为1，否则为0`**

    按位异或运算符：当两对应的二进位相异（不同）时，结果为 1

    

  - 取反 ～ **`0变成1，1变成0`**

    按位取反运算符：对数据的每个二进制位取反,即把 1 变为 0，把 0 变为 1

    

  - 左移 <<  **`高位取消，低位补0`**

    左移动运算符：运算数的各二进位全部左移若干位，由"<<"右边的数指定移动的位数，高位丢弃，低位补 0。

    

  - 右移 >> 地位 **`从低位开始取消`**

    右移动运算符：把">>"左边的运算数的各二进位全部右移若干位，">>"右边的数指定移动的位数

    

    ```python
    >>> a = 60 
    >>> bin(a)
    '0b111100'
    >>> c = a<<2
    >>> bin(c)
    '0b11110000'
    >>> d = a>>2
    >>> bin(d)
    '0b1111'
    >>> f = a>>3
    >>> bin(f)
    '0b111'
    >>> 
    
    ```

    

### 4.2.5 逻辑运算符 `and（bool 与）；or（bool 或）；not（bool 非）  `返回 bool值

| 运算符 | 逻辑表达式 | 描述                                                         | 实例                    |
| :----- | :--------- | :----------------------------------------------------------- | :---------------------- |
| and    | x and y    | 布尔"与" - 如果 x 为 False，x and y 返回 False，否则它返回 y 的计算值。 | (a and b) 返回 20。     |
| or     | x or y     | 布尔"或" - 如果 x 是 True，它返回 x的值，否则它返回 y 的计算值。 | (a or b) 返回 10。      |
| not    | not x      | 布尔"非" - 如果 x 为 True，返回 False 。如果 x 为 False，它返回 True。 | not(a and b) 返回 False |

**补充知识点**

- bool 值

  - 0的bool 值为false

    ```python
    >>> bool(0)
    False
    >>> bool(2)
    True
    >>> bool(-2)
    Truen
    >>> bool(0)
    False
    >>> bool(2.2424)
    True
    >>> bool(2+1j)
    True
    
    >>> import math
    >>> bool(math.e)
    True
    >>> bool(math.pi)
    True
    >>> math.pi
    3.141592653589793
    >>> 
    
    ```

    

- 逻辑规则总结

  - and    `( a and b )`          全为ture返回true 否则返回 false

  - or       `( a  or  b  )`      全为false 返回 false 否则 返回true

  - not     `not( a )`                Ture返回false ，false返沪true

    ```python
    >>> a = 10
    >>> b = 20
    >>> 
    >>> if ( a and b ):
    ...     print ("1 - 变量 a 和 b 都为 true")
    ... else:
    ...     print ("1 - 变量 a 和 b 有一个不为 true")
    ... 
    1 - 变量 a 和 b 都为 true
    >>> if ( a or b ):
    ...     print ("2 - 变量 a 和 b 都为 true，或其中一个变量为 true")
    ... else:
    ...     print ("2 - 变量 a 和 b 都不为 true")
    ... 
    2 - 变量 a 和 b 都为 true，或其中一个变量为 true
    
    
    # 修改变量 a 的值
    >>> a = 0
    >>> if ( a and b ):
    ...     print ("3 - 变量 a 和 b 都为 true")
    ... else:
    ...     print ("3 - 变量 a 和 b 有一个不为 true")
    ... 
    3 - 变量 a 和 b 有一个不为 true
    >>> if ( a or b ):
    ...     print ("4 - 变量 a 和 b 都为 true，或其中一个变量为 true")
    ... else:
    ...     print ("4 - 变量 a 和 b 都不为 true")
    ... 
    4 - 变量 a 和 b 都为 true，或其中一个变量为 true
    >>> if not( a and b ):
    ...     print ("5 - 变量 a 和 b 都为 false，或其中一个变量为 false")
    ... else:
    ...     print ("5 - 变量 a 和 b 都为 true")
    ... 
    5 - 变量 a 和 b 都为 false，或其中一个变量为 false
    ```

    

### 4.2.6 成员运算符  `in; not in` 

| 运算符 | 描述                                                    | 实例                                              |
| :----- | :------------------------------------------------------ | :------------------------------------------------ |
| in     | 如果在指定的序列中找到值返回 True，否则返回 False。     | x 在 y 序列中 , 如果 x 在 y 序列中返回 True。     |
| not in | 如果在指定的序列中没有找到值返回 True，否则返回 False。 | x 不在 y 序列中 , 如果 x 不在 y 序列中返回 True。 |



```python
>>> a = [2,'w',"我"]
>>> print(2 in a)
True


>>> print(3 not in a ) 
True
>>> print(2 not in a )
False
>>> print(3 not in a)
True
```



### 4.2.7 身份运算符 `is ； is not`

| 运算符 | 描述                                        | 实例                                                         |
| :----- | :------------------------------------------ | :----------------------------------------------------------- |
| is     | is 是判断两个标识符是不是引用自一个对象     | x is y, 如果 id(x) 等于 id(y) , **is** 返回结果 True         |
| is not | is not 是判断两个标识符是不是引用自不同对象 | x is not y, 如果 id(x) 不等于 id(y). **is not** 返回结果 True |

```python
>>> a = 1 
>>> b = 2; c =2
>>> print(a is b)
False
>>> print(a is not b)
True
>>> print (b is c)
True
>>> print (b is not  c)
False
>>> print (id(a) == id(b))
False
>>> print (id(a) != id(b))
True
>>> print (id(c) != id(b))
False
>>> print (id(c) == id(b))
True
>>> 
```



### 4.2.8 运算符优先级 `括号；取 调用 切片 引用 ；异步；四则；位运算；比较运算；逻辑运算；条件表达；lambda; 赋值`



| 运算符                                                       | 描述                               |
| :----------------------------------------------------------- | :--------------------------------- |
| `(expressions...)`,`[expressions...]`, `{key: value...}`, `{expressions...}` | 圆括号的表达式                     |
| `x[index]`, `x[index:index]`, `x(arguments...)`, `x.attribute` | 读取，切片，调用，属性引用         |
| await x                                                      | await 表达式                       |
| `**`                                                         | 乘方(指数)                         |
| `+x`, `-x`, `~x`                                             | 正，负，按位非 NOT                 |
| `*`, `@`, `/`, `//`, `%`                                     | 乘，矩阵乘，除，整除，取余         |
| `+`, `-`                                                     | 加和减                             |
| `<<`, `>>`                                                   | 移位                               |
| `&`                                                          | 按位与 AND                         |
| `^`                                                          | 按位异或 XOR                       |
| `|`                                                          | 按位或 OR                          |
| `in,not in, is,is not, <, <=, >, >=, !=, ==`                 | 比较运算，包括成员检测和标识号检测 |
| `not x`                                                      | 逻辑非 NOT                         |
| `and`                                                        | 逻辑与 AND                         |
| `or`                                                         | 逻辑或 OR                          |
| `if -- else`                                                 | 条件表达式                         |
| `lambda`                                                     | lambda 表达式                      |
| `:=`                                                         | 赋值表达式                         |



## 4.3 转义符

### 4.3.1 多行语句

![image-20230721212416663](python基础md配图/image-20230721212416663.png)



### 4.3.2 单引号 和双引号的区别  `嵌套；转义；多行字符串；字符串插值`

在 Python 中，字符串可以使用双引号或单引号来定义，它们在**功能上是等价的**，但有一些细微的区别：

- 嵌套使用：

  - 如果字符串本身包含双引号，那么可以使用单引号来定义该字符串，以避免冲突。

  - 同样，如果字符串包含单引号，可以使用双引号来定义。
    - 例如：


```python
							str1 = "I'm a string with single quotes."
							str2 = 'He said, "Hello!"'
```

- 转义字符：

   ​    在使用双引号或单引号定义字符串时，可以通过反斜杠 `\` 来插入特殊字符，例如换行符 `\n` 或制表符 `\t`。

   ​	例如：
   ```python
   					str3 = "This is a string\nwith a new line."
   					str4 = 'This is a string\twith a tab.'
   ```

- 多行字符串：

   ​	双引号和单引号都允许定义多行字符串，但通常使用三重引号 `"""` 或 `'''` 来实现，这样更方便。

   ​	例如：
   ```python
   				str5 = """This is a 
   				multi-line string."""
   ```

- 字符串插值：

   ​     在 Python 3.6+ 中，可以使用 f-strings 来进行字符串插值，它使用花括号 `{}` 来插入变量值。在 f-strings 中，单引号和双引号没	 有区别。

   ​	 例如：
   ```python
   					name = "Alice"
   	        str6 = f"My name is {name}."
   ```

### 4.3.3 转义符 `'\'或者“\”`

|   转义字符   |                             描述                             |
| :----------: | :----------------------------------------------------------: |
| \\(在行尾时) |                            续行符                            |
|     \\\      |                          反斜杠符号                          |
|     \\'      |                            单引号                            |
|     \\"      |                            双引号                            |
|      \a      |                             响铃                             |
|      \b      |                       退格(Backspace)                        |
|     \000     |                              空                              |
|      \n      |                             换行                             |
|      \v      |                          纵向制表符                          |
|      \t      |                          横向制表符                          |
|      \r      | 回车，将 \r 后面的内容移到字符串开头，并逐一替换开头部分的字符，直至将 \r 后面的内容完全替换完成。 |
|      \f      |                             换页                             |
|     \yyy     |      八进制数，y 代表 0~7 的字符，例如：\012 代表换行。      |
|     \xyy     |  十六进制数，以 \x 开头，y 代表的字符，例如：\x0a 代表换行   |
|    \other    |                   其它的字符以普通格式输出                   |

```python
# 引号中的 \ 是续行符 对操作有帮助 对输出结果无影响
print("第一行\
第二行\
第三行")

# \\ 输出 \ , ' , ",

print('\\', '\'', '\"')

print('\000')

print('\f')

>>> print("Hello \v World!") 
Hello 
       World!
>>> 

>>> print("Hello \r World!") 
 World!
>>> print("Hello \t World!") 
Hello 	 World!

>>> print("Hello \f World!") 
Hello 
       World!
>>> 

```



			# 五、 模块和函数

## 5.1 Python 内置模块



## 5.2 python 内置函数

min（）

max()

sorted()

sum

reversed

enmurate

 





# 六、 变量类型 

## 七 数字；八 序列；九 字符串；

![image-20230722173150767](python基础md配图/image-20230722173150767.png)

# 七、 Number 数字类型

## 7.1 数字类型分类

### 7.1.1 int 

**整型(Int)** 	-   通常被称为是整型或整数，**<u>是正或负整数，不带小数点</u>**。Python3 整型是没有限制大小的，可以当作 Long 类型使用，所						 以 Python3 没有 Python2 的 Long 类型。	

```python
>>> a = 1
>>> b = -1
>>> type (a)
<class 'int'>
>>> type (b)
<class 'int'>
```



### 7.1.2 float

**浮点型(float)** - 浮点型由，**<u>整数部分与小数部分组成</u>**，浮点型也可以使用科学计数法表示（2.5e2 = 2.5 x 10^2 = 250）

​						  `2.5e2 = 250 ,英文字母e后面的数字表示乘以10的多少次方`

```python
>>> a = 5.2
>>> b = 5.2e3
>>> print (a,b,type(a),type(b))
5.2 5200.0 <class 'float'> <class 'float'>
```



### 7.1.3 complex

**复数( (complex))** - 复数由实数部分和虚数部分构成，可以用a + bj,

​								 或者`complex(a,b)`表示， 复数的实部a和虚部b都是浮点型。

```python
>>> d = 1+2j
>>> type(d)
<class 'complex'>
>>> print(d)
(1+2j)


>>> a = complex(2,3)
>>> print("a = ",a,"a的类型是",type(a))
a =  (2+3j) a的类型是 <class 'complex'>
```



## 7.2 数字类型之间的转换

- **int(x)** 将x转换为一个整数。
- **float(x)** 将x转换到一个浮点数。
- **complex(x)** 将x转换到一个复数，实数部分为 x，虚数部分为 0。
- **complex(x, y)** 将 x 和 y 转换到一个复数，实数部分为 x，虚数部分为 y。x 和 y 是数字表达式。

```python
>>> a = 1
>>> float(a)
1.0
>>> int(a)
1
>>> complex(a)
(1+0j)
>>> complex(a,2)
(1+2j)
```



## 7.3 数字类型对应的函数



### 7.3.1  内置函数 `abs( ) ; round( ); pow()`

- ` abs( )  `		绝对值函数 **absolute value** 
- ` round ( ) `    四舍五入函数  （周围附近）    
- `max ( )`        取最大值
- `min ( )`        取最小值
- `pow ( )`        取幂值   `pow(2,3)` 同`2**3`



​			以下是` round()` 方法的语法:

```python
					round( x [, n]  )
					- x -- 数值表达式。
					- n -- 表示从小数点位数，其中 x 需要四舍五入，默认值为 0。
```

​		**4舍6入5凑偶**  			

​        对于位数很多的近似数，当有效位数确定后，其后面多余的数字应该舍去，只保留有效数字最末一位，这种修约（舍入）规则是“四舍六入五成双”，也即“4舍6入5凑偶”，

​		这里“四”是指≤4 时舍去，"六"是指≥6时进上，"五"指的是根据5后面的数字来定，当5后有数时，舍5入1；当5后无有效数字时，需要分两种情况来讲：
​		（1）5前为奇数，舍5入1；
​		（2）5前为偶数，舍5不进（0是偶数）。



![image-20230723072826030](python基础md配图/image-20230723072826030.png)

```python
>>> a=-2
>>> abs(a)
2


>>> round(1.24) 
1
>>> round (1.24,1)        		# 保留小数点后一位
1.2
>>> round (1.245,2)           # 保留小数点后二位，5为最后位时，n为2 且小数点 n-1 位 是 2 为偶数 则 5进 1
1.25
>>> round (1.235,2)
1.24
>>> round (1.2335,3)
1.234
>>> round (1.2335,2)
1.23
>>> round(1.2335)
1
>>> round (1.335,2)          # 保留小数点后二位，5为最后位时，n为2 且小数点 n-1 位 是 3 为奇数 则舍5
1.33
>>> round (1.215,2)
1.22
>>> round (1.125,2)          # 保留小数点后二位，5为最后位时，n为2 且小数点 n-1 位 是 1 为奇数 则舍5
1.12


>>> x = {242,2535,5325}
>>> y = [13,2324,4255]
>>> type(x)
<class 'set'>
>>> type(y)
<class 'list'>
>>> max(y)
4255
>>> min(y)
13
>>> max(x)
5325
>>> min(x)
242

>>> print(2**3)
8
>>> pow(2,4.2)
18.37917367995256
>>> print(2**4.2)
18.37917367995256
>>> print(2.8**4.2)
75.52030437065308
>>> print(2.5**-24)
2.81474976710656e-10

```

### 7.3.2 math 模块 和 cmath 模块

- `Python math` 模块提供了许多对浮点数的数学运算函数。
- `Python cmath` 模块包含了一些用于复数运算的函数。

```python
>>> import math
>>> dir(math)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'lcm', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'nextafter', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc', 'ulp']
```

这些是Python中`math`模块提供的一些内置函数和常量。`math`模块是Python标准库中的一个数学模块，提供了许多数学运算和常数。以下是对这些函数和常量的简要解释：

- 三角函数：
   - `acos()`: 返回x的反余弦值，其中x是一个复数。
   - `acosh()`: 返回x的反双曲余弦值，其中x是一个复数。
   - `asin()`: 返回x的反正弦值，其中x是一个复数。
   - `asinh()`: 返回x的反双曲正弦值，其中x是一个复数。
   - `atan()`: 返回x的反正切值，其中x是一个复数。
   - `atanh()`: 返回x的反双曲正切值，其中x是一个复数。

- 指数和对数函数：
   - `exp()`: 返回e的x次幂，其中x是一个复数。
   - `log()`: 返回x的对数，其中x是一个复数，默认以e为底数。
   - `log10()`: 返回x的以10为底的对数，其中x是一个复数。

- 双曲函数：
   - `cosh()`: 返回x的双曲余弦值，其中x是一个复数。
   - `sinh()`: 返回x的双曲正弦值，其中x是一个复数。
   - `tanh()`: 返回x的双曲正切值，其中x是一个复数.

- 幂运算和开方：
   - `pow()`: 返回x的y次幂，其中x和y都是复数。
   - `sqrt()`: 返回x的平方根，其中x是一个复数。

- 常用数学常数：
   - `e`: 自然对数的底数（常数e，约等于2.71828），其中e是一个复数。
   - `pi`: 圆周率π，其中pi是一个复数。
   - `tau`: 圆周率的两倍，即2π，其中tau是一个复数。

- 其他数学函数：
   - `ceil()`: 返回不小于x的最小整数。
   - `copysign()`: 返回带有x的绝对值和y的符号的浮点数。
   - `degrees()`: 将x从弧度转换为度数。
   - `fabs()`: 返回x的绝对值。
   - `factorial()`: 返回x的阶乘。
   - `floor()`: 返回不大于x的最大整数。
   - `fmod()`: 返回x除以y的余数。
   - `frexp()`: 返回x的尾数和指数，用于浮点数表示。
   - `fsum()`: 返回一个迭代器的浮点数总和。
   - `gamma()`: 返回x的伽玛函数值。
   - `gcd()`: 返回x和y的最大公约数。
   - `hypot()`: 返回欧几里德范数sqrt(x*x + y*y)。
   - `isclose()`: 检查两个复数是否接近。
   - `isfinite()`: 检查复数是否是有限数。
   - `isinf()`: 检查复数是否是正无穷大或负无穷大。
   - `isnan()`: 检查复数是否是NaN（Not a Number）。
   - `isqrt()`: 返回x的平方根的整数部分。
   - `lcm()`: 返回x和y的最小公倍数。
   - `ldexp()`: 返回x * (2**i)。
   - `lgamma()`: 返回x的自然对数伽玛函数值。
   - `log1p()`: 返回1 + x的自然对数。
   - `log2()`: 返回x的以2为底的对数。
   - `modf()`: 返回x的小数部分和整数部分。
   - `nan`: 非数字，其中nan是一个复数。
   - `radians()`: 将x从度数转换为弧度。
   - `remainder()`: 返回x除以y的余数，与`fmod()`的区别在于处理负数的方式。
   - `sin()`: 返回x的正弦值，其中x是一个复数。
   - `tan()`: 返回x的正切值，其中x是一个复数。
   - `trunc()`: 返回x的截断整数部分。

- 近似和浮点数操作：
   - `erf()`: 返回x的误差函数值。
   - `erfc()`: 返回x的余补误差函数值。
   - `expm1()`: 返回e的x次幂减去1，其中x是一个复数。
   - `nextafter()`: 返回浮点数x和y之间的下一个浮点数。
   - `perm()`: 返回x的排列数。

- 累乘和累加：
   - `prod(iterable, start=1)`: 返回迭代器中所有元素的累积积。
   - `sum(iterable, start=0)`: 返回迭代器中所有元素的累积和。

- 浮点数常量：
   - `inf`: 正无穷大，其中inf是一个复数。
   - `infj`: 正无穷大的虚部，其中infj是一个复数。
   - `nanj`: 非数字的虚部，其中nanj是一个复数。

- 未分类常数：
     - `ulp()`: 返回x的最小单位。


这些函数和常数

提供了对复数进行各种数学运算和操作的功能，非常有用于科学计算和数学领域的复数处理。

```python
>>> import cmath
>>> dir(cmath)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atanh', 'cos', 'cosh', 'e', 'exp', 'inf', 'infj', 'isclose', 'isfinite', 'isinf', 'isnan', 'log', 'log10', 'nan', 'nanj', 'phase', 'pi', 'polar', 'rect', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau']
>>> 
```

根据`cmath`模块提供的函数的功能，可以将它们分为以下几类：

- 反三角函数

​			`acos()`, `acosh()`, `asin()`, `asinh()`, `atan()`, `atanh()` 这些函数用于计算复数的反余弦、反双曲余弦、反正弦、

​			反双曲正弦、反正切和反双曲正切值。

- 三角函数

​			`cos()`, `cosh()`, `sin()`, `sinh()`, `tan()`, `tanh()` 这些函数用于计算复数的余弦、双曲余弦、正弦、双曲正弦、正切

​			和双曲正切值。

- 指数和对数函数

  ​	`e`, `exp()`, `log()`, `log10()` 这些函数用于计算复数的指数函数、自然对数、以及以10为底的对数。

- 特殊常数

​			`inf`, `infj`, `nan`, `nanj`, `pi`, `tau` 这些常数代表正无穷大、正无穷大的虚部、NaN（非数字）、NaN的虚部、圆周率π以

​			及圆周率的两倍τ。

- 判断函数

  ​	`isclose()`, `isfinite()`, `isinf()`, `isnan()` 这些函数用于判断复数是否接近、是否是有限数、是否是正无穷大或负无穷大、

  ​	是否是NaN。

- 复数运算

     `phase()`, `polar()`, `rect()`, `sqrt()` 这些函数用于计算复数的辐角（相位角）、极坐标表示、复数的乘方、平方根。

  

### 7.3.3  math 模块数字  取近似值 `ceil ( ) ; floor( ) ; fabs ( )；modf()  `

- `math.ceil( )`               向上取整

  <img src="python基础md配图/image-20230723070906496.png" alt="image-20230723070906496" style="zoom: 50%;" />

- `math.floor( )`   	      向下取整

- `math.fabs( )`               取绝对值   **float absolute value**

   **abs()和fabs()的主要区别在于**：

    

  - ```python
      abs()函数可以接受任何类型的数字作为输入参数，包括整数、浮点数和复数；
      fabs()函数只接受浮点数作为输入参数。 # 如果你试图传递复数作为输入参数，则会抛出TypeError异常。 整数会转成浮点数
    ```

  - ```python
      abs()函数是Python自带的内置函数，而fabs()函数在math模块中定义。
      在使用fabs()函数之前，我们需要使用import语句来引用math模块。
    ```

- `math.modf ( )`         分离浮点数的整数部分和小数部分

```python
>>> print(a,b,c,d,e)
1 5.56 5.4 {1, 2, 4} -6.3
>>> import math
>>> math.ceil(b)
6
>>> math.floor(b)
5
>>> math.fabs(e)
6.3
>>> abs(e)
6.3
>>> f = -5
>>> math.fabs(f)
5.0
>>> abs(f)
5
>>> math.fabs(-2)
2.0

>>> complex(2,4) 
(2+4j)
>>> math.fabs(complex(2,4))      # math.fabs() 不支持复数
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't convert complex to float

>>> abs(complex(2,4))           # abs（） 支持复数
4.47213595499958

>>> math.modf(24.5353663)
(0.5353662999999997, 24.0)
>>> math.modf(2.44449)
(0.44449000000000005, 2.0)

```

### 7.3.4 math 模块  数字 对数、 指数、平方根 `log( ) ; log 10( ) ;  pow( ) ; sqrt ();hypot()`

- `math.log ( )`       

  - ```python
    math.log(x[, base])
    
    #log()是不能直接访问的，需要导入 math 模块，通过静态对象调用该方法。
    - x -- 数值表达式。
    - base -- 可选，底数，默认为 e。
    ```

- `math.log10( )`

  - ```python
    math.log10( x )
    #`log10()`是不能直接访问的，需要导入` math` 模块，通过静态对象调用该方法。
    
    ## 参数
    - x -- 数值表达式。
    ## 返回值
    返回以10为基数的x对数，x>0
    ```

- `math.pow( )`

  - ​	**描述**

    **`pow()`** 方法返回 xy（x的y次方） 的值。

    > 在python中，求x的y次方的方法有很多，例如内置函数`pow()`，math模块的`math.pow()`，以及`**`运算符，他们都需要接受两个参数，但他们各有区别：
    >
    > 1. `**`运算符,内置函数`pow()`或者`math.pow()`可以用来计算幂次方.
    > 2. 内置函数`pow()`和math模块的`math.pow()`功能是一样的，但在返回值上，`math.pow()`总是返回浮点型

  - ######    **语法**

    ```python
    math.pow(x,y)
    ## 参数
    
    - x -- 数值表达式。
    - y -- 数值表达式。
    
    ------
    
    ## 返回值
    
    返回 xy（x的y次方） 的值。
    ```

    ------

  - `math.sqrt( )`           开平方      **square root**
  - `math.hypot( )`         **hypot()** 返回欧几里德范数 sqrt(x*x + y*y)。

  ![image-20230723090917586](python基础md配图/image-20230723090917586.png)

```python
>>> math.log(8)      # 默认以e为底
2.0794415416798357
>>> math.log2(8)      # 以2为底
3.0
>>> math.log10(100)    # 以10为底
2.0



>>> pow(2,3)
8
>>> print(2**3)
8
>>> math.pow(2,3)   # math.pow 返回值为float
8.0



>>> math.sqrt(100)
10.0
>>> math.sqrt(-100)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: math domain error
>>> math.sqrt(complex(100,10))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't convert complex to float




>>> import math
>>> math.hypot(3,4)
5.0
```



### 7.3.5  `random` 模块 产生随机数 `random( ); randrange( ); seed( ); uniform( ); choice( ); shuffle( ); sample()`

- 数字

  - `random.random( )`                   范围:  [0,1)                  

    

  - `random.randrange ( )`           范围:  random.randrange(start, end, step).    产生范围  [start,end)  步长 为step

    ​															    step 默认为1 ;  start 默认为0    生成的是 int

    

  - `random.seed( )`                       提前声明， 用于标记随机数。 random.seed( a )  a 为 int，用于区分不同种子

    

  - `random.uniform( )`                 范围:  random.uniform(a, b).    产生范围  [a,b]   生成的float

    ​															

- 序列

  - `random.choice( )`                    random.choice(seq)  范围：seq中的任意一元素， seq 可以是 list tuple  string

  - `random.shuffle( )`                  随机排序

    ![image-20230723103836885](python基础md配图/image-20230723103836885.png)

  - `random.sample( )`                    random.sampel(seq,num)  从 seq 中随机选取 num 个元素

    ![image-20230723105433312](python基础md配图/image-20230723105433312.png)

```python
## random（）
>>> random.random()
0.6332620517806788
>>> random.random(1,4)  # 不能给参数
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: Random.random() takes no arguments (2 given)

## randrange()

>>> random.randrange(1,100)
15
>>> random.randrange(1,100)  # 1-99 步长1
52
>>> random.randrange(1,100)
47
>>> random.randrange(1,100)
13
>>> random.randrange(1,100,2) # 1-99 步长2
81
>>> random.randrange(1,100,2)
39


>>> random.randrange(100)   # 0-99 取消start采用默认0
28
>>> random.randrange(100,2)  # start不指定时， 不能添加步长
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/Users/xieshan/env/Python_env/anaconda3/lib/python3.9/random.py", line 316, in randrange
    raise ValueError("empty range for randrange() (%d, %d, %d)" % (istart, istop, width))
ValueError: empty range for randrange() (100, 2, -98)


## seed()

>>> random.random()  
0.030010436181082012     # 产生随机数
>>> random.random()
0.2983065543551682

>>> random.seed(10)     # 声明种子10号  生成随机数 0.5714025946899135
>>> random.random()
0.5714025946899135

>>> random.random()     # 不调用种子 无法生成指定随机数
0.4288890546751146

>>> random.seed(10)    # 调用种子  生成之前的制定随机数  0.5714025946899135
>>> random.random()
0.5714025946899135

>>> random.seed(9)
>>> random.random()
0.46300735781502145
>>> random.seed(9)
>>> random.random()
0.46300735781502145

>>> random.seed(99)         #同样适用于 给定 范围的随机数
>>> random.randrange(90)
51
>>> random.seed(99)
>>> random.randrange(90)
51

# random.uniform

>>> random.uniform(1,2)
1.8614921993193687
>>> random.uniform(1,2)
1.2125908594748118
>>> random.uniform(1,2)
1.4614832897526613
>>> random.seed(22)
>>> random.uniform(1,2)
1.9582093798172728
>>> random.seed(22)
>>> random.uniform(1,2)
1.9582093798172728



# random.choice()

>>> a = {'asd',"wo"}  # 不支持 set
>>> type(a)
<class 'set'>
>>> random.choice(a)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/Users/xieshan/env/Python_env/anaconda3/lib/python3.9/random.py", line 346, in choice
    return seq[self._randbelow(len(seq))]
TypeError: 'set' object is not subscriptable


>>> a = ['asd',"wo"]  # 支持 list
>>> type(a)
<class 'list'>
>>> random.choice(a)
'asd'
>>> random.choice(range(10))   
0
>>> random.choice(range(10))
9


>>> b=tuple(b)   # 支持tuple
>>> type(b)
<class 'tuple'>
>>> b
('asd', 'wo')
>>> random.choice(b)
'wo'


>>> d=str(a)    # 支持string
>>> d
"['asd', 'wo']"
>>> type(d)
<class 'str'>
>>> random.choice(d)
'a'
>>> random.choice(d)
"'"


# random.shuffle()

>>> print (a,b,c,d)
['wo', 'asd'] ('asd', 'wo') {'woshiyige'} ['asd', 'wo']
>>> type(a)
<class 'list'>
>>> type(c)
<class 'set'>
>>> type(b)
<class 'tuple'>
>>> type(d)
<class 'str'>

>>> random.shuffle(a)
>>> a
['wo', 'asd']

>>> random.shuffle(b)    #不支持tuple  tuple一创建顺序固定 无法进行随机排序
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/Users/xieshan/env/Python_env/anaconda3/lib/python3.9/random.py", line 362, in shuffle
    x[i], x[j] = x[j], x[i]
TypeError: 'tuple' object does not support item assignment
>>> b
('asd', 'wo')
>>> random.shuffle(c)
>>> c
{'woshiyige'}

>>> random.shuffle(d)     # 不支持str random.shuffle不适用于字符串。
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/Users/xieshan/env/Python_env/anaconda3/lib/python3.9/random.py", line 362, in shuffle
    x[i], x[j] = x[j], x[i]
TypeError: 'str' object does not support item assignment

# sample()

>>> random.sample(a,2)
['wo', 'asd']
>>> random.sample(range(10),2)
[0, 9]
>>> random.sample(range(10),2)
[3, 2]
>>> random.sample(range(10),2)
[1, 8]
>>> random.sample(range(10),6)
[9, 0, 5, 4, 2, 7]
```



### 7.3.6 math模块 cmath模块 三角函数 `sin( );cos(); tan(); asin( ); acos(); atan();atan2(y,x);degrees( ); radians( )`

|    函数     |                       描述                        |
| :---------: | :-----------------------------------------------: |
|   acos(x)   |               返回x的反余弦弧度值。               |
|   asin(x)   |               返回x的反正弦弧度值。               |
|   atan(x)   |               返回x的反正切弧度值。               |
| atan2(y, x) |       返回给定的 X 及 Y 坐标值的反正切值。        |
|   cos(x)    |               返回x的弧度的余弦值。               |
|   sin(x)    |               返回的x弧度的正弦值。               |
|   tan(x)    |                返回x弧度的正切值。                |
| degrees(x)  | 将弧度转换为角度,如degrees(math.pi/2) ， 返回90.0 |
| radians(x)  |                 将角度转换为弧度                  |

![image-20230723110552952](python基础md配图/image-20230723110552952.png)



![image-20230723110519329](python基础md配图/image-20230723110519329.png)

```python
>>> math.sin(10)
-0.5440211108893699
>>> math.sin(10+2j)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't convert complex to float
>>> import cmath
>>> math.sin(10+2j)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't convert complex to float
>>> math.sin(10+2j)

```



### 7.3.7 math模块 常量数字 `e ; pi`

- e    数学常量 e，e即自然常数（自然常数）
- pi   数学常量 pi（圆周率，一般以π来表示）



```python
>>> math.e
2.718281828459045
>>> math.pi
3.141592653589793
```



# 八 、序列 

`str ‘ ’ or “ ”; list [ ] ; tuple ( ) ; range (num) ;  bytes b' ' or b '' '' ;  bytearray   bytearray(b' ') ; set  { }; frozenset  frozenset({ });` 

1. **字符串（str）**：由字符组成的序列，用单引号或双引号括起来。例如：`'hello'` 或 `"world"`。
2. **列表（list）**：由任意类型的元素组成的序列，用方括号括起来。列表是可变序列，可以通过索引修改元素。例如：`[1, 2, 3]` 或 `['apple', 'orange', 'banana']`。
3. **元组（tuple）**：与列表类似，但一旦创建，元素不可修改，用圆括号括起来。元组是不可变序列。例如：`(1, 2, 3)` 或 `('John', 25, 'Male')`。
4. **范围（range）**：表示一个数字范围的不可变序列，常用于循环和切片操作。例如：`range(5)` 代表从 0 到 4 的序列。
5. **字节串（bytes）**：类似于字符串，但是包含原始的字节值，用单引号或双引号括起来，前缀为 `b`。例如：`b'hello'` 或 `b"world"`。
6. **字节数组（bytearray）**：与字节串类似，但是可变的，用方括号括起来，前缀为 `bytearray`。例如：`bytearray(b'hello')`。
7. **集合（set）**：包含不重复元素的无序集合，用花括号括起来。例如：`{1, 2, 3}` 或 `{'apple', 'orange', 'banana'}`。
8. **冻结集合（frozenset）**：与集合类似，但是不可修改，用 `frozenset()` 函数创建。例如：`frozenset({1, 2, 3})`。

## 8.1 序列分类

- 是否可变
  - 可变
    - 列表（list）
    - 字节数组（bytearray）
  - 不可变
    - 元组（tuple）             但一旦创建，元素不可修改
    - 字符串（str）              
    - 范围（range）            表示一个数字范围 不可变
    - 字节串（bytes）          
- 是否有序
  - 有序
    - 字符串（str）
    - 列表（list）
    - 元组（tuple）
    - 范围（range）
    - 字节串（bytes）
  - 无序
    - 集合（set）
- 序列元素类型
  - 数字
    - 列表（list）
    - 元组（tuple）
    - 范围（range）
  - 字符
    - 字符串（str）
    - 字节串（bytes）

## 8.2 序列索引

- 正索引范围：从 0 到 n-1，例如 0 表示第一个元素，1 表示第二个元素，以此类推。

- 负索引范围：从 -1 到 -n，例如 -1 表示最后一个元素，-2 表示倒数第二个元素，以此类推。

  ```python
  my_list = [10, 20, 30, 40, 50]
  
  # 正索引
  print(my_list[0])    # 输出：10
  print(my_list[2])    # 输出：30
  print(my_list[4])    # 输出：50
  
  # 负索引
  print(my_list[-1])   # 输出：50
  print(my_list[-3])   # 输出：30
  print(my_list[-5])   # 输出：10
  ```

## 8.3 序列操作

### 8.3.1 相加

- 可操作数据类型
  - list
  - str
  - tuple
  - bytes
  - bytearray

```python
>>> stra='asffsaf'
>>> strb='fagghhh'
>>> print(stra+strb)
asffsaffagghhh
>>> type(stra+strb)
<class 'str'>


>>> lista=['ad',24,2555]
>>> listb=['fa',55,66,'sf']
>>> type(lista+listb)
<class 'list'>
>>> print(lista+listb)
['ad', 24, 2555, 'fa', 55, 66, 'sf']


>>> tuplea=('a',2,'fa')
>>> tupleb=('gg',2425,255)
>>> type(tuplea+tupleb)
<class 'tuple'>
>>> print(tuplea+tupleb)
('a', 2, 'fa', 'gg', 2425, 255)
>>> 

>>> bytesa=b'asd'
>>> bytesb=b'aasdgggd'
>>> print(bytesa+bytesb)
b'asdaasdgggd'
>>> type(bytesa+bytesb)
<class 'bytes'>
>>> 

>>> a = bytearray(b'afsfaf')
>>> print(type(a))
<class 'bytearray'>
>>> b = bytearray(b'afsasdfaf')
>>> print(a+b)
bytearray(b'afsfafafsasdfaf')
>>> type(a+b)
<class 'bytearray'>
```



- 不可操作数据类型
  - set
  - range
  - 不同数据类型之间

```python
>>> seta ={'2',24,'af'} 
>>> setb ={'22',"asfaf",'af'} 
>>> print(seta+setb)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'set' and 'set'
>>> type(seta)
<class 'set'>

rangea = range(8)
rangeb = range(2)

print(rangea+rangeb)
TypeError: unsupported operand type(s) for +: 'range' and 'range'

>>> stra = 'afaf'
>>> print(a+stra)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't concat str to bytearray


```

### 8.3.2 切片

- `sname[start : end : step]`

​			其中，各个参数的含义分别是：

​				`sname`：表示序列的名称；

​				`start`：表示切片的开始索引位置（包括该位置），此参数也可以不指定，会默认为 0，也就是从序列的开头进行切片；

​				`end`：	表示切片的结束索引位置（不包括该位置），如果不指定，则默认为序列的长度；

​				`step`：  表示在切片过程中，隔几个存储位置（包含当前位置）取一次元素，也就是说，如果 step 的值大于 1，则在进行切片							   去序列元素时，会“跳跃式”的取元素。如果省略设置 step 的值，则最后一个冒号就可以省略。

​				例如，对字符串“W3Cschool”进行切片：

```python
						str="W3Cschool"
						#取索引区间为[0,2]之间（不包括索引2处的字符）的字符串
						print(str[:2])
						#隔 1 个字符取一个字符，区间是整个字符串
						print(str[::2])
						#取整个字符串，此时 [] 中只需一个冒号即可
						print(str[:])
```

- 可操作类型
  - str
  - list
  - tuple
  - bytes
  - bytearray
  - range
- 不可操作类型
  - set

```python
stra = 'woshi1个字符串a'
lista = ['wo', "是", 1, 'ge', "列表a"]
tuplea = ('wo', "是", 1, 'ge', "元组a")
bytesa = b'zijiea'
bytearraya = bytearray(b'zijiezuaa')
seta = {'wo', "是", 1, 'ge', "集合a"}
rangea = range(8)
strb = 'woshi1个字符串b'
listb = ['wo', "是", 1, 'ge', "列表b"]
tupleb = ('wo', "是", 1, 'ge', "元组b")
bytesb = b'zijieb'
bytearrayb = bytearray(b'zijiezub')
setb = {'wo', "是", 1, 'ge', "集合b"}


print(stra[:2])
print(lista[:2])
print(tuplea[:2])
print(bytesa[:2])
print(bytearraya[:2])
print(rangea)
print(rangea[:6])
print(seta[:2])    # set 不可切片

# 结果
wo
['wo', '是']
('wo', '是')
b'zi'
bytearray(b'zi')
range(0, 8)
range(0, 6)

Traceback (most recent call last):
  File "/Users/xieshan/PycharmProjects/pythonProject12/venv/test.py", line 38, in <module>
    print(seta[:2])
TypeError: 'set' object is not subscriptable

```

### 8.3.3 相乘 

- 可操作类型
  - str
  - list
  - tuple
  - bytes
  - bytearray
- 不可操作类型
  - set
  - range

```python
print(stra*3)
print(lista*3)
print(tuplea*3)
print(bytesa*3)
print(bytearraya*3)
print(seta*3)  #不支持
print(rangea*3)  #不支持
# 结果
woshi1个字符串awoshi1个字符串awoshi1个字符串a
['wo', '是', 1, 'ge', '列表a', 'wo', '是', 1, 'ge', '列表a', 'wo', '是', 1, 'ge', '列表a']
('wo', '是', 1, 'ge', '元组a', 'wo', '是', 1, 'ge', '元组a', 'wo', '是', 1, 'ge', '元组a')
b'zijieazijieazijiea'
bytearray(b'zijiezuaazijiezuaazijiezuaa')

TypeError: unsupported operand type(s) for *: 'set' and 'int'
TypeError: unsupported operand type(s) for *: 'range' and 'int'
```

### 8.3.4 查询  `print(value in seq)`



```python
			value in sequence
```

​				其中，value 表示要检查的元素，sequence 表示指定的序列。
​				例如，检查字符‘C’是否包含在字符串“W3Cschool”中，可以执行如下代码：

```python
			str="W3Cschool"
			print('C'in str)
```

可操作类型

- str
- list
- tuple
- bytes
- bytearray
- set
- range

```python
print('wo' in stra)
print('wo' in lista)
print('wo' in tuplea)
print(b'zi' in bytesa)
print(b'zi' in bytearraya)
print('wo' in seta)
print(2 in rangea)

# 结果

True
True
True
True
True
True
True
```

## 8.4 序列函数

### 8.4.1 数字函数 `min( ); max( );sorted( );sum( )`

​	`min( ) max( ) sorted( )` 			

   			 int 按照大小 计算				

​				str 按照ASCII值 计算

   `sum( )` 只支持纯数字

```python
stra = 'woshi1个字符串a'
lista = ['wo', "是", 1, 'ge', "列表a"]
tuplea = ('wo', "是", 1, 'ge', "元组a")
bytesa = b'zijiea'
bytearraya = bytearray(b'zijiezuaa')
seta = {'wo', "是", 1, 'ge', "集合a"}
rangea = range(8)

>>> min(stra)
'1'
>>> max(stra)
'符'
>>> ord('1')
49
>>> ord('符')
31526
>>> sorted(stra)
['1', 'a', 'h', 'i', 'o', 's', 'w', '个', '串', '字', '符']

>>> min(lista)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: '<' not supported between instances of 'int' and 'str'

```

### 8.4.2 反转操作 `reversed( )`

- 用法
  - ​	`list(reversed(seq))`
- 不支持 set

```python
stra = 'woshi1个字符串a'
lista = ['wo', "是", 1, 'ge', "列表a"]
tuplea = ('wo', "是", 1, 'ge', "元组a")
bytesa = b'zijiea'
bytearraya = bytearray(b'zijiezuaa')
seta = {'wo', "是", 1, 'ge', "集合a"}
rangea = range(8)



print(list(reversed(stra)))
print(list(reversed(lista)))
print(list(reversed(tuplea)))
print(list(reversed(bytesa)))
print(list(reversed(bytearraya)))
print(list(reversed(rangea)))
print(list(reversed(seta)))  # 不支持


# 结果

['a', '串', '符', '字', '个', '1', 'i', 'h', 's', 'o', 'w']
['列表a', 'ge', 1, '是', 'wo']
['元组a', 'ge', 1, '是', 'wo']
[97, 101, 105, 106, 105, 122]
[97, 97, 117, 122, 101, 105, 106, 105, 122]
[7, 6, 5, 4, 3, 2, 1, 0]
Traceback (most recent call last):
  File "/Users/xieshan/PycharmProjects/pythonProject12/venv/test.py", line 47, in <module>
    print(list(reversed(seta)))
TypeError: 'set' object is not reversible
```

### 8.4.3 枚举函数 `enumerate ( )`

![image-20230723184626500](python基础md配图/image-20230723184626500.png)

​					`enumerate()` 是 Python 中的一个内置函数，它用于将一个可迭代对象（如列表、元组、字符串等）组合为一个索引序											 列，同时返回索引和对应的元素。

​					`enumerate()` 函数的语法如下:

```python
				enumerate(iterable, start=0)
```

​					参数说明：

- `iterable`：要进行枚举的可迭代对象，可以是列表、元组、字符串等。
- `start`：可选参数，表示索引的起始值，默认为 0。如果指定了 `start` 参数，索引将从该值开始，否则从 0 开始。

​	`enumerate()` 返回一个枚举对象，它是一个迭代器。枚举对象生成一系列的元组，每个元组包含两个值：索引和对应的元素。

```python
bytesa = b'zijiea'


for i, v in enumerate(bytesa):
    print("序号", i, "值", v)


# 结果

序号 0 值 122
序号 1 值 105
序号 2 值 106
序号 3 值 105
序号 4 值 101
序号 5 值 97
```

# 九、字符串

## 9.1 创建字符串        `str = '' 或者 str =" "`

**单引号 双引号 都可以创建字符串** 

```python
>>> str1 = "1"
>>> str2 = '2332'
>>> type(str1)
<class 'str'>
>>> type(str2)
<class 'str'>
```



## 9.2 字符串 索引方式   `0 和 -1`

-  0 索引 
  - 从左到右
  - 0 ~ len-1
- -1 索引
  - 从右到左
  - -1 ～ -len

```python
>>> zfc = 'woshiyigezifuchuan'
>>> zfc[0]
'w'
>>> zfc[2]
's'
>>> zfc[-2]
'a'
>>> zfc[-1]
'n'

```



## 9.3 字符串 运算符 

| 操     作符 |                             描述                             |
| :---------: | :----------------------------------------------------------: |
|      +      |                          字符串连接                          |
|      *      |                        重复输出字符串                        |
|     []      |                   通过索引获取字符串中字符                   |
|    [ : ]    | 截取字符串中的一部分（切片），遵循**左闭右开**原则，str[0:2] 是不包含第 3 个字符的（详见上上节内容）。 |
|     in      |       成员运算符 - 如果字符串中包含给定的字符返回 True       |
|   not in    |      成员运算符 - 如果字符串中不包含给定的字符返回 True      |
|     r/R     | 原始字符串 - 原始字符串：所有的字符串都是直接按照字面的意思来使用，没有转义特殊或不能打印的字符。 原始字符串除在字符串的第一个引号前加上字母 r（不区分大小写）以外，与普通字符串有着几乎完全相同的语法。 |
|  ‘’ ’‘ ’‘   |                          格式字符串                          |

~~~python
>>> a = '字符串a'
>>> b = '字符串b'
>>> print(a+b)
字符串a字符串b
>>> print(a*2)
字符串a字符串a
>>> print(a[2])
串
>>> print(a[2:4])
串a
>>> print(a in a)
True
>>> print(a not in b)
True

# 转义符 标记引号 会失效

>>> c = '我是一个带转义符“\”的字符串'
>>> print(c)
我是一个带转义符“\”的字符串
>>> d = r'我是一个带转义符“\”的字符串'
>>> print(d)

>>> c = '我是一个带\v转义符“\”的字符串'
>>> print(c)
我是一个带
          转义符“\”的字符串
>>> c =r'我是一个带\v转义符“\”的字符串'
>>> print(c)
我是一个带\v转义符“\”的字符串





在Python中，三个引号（单引号或双引号）被用于创建多行字符串。这种表示方式与使用三个双引号的方式类似，但它可以用于创建包含换行符的多行文本，而不需要显示输入换行符。

以下是使用三个引号（'''...''' 或 """..."""）创建多行字符串的示例：

使用三个单引号：
```python
multiline_string = '''
This is a multi-line string.
It can span across multiple lines.
You don't need to use escape characters like \n.
'''
print(multiline_string)
```

使用三个双引号：
```python
multiline_string = """
This is another multi-line string.
It can also span across multiple lines.
Again, you don't need to use escape characters like \n.
"""
print(multiline_string)
```

无论使用单引号还是双引号，三个引号创建的多行字符串在输出时将保留原始格式，包含其中的换行符。

需要注意的是，三个引号创建的多行字符串通常用于注释、文档字符串或其他情况，而不是用作普通的字符串常量。

~~~



## 9.4 字符串前缀和格式化

### 9.4.1 字符串前缀 `r b f u`

​		下面是一个将不同的字符串前缀以表格形式表示的示例：

| 字符串前缀           | 描述                                        | 示例                                          |
| -------------------- | ------------------------------------------- | --------------------------------------------- |
| 普通字符串           | 默认字符串类型，不需要前缀                  | `message = "Hello, world!"`                   |
| 原始字符串 (`r`)     | 不对转义字符进行解释，适用于正则表达式等    | `path = r"C:\Users\Username"`                 |
| 字节字符串 (`b`)     | 创建字节字符串，用于处理二进制数据          | `binary_data = b'\x48\x65\x6c\x6c\x6f'`       |
| 格式化字符串 (`f`)   | 插入变量值的格式化字符串                    | `name = "Alice"; greeting = f"Hello, {name}"` |
| Unicode 字符串 (`u`) | 创建 Unicode 字符串（在 Python 3 默认支持） | `unicode_str = u"こんにちは"`                 |

​		这个表格列出了不同的字符串前缀，描述了它们的特点和用途，并举了相应的示例。根据字符串的需求和处理方式，你可以选择适当的前缀来创建合适的字符串。



字符串格式化是指将变量的值插入到一个字符串中，以形成一个新的字符串。

### 9.4.2 % 格式化 操作 `%(seq1,seq2,...,)`

| `%c`  | 格式化字符及其ASCII码                |
| ----- | ------------------------------------ |
| ` %s` | 格式化字符串                         |
| `%d`  | 格式化整型                           |
| `%u`  | 格式化无符号整型                     |
| ` %o` | 格式化无符号八进制数                 |
| `%x`  | 格式化无符号十六进制数               |
| `%X`  | 格式化无符号十六进制数（大写）       |
| ` %f` | 格式化浮点数字，可指定小数点后的精度 |
| ` %e` | 用科学计数法格式化浮点数             |
| `%E`  | 作用同`%e`，用科学计数法格式化浮点数 |
| `%g`  | `%f`和`%e`的简写                     |
| `%G`  | `%f `和` %E` 的简写                  |
| `%p`  | 用十六进制数格式化变量的地址         |



```python
>>> name = "xiaoming"
>>> age = ‘12’

#>>> print('%s的年龄是%d',name,age) # 格式是 %（seq1,seq2）
#%s的年龄是%d xiaoming 12


#>>> print('%s的年龄是%d',%(name,age))   # 不能有 逗号
#  File "<stdin>", line 1
#    print('%s的年龄是%d',%(name,age))
                     ^
#SyntaxError: invalid syntax

#>>> name = 'xiaoming'            # 跟单 双引号 无关 不能有逗号
#>>> print('%s的年龄是%d',%(name,age))
#  File "<stdin>", line 1
#    print('%s的年龄是%d',%(name,age))
                     ^
SyntaxError: invalid syntax
>>> print('%s的年龄是%d'%(name,age))
xiaoming的年龄是12

```

格式化操作符辅助指令:

| 符号  |                             功能                             |
| :---: | :----------------------------------------------------------: |
|   *   |                    定义宽度或者小数点精度                    |
|   -   |                          用做左对齐                          |
|   +   |                   在正数前面显示加号( + )                    |
| <sp>  |                      在正数前面显示空格                      |
|   #   | 在八进制数前面显示零('0')，在十六进制前面显示'0x'或者'0X'(取决于用的是'x'还是'X') |
|   0   |            显示的数字前面填充'0'而不是默认的空格             |
|   %   |                    '%%'输出一个单一的'%'                     |
| (var) |                      映射变量(字典参数)                      |
| m.n.  |    m 是显示的最小总宽度,n 是小数点后的位数(如果可用的话)     |

### 9.4.3  str.format( ) 格式化

​			使用`str.format()`方法：
​			这是一种更灵活和推荐的字符串格式化方法，在 Python 2.6+ 和 Python 3.x 版本中都可以使用。它使用花括号 `{}` 作为占位符，并使用`str.format()`方法将变量的值插入到字符串中。

​			例如：
```python
		name = "Alice"
		age = 30
		formatted_str = "My name is {}, and I am {} years old.".format(name, age)
		print(formatted_str)
```

### 9.4.4 f-string 格式化

   		使用 f-strings（在 Python 3.6+ 版本中引入）：
   		  f-strings 是一种更简洁和直观的字符串格式化方法。它在字符串前面加上 `f` 或 `F`，然后在花括号 `{}` 中使用变量名。

​			例如：

```python
		name = "Alice"
		age = 30
		formatted_str = f"My name is {name}, and I am {age} years old."
		print(formatted_str)
```

## 9.5 Unicode 字符串

在Python2中，普通字符串是以8位ASCII码进行存储的，而Unicode字符串则存储为16位unicode字符串，这样能够表示更多的字符集。使用的语法是在字符串前面加上前缀 u。

在Python3中，所有的字符串都是Unicode字符串。



## 9.6 字符串 函数

### 9.6.1 字符串包

```python
>>> dir(str)
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

```

这些函数是Python字符串对象的内置方法，它们允许您在字符串上执行各种操作和转换。下面对这些函数进行简要解释：

1. `__add__`: 实现字符串的加法运算，用于连接两个字符串。

2. `__class__`: 返回对象所属的类。

3. `__contains__`: 检查字符串是否包含指定子串。

4. `__delattr__`: 删除对象的属性。

5. `__dir__`: 返回对象的属性列表。

6. `__doc__`: 返回对象的文档字符串。

7. `__eq__`: 实现字符串的相等比较运算。

8. `__format__`: 格式化字符串。

9. `__ge__`: 实现字符串的大于等于比较运算。

10. `__getattribute__`: 获取对象的属性。

11. `__getitem__`: 获取字符串的指定索引位置的字符。

12. `__getnewargs__`: 用于序列化字符串。

13. `__gt__`: 实现字符串的大于比较运算。

14. `__hash__`: 返回对象的哈希值。

15. `__init__`: 初始化对象。

16. `__init_subclass__`: 在子类初始化时调用。

17. `__iter__`: 返回字符串的迭代器。

18. `__le__`: 实现字符串的小于等于比较运算。

19. `__len__`: 返回字符串的长度。

20. `__lt__`: 实现字符串的小于比较运算。

21. `__mod__`: 实现字符串的格式化运算（%操作符）。

22. `__mul__`: 实现字符串的乘法运算，用于重复字符串。

23. `__ne__`: 实现字符串的不等比较运算。

24. `__new__`: 创建对象时调用的构造函数。

25. `__reduce__`: 用于序列化字符串。

26. `__reduce_ex__`: 用于序列化字符串。

27. `__repr__`: 返回对象的字符串表示形式。

28. `__rmod__`: 实现字符串的反向格式化运算。

29. `__rmul__`: 实现字符串的反向乘法运算。

30. `__setattr__`: 设置对象的属性。

31. `__sizeof__`: 返回对象的大小。

32. `__str__`: 返回对象的字符串表示形式。

33. `__subclasshook__`: 子类钩子函数。

34. `capitalize()`: 将字符串的首字母转换为大写。

35. `casefold()`: 将字符串进行大小写折叠，用于忽略大小写的比较。

36. `center(width, fillchar=' ')`: 将字符串居中并使用指定字符（`fillchar`）填充到指定宽度。

37. `count(sub, start, end)`: 统计子串在字符串中出现的次数。

38. `encode(encoding='utf-8', errors='strict')`: 将字符串编码为字节对象。

39. `endswith(suffix, start, end)`: 检查字符串是否以指定的后缀结尾。

40. `expandtabs(tabsize=8)`: 将字符串中的制表符（`\t`）替换为指定数量的空格。

41. `find(sub, start, end)`: 查找子串在字符串中的第一个出现位置。

42. `format(*args, **kwargs)`: 格式化字符串，用参数填充占位符。

43. `format_map(map)`: 格式化字符串，使用映射填充占位符。

44. `index(sub, start, end)`: 查找子串在字符串中的第一个出现位置，如果未找到则引发异常。

45. `isalnum()`: 检查字符串是否由字母和数字组成。

46. `isalpha()`: 检查字符串是否全由字母组成。

47. `isascii()`: 检查字符串是否全由ASCII字符组成。

48. `isdecimal()`: 检查字符串是否全由十进制数字字符组成。

49. `isdigit()`: 检查字符串是否全由数字字符组成。

50. `isidentifier()`: 检查字符串是否是一个合法的Python标识符。

51. `islower()`: 检查字符串中的所有字母是否都是小写。

52. `isnumeric()`: 检查字符串是否全由数字字符组成，包括阿拉伯数字和其他数字字符。

53. `isprintable()`: 检查字符串是否是可打印的，即不包含控制字符。

54. `isspace()`: 检查字符串是否全由空格字符组成。

55. `istitle()`: 检查字符串是否每个单词的首字母都大写。

56. `isupper()`: 检查字符串中的所有字母是否都是大写。

57. `join(iterable)`: 将可迭代对象中的字符串元素连接起来，用当前字符串作为连接符。

58. `ljust(width, fillchar=' ')`: 将字符串左对齐并使用指定字符（`fillchar`）填充到指定宽度。

59. `lower()`: 将字符串转换为小写。

60. `lstrip(chars=None)`: 去除字符串开头的指定字符（默认为空格）。

61. `maketrans(x, y, z)`: 创建一个字符映射转换表，用于`translate()`方法。

62. `partition(sep)`: 将字符串拆分成三部分，其中第一个匹配的`sep`作为分隔符。

63. `removeprefix(prefix)`: 去除字符串开头的指定前缀。

64. `removesuffix(suffix)`: 去除字符串结尾的指定后缀。

65. `replace(old, new, count)`: 将字符串中的旧子串替换为新子串，可指定替换次数。

66. `rfind(sub, start, end)`: 查找子串在字符串中的最后一个出现位置。

67. `rindex(sub, start, end)`: 查找子串在字符串中的最后一个出现位置，如果未找到则引发异常。

68. `rjust(width, fillchar=' ')`: 将字符串右对齐并使用指定字符（`fillchar`）填充到指定宽度。

69. `rpartition(sep)`: 将字符串从右侧开始拆分成三部分，其中最后一个匹配的`sep`作为分隔符。

70. `rsplit(sep, maxsplit)`: 从右侧开始使用指定的分隔符拆分字符串。

71. `rstrip(chars=None)`: 去除字符串结尾的指定字符（默认为空格）。

72. `split(sep, maxsplit)`: 使用指定的分隔符拆分字符串，可指定最大拆分次数。

73. `splitlines(keepends=False)`: 将字符串按行拆分成一个列表，如果`keepends=True`，则保留行尾换行符。

74. `startswith(prefix, start, end)`: 检查字符串是否以指定的前缀开头。

75. `strip(chars=None)`: 去除字符串开头和结尾的指定字符（默认为空格）。

76. `swapcase()`: 将字符串中的大写字母转换为小写，小写字母转换为大写。

77. `title()`: 将字符串中的每个单词的首字母转换为大写。

78. `translate(table)`: 使用指定的转换表进行字符替换。

79. `upper()`: 将字符串转换为大写。

80. `zfill(width)`: 在字符串的左侧填充零以达到指定宽度。



### 9.6.2 字符串操作

```python
#四则
```

- `__add__`: 实现字符串的加法运算，用于连接两个字符串。

- `__mul__`: 实现字符串的乘法运算，用于重复字符串。   `multiple`    英*/*ˈmʌltɪp(ə)l*/*    美*/*ˈmʌltɪp(ə)l*/*   

  ​																												*adj.*多个的，多种的；多人共有的；影响身体许多部位的

  ​																												*n.*倍数；<英>连锁商店；（电信）复联，复接



```python
#大小写
```

`capitalize()`: 将字符串的首字母转换为大写。   `无参数 ，返回首字母大写字符串，对字符串无修改`

<img src="python基础md配图/image-20230730104303907.png" alt="image-20230730104303907" style="zoom: 50%;" />

- `casefold()`: 将所有字符转换为小写，并且将具有特殊变体的字符（例如德语中的"Ö"）转换为它们的常规形式，以便更准确地进行						字符串比较和匹配。 														 		 `无参数 ，对字符串无修改`
- `swapcase()`: 将字符串中的大写字母转换为小写，小写字母转换为大写。  `无参数 ，对字符串无修改`
- `title()`: 将字符串中的每个单词的首字母转换为大写。                               `无参数 ，对字符串无修改`

- `lower()`: 将字符串转换为小写。                                                                     `无参数 ，对字符串无修改`
- `upper()`: 将字符串转换为大写。                                                                     `无参数 ，对字符串无修改`
- `istitle()`: 检查字符串是否每个单词的首字母都大写。                              `无参数 ，对字符串无修改,返回bool值`
- `isupper()`: 检查字符串中的所有字母是否都是大写。                                  `无参数 ，对字符串无修改,返回bool值`
- `islower()`: 检查字符串中的所有字母是否都是小写                                      `无参数 ，对字符串无修改,返回bool值`

<img src="python基础md配图/image-20230730104606784.png" alt="image-20230730104606784" style="zoom:50%;" />

```python
	# 填充
```

- `center(width,'fillchar')`:     **中对齐 **   将字符串居中并使用指定字符填充到指定宽度。
- `ljust(width, 'fillchar')`:     **左对齐**    将字符串左对齐并使用指定字符填充到指定宽度。 
- `rjust(width, 'fillchar')`:     **右对齐**    将字符串右对齐并使用指定字符填充到指定宽度。
- `zfill(width)`:                             **左侧加0**  在字符串的左侧填充零以达到指定宽度。 zero fill
- `expandtabs(tabsize=8)`:                           将字符串中的制表符替换为指定数量的空格。 \t 制表符

<img src="python基础md配图/image-20230730104908726.png" alt="image-20230730104908726" style="zoom:50%;" />

<img src="python基础md配图/image-20230730104826451.png" alt="image-20230730104826451" style="zoom:50%;" />

![image-20230730105027279](python基础md配图/image-20230730105027279.png)

- `join(iterable)`:    将可迭代对象中的字符串元素连接起来，用当前字符串作为连接符。



```python
	# 去除
```

- `lstrip(chars=None)`: 去除字符串开头的指定字符（默认为空格）。

- `rstrip(chars=None)`: 去除字符串结尾的指定字符（默认为空格）。

- `strip(chars=None)`: 去除字符串开头和结尾的指定字符（默认为空格）。

  <img src="python基础md配图/image-20230730110146467.png" alt="image-20230730110146467" style="zoom:50%;" />

- `removeprefix(prefix)`: 去除字符串开头的指定前缀。

- `removesuffix(suffix)`: 去除字符串结尾的指定后缀。

<img src="python基础md配图/image-20230730105348565.png" alt="image-20230730105348565" style="zoom:50%;" />

```python
	# 替换
```

- `replace(old, new, count)`: 将字符串中的旧子串替换为新子串，可指定替换次数。
- `translate(table)`: 使用指定的转换表进行字符替换。

```python
	# 拆分
```

- `rpartition(sep)`: 将字符串从右侧开始拆分成三部分，其中最后一个匹配的`sep`作为分隔符。
- `rsplit(sep, maxsplit)`: 从右侧开始使用指定的分隔符拆分字符串。
- `split(sep, maxsplit)`: 使用指定的分隔符拆分字符串，可指定最大拆分次数。
- `splitlines(keepends=False)`: 将字符串按行拆分成一个列表，如果`keepends=True`，则保留行尾换行符。
  - str.splitlines()  									默认，按字符串拆分，不保留字符串
  - str.splitlines(keepends=true)          拆分时保留字符串

### 9.6.3 字符串查找和判断 

```python
# 比较   直接使用比较符号
```

- `__eq__`: 实现字符串的相等比较运算。         equal
- `__ge__`: 实现字符串的大于等于比较运算。   greater equal
- `__gt__`: 实现字符串的大于比较运算。           greater than
- `__le__`: 实现字符串的小于等于比较运算。   less equal
- `__lt__`: 实现字符串的小于比较运算。           less than
- `__ne__`: 实现字符串的不等比较运算。           not equal



```python
# 子串处理  
```

- `__contains__`: 检查字符串是否包含指定子串。   # 关键词 in

- `count(sub, start, end)`: 统计子串在字符串中出现的次数。
- `find(sub, start, end)`: 查找子串在字符串中的第一个出现位置。
- `index(sub, start, end)`: 查找子串在字符串中的第一个出现位置，如果未找到则引发异常。



```python
# 字符串构成
```

- `startswith(prefix, start, end)`: 检查字符串是否以指定的前缀开头。
- `endswith(suffix, start, end)`: 检查字符串是否以指定的后缀结尾。

- `isalnum()`: 检查字符串是否由字母和数字组成。
- `isalpha()`: 检查字符串是否全由字母组成。
- `isascii()`: 检查字符串是否全由ASCII字符组成。
- `isdecimal()`: 检查字符串是否全由十进制数字字符组成。
- `isdigit()`: 检查字符串是否全由数字字符组成。
- `isidentifier()`: 检查字符串是否是一个合法的Python标识符。
- `isnumeric()`: 检查字符串是否全由数字字符组成，包括阿拉伯数字和其他数字字符。
- `isprintable()`: 检查字符串是否是可打印的，即不包含控制字符。
- `isspace()`: 检查字符串是否全由空格字符组成。

### 9.6.4 字符串格式化和编码

- `__format__`: 格式化字符串。
- `encode(encoding='utf-8', errors='strict')`: 将字符串编码为字节对象。



~~~python
## 函数
strself.capitalize() 无参数 ，返回首字母大写字符串，对字符串无修改
>>>str1='a2Fsfaaa'
>>>print(str.capitalize()) 
A2fsfaaa
>>> str1
'a2Fsfaaa'

## 函数

strself.casefold()
>>> str2 = 'aaaAAAbbbBBB'
>>> str2.casefold()
'aaaaaabbbbbb'
>>> str3 = 'AAABBB'
>>> str3.casefold()
'aaabbb'
>>> str3
'AAABBB'

## 函数

strself.swapcase()

>>> str1.swapcase()
'A2fSFAAA'
>>> str1
'a2Fsfaaa'
>>> 

## 函数
strself.title()

>>> str1.title()
'A2Fsfaaa'
>>> str1
'a2Fsfaaa'

## 函数
strself.lower()
strself.upper()

>>> str1.lower()
'a2fsfaaa'
>>> str1
'a2Fsfaaa'
>>> str1.upper()
'A2FSFAAA'
>>> str1
'a2Fsfaaa'

## 函数
strself.istitle()
strself.isupper()

>>> str1.istitle()
False
>>> str.isupper()
>>> str1.isupper()
False

## 函数 center ljust rjust
strself.center(widith,'fillchar')
str.center(strself,widith,'fillchar')

str1 = 'AAddd2'
str2 = str.center(str1, 20, 'x')
print(str2)
print(str2.center(30, 'a'))

xxxxxxxAAddd2xxxxxxx
aaaaaxxxxxxxAAddd2xxxxxxxaaaaa

>>> str1.ljust(11,'x')
'a2Fsfaaaxxx'

>>> str1.rjust(11,'x')
'xxxa2Fsfaaa'

## 函数 
strself.expandtabs()

str3 = 'AAddd\t2'
str4 = str.expandtabs(str3, 16)
print(str4)

AAddd           2

## 函数 

strself.join(seq)
str.join(strself,seq)

tuple1 = ('t1', 't2', 't3')
tuple2 = ('T2', 'T2', 'T3')
str1 = '第一段'
endstr = str1.join(tuple1)
print(endstr)
endstr2 = str.join(str1, tuple2)
print(endstr2)

t1第一段t2第一段t3
T2第一段T2第一段T3

## 函数 lstrip rstrip strip

strself.lstrip('char')
str.lstrip(strself,'char')

>>> str1.lstrip('a')
'2Fsfaaa'
>>> str1.rstrip('a')
'a2Fsf'
>>> str1.strip('a')
'2Fsf'

## 函数 removeprefix removesuffix
strself.removeprefix('char')
str.removeprefix(strself,'char')

>>> str1.removeprefix('a')
'2Fsfaaa'
>>> str1.removesuffix('a')
'a2Fsfaa'

## 函数 replace 
strself.replace('oldchar','newchar')
str.replace(strself,'oldchar','newchar')

>>> str1 = 'a,asdfafs,aaa'
>>> str1.replace('a','b')
'b,bsdfbfs,bbb'

str2 = str.replace(str1, 'a', 'b')
print(str2)

b,bsdfbfs,bbb

## 函数 translate()

translatetable = str.maketrans('str1'，'str2')
strself.translate(transtable)

在 Python 中，实际上没有 `str.translate()` 函数。也就是说，字符串类（`str`）并没有直接提供 `translate()` 方法。
但是，Python 中的字符串类（`str`）提供了一个 `str.maketrans()` 静态方法，它用于创建一个字符映射表，然后可以与 `str.translate()` 方法一起使用来进行字符串的转换。这样的组合可用于执行字符替换、删除、映射等操作。

使用语法如下：
```python
str.maketrans(x[, y[, z]])
```
- `x`: 需要被替换的字符
- `y`: 替换的字符
- `z`: 要删除的字符

语法如下：
```python
str.translate(table)
```
- `table`: 由 `str.maketrans()` 方法创建的字符映射表


table = str.maketrans("aeiou", "12345")      # 创建字符映射表
text = "hello world"                         # 需要进行转换的字符串
translated_text = text.translate(table)      # 使用 translate 方法进行转换
print(translated_text)

输出：
h2ll4 w4rld

在上述示例中，我们首先使用 `str.maketrans()` 创建了一个字符映射表，该映射表将字母 "a" 转换为 "1"，"e" 转换为 "2"，"i" 转换为 "3"，"o" 转换为 "4"，"u" 转换为 "5"。然后，我们使用 `str.translate()` 方法根据这个映射表对字符串 "hello world" 进行转换，得到了转换后的结果 "h2ll4 w4rld"。注意没有在映射表中的字符（如空格）会保持不变。


## 函数 rpartition

strself.rpartition('char')  # char是字符串中的一个字符，结果是将 字符串 按照char最后一次出现的位置开始将 字符串分成3份，若															字符串长度不够，用 空格  补齐
str.rpartition(strself,'char')

str1 = 'a,asdfafs,aaa'
str2 = str.rpartition(str1, 's')
print(str2)

>>> str1 = 'a,asdfafs,aaa'
>>> str1.rpartition('a')
('a,asdfafs,aa', 'a', '')


## 函数 rsplit() split()

strself.rsplit('char','拆分次数')   # 右拆分，从右开始拆分，过程中 'char'会去掉，若'char'不足则会显示最大拆分结果
str.split(strself,'char','拆分次数')  #左拆分，从左开始拆分，过程中 'char'会去掉，若'char'不足则会显示最大拆分结果
>>> str1
'a,asdfafs,aaa'
>>> str1.rsplit('a',5)
['a,', 'sdf', 'fs,', '', '', '']
>>> str1.rsplit('a',8)
['', ',', 'sdf', 'fs,', '', '', '']
>>> str1.rsplit('a',10)
['', ',', 'sdf', 'fs,', '', '', '']
>>> str1.rsplit('a',4)
['a,asdf', 'fs,', '', '', '']
>>> str1.split('a',4)
['', ',', 'sdf', 'fs,', 'aa']
>>> 

str1 = 'a,asdfafs,aaa'
str2 = str.split(str1, 'a', 20)
print(str2)
['', ',', 'sdf', 'fs,', '', '', '']


# 函数  splitlines() 
>>> str2 ='这是一个换行符\n，一个指表格符\v，一个回车符\r'
>>> str2
'这是一个换行符\n，一个指表格符\x0b，一个回车符\r'
>>> str2.splitlines()
['这是一个换行符', '，一个指表格符', '，一个回车符']
>>> str2.splitlines(keepends=True)           # True T必须大写
['这是一个换行符\n', '，一个指表格符\x0b', '，一个回车符\r']



# 函数  count()  find()  index()

strself.count('char',startindex,endindex)
str.find(strself,'char',startindex,endindex)

>>> str1.count('a')
6
>>> str1.count('a',2,6)
1
>>> str1.find('a')
0
>>> str1.find('a',1,4)
2
>>> str1.index('a')
0
>>> str1.index('a',2,3)
2
>>> str1.index('a',3,4)   # 未找到索引报错
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not foun

# startswith() endswith()
strself.startswith('char',startindex,endindex)
str.endswith(strself,'char',startindex,endindex)

>>> str1.startswith('a')
True
>>> str1.startswith('a',3,4)
False
>>> str1.endswith('a',3,4)
False
>>> str1.endswith('a')
True
>>> str1
'a,asdfafs,aaa'

# isspace()
>>> str1.isspace()
False
~~~



# 十、列表

## 10.1 列表 CRDU

### 10.1.1 创建 [ ] ;`append();extend();insert()`

```python
>>> list1= [11,"da",2424,'ads']
>>> list1
[11, 'da', 2424, 'ads']
>>> type(list1)
<class 'list'>



>>> list1
['da', 2424, 'ads']
>>> list1.append('新加')
>>> list1
['da', 2424, 'ads', '新加']

>>> list1
[11, 'da']
>>> list1.extend(str1)
>>> list1
[11, 'da', 'a', ',', 'a', 's', 'd', 'f', 'a', 'f', 's', ',', 'a', 'a', 'a']
>>> str1
'a,asdfafs,aaa'

>>> list1
[[1], '我']
>>> list1.insert(1,'hao')
>>> list1
[[1], 'hao', '我']


```

### 10.1.2 索引 0 和 -1

- 0 索引 
  - 从左到右
  - 0 ~ len-1
- -1 索引
  - 从右到左
  - -1 ～ -len

```python
>>> list1= [11,"da",2424,'ads']
>>> list1[0]
11
>>> list1[-1]
>>> list1[0:2]  # 切片
[11, 'da']
```

### 10.1.3 删除 `del;clear();remove();pop()`

```python
>>> list1= [11,"da",2424,'ads']
>>> del list1[0]
>>> list1
['da', 2424, 'ads']

>>> list1.clear()
>>> list1
[]

>>> list1= [11,"da",2424,'ads']
>>> list1.remove(2424)
>>> list1
[11, 'da', 'ads']
>>> list1.pop(2)
'ads'
>>> list1
[11, 'da']

```



### 10.1.4 更新  `list1.[index]= value `



```python
>>> list1
[[1], 'hao', '我']
>>> list1[0]=1
>>> list1
[1, 'hao', '我']

```



### 10.1.5 复制 `copy();deepcopy` 反转`reversed()`排序`sort()`

```python
Olist = [1, 2, [3, 4]]
Clist = Olist.copy()
print(Olist)  # [1, 2, [3, 4]]
print(Clist)  # [1, 2, [3, 4]]
# 第二层
Olist[2][0] = 1
print(Olist)  # [1, 2, [1, 4]]
print(Clist)  # [1, 2, [1, 4]]

# 第一层
Olist[0] = 3
print(Olist) # [3, 2, [1, 4]]
print(Clist) # [1, 2, [1, 4]]


import copy

Olist = [1, 2, [3, 4]]
Clist = copy.deepcopy(Olist)
print(Olist) #[1, 2, [3, 4]]
print(Clist) #[1, 2, [3, 4]]
# 第二层
Olist[2][0] = 1
print(Olist) #[1, 2, [1, 4]]
print(Clist) #[1, 2, [3, 4]]

# 第一层
Olist[0] = 3
print(Olist) #[3, 2, [1, 4]]
print(Clist) #[1, 2, [3, 4]]


list1 = [13, 324, 42424, 4222, 24]
#第一种反转
list1.reverse()
print(list1) 										#[24, 4222, 42424, 324, 13]
# 第二种反转
print(list(reversed(list1)))  #[24, 4222, 42424, 324, 13]



>>> list1
[13, 324, 42424, 4222, 24]
>>> list1.sort()
>>> list1
[13, 24, 324, 4222, 42424]
>>> list1.sort(reverse= True)
>>> list1
[42424, 4222, 324, 24, 13]


```



## 10.2 列表操作

### 10.2.1  `len + *  in enumerate`

| Python 表达式                         | 结果                         | 描述                 |
| :------------------------------------ | :--------------------------- | :------------------- |
| len([1, 2, 3])                        | 3                            | 长度                 |
| [1, 2, 3] + [4, 5, 6]                 | [1, 2, 3, 4, 5, 6]           | 组合                 |
| ['Hi!'] * 4                           | ['Hi!', 'Hi!', 'Hi!', 'Hi!'] | 重复                 |
| 3 in [1, 2, 3]                        | True                         | 元素是否存在于列表中 |
| for x in [1, 2, 3]: print(x, end=" ") | 1 2 3                        | 迭代                 |

### 10.2.2  拼接  `+=`  和嵌套 [[],[],[[]]]

```python

## 拼接
>>> list1
['da', 2424, 'ads', '新加']
>>> list1 += ['1']
>>> list1
['da', 2424, 'ads', '新加', '1']

## 嵌套

>>> list1.append([123])
>>> list1
['da', 2424, 'ads', '新加', '1', [123]]
>>> list1.append('2')
>>> list1.append(1)
>>> list1.append([[1]])
>>> list1
['da', 2424, 'ads', '新加', '1', [123], '2', 1, [[1]]]

```



## 10.3  列表 函数

```python
>>> dir(list)
['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```

您列出的内容是 `list` 类的一些特殊方法（魔术方法）以及一些常用的方法。下面对这些方法进行简要解释：

1. 特殊方法（魔术方法）：
   - `__add__`: 实现列表的加法运算，例如 `list1 + list2`。
   - `__class__`: 获取对象所属的类。
   - `__class_getitem__`: 用于支持类的泛型（Generics）。
   - `__contains__`: 判断元素是否在列表中，例如 `item in list_obj`。
   - `__delattr__`: 实现删除对象的属性，例如 `del list_obj.attr`。
   - `__delitem__`: 实现删除列表中指定位置的元素，例如 `del list_obj[3]`。
   - `__dir__`: 获取对象的属性和方法列表。
   - `__doc__`: 获取类或函数的文档字符串（docstring）。
   - `__eq__`: 实现列表的相等性比较，例如 `list1 == list2`。
   - `__format__`: 格式化对象。
   - `__ge__`: 实现列表的大于等于比较，例如 `list1 >= list2`。
   - `__getattribute__`: 获取对象的属性。
   - `__getitem__`: 实现索引访问，例如 `list_obj[3]`。
   - `__gt__`: 实现列表的大于比较，例如 `list1 > list2`。
   - `__hash__`: 获取对象的哈希值。
   - `__iadd__`: 实现列表的就地加法运算，例如 `list1 += list2`。
   - `__imul__`: 实现列表的就地乘法运算，例如 `list1 *= 3`。
   - `__init__`: 初始化对象，在创建对象时调用。
   - `__init_subclass__`: 在定义子类时调用。
   - `__iter__`: 获取可迭代对象。
   - `__le__`: 实现列表的小于等于比较，例如 `list1 <= list2`。
   - `__len__`: 获取列表的长度，例如 `len(list_obj)`。
   - `__lt__`: 实现列表的小于比较，例如 `list1 < list2`。
   - `__mul__`: 实现列表的乘法运算，例如 `list_obj * 3`。
   - `__ne__`: 实现列表的不等比较，例如 `list1 != list2`。
   - `__new__`: 创建对象时调用，用于实例化对象。
   - `__reduce__`: 支持对象的序列化和反序列化。
   - `__reduce_ex__`: 支持对象的序列化和反序列化（带扩展参数）。
   - `__repr__`: 获取对象的字符串表示，用于 `repr(obj)`。
   - `__reversed__`: 获取列表的逆序迭代器，用于 `reversed(list_obj)`。
   - `__rmul__`: 实现列表的右乘法运算，例如 `3 * list_obj`。
   - `__setattr__`: 设置对象的属性。
   - `__setitem__`: 实现索引赋值，例如 `list_obj[3] = value`。
   - `__sizeof__`: 获取对象在内存中占用的字节数。
   - `__str__`: 获取对象的字符串表示，用于 `str(obj)`。
   - `__subclasshook__`: 支持类的继承。
2. 常用方法：
   - `append`: 将一个元素添加到列表末尾。
   - `clear`: 移除列表中的所有元素。
   - `copy`: 返回列表的浅拷贝（新的列表对象，但元素是原列表的引用）。
   - `count`: 返回指定元素在列表中出现的次数。
   - `extend`: 将一个可迭代对象的所有元素添加到列表末尾。
   - `index`: 返回指定元素第一次出现的位置。
   - `insert`: 在指定位置插入一个元素。
   - `pop`: 移除并返回列表中指定位置的元素。
   - `remove`: 移除列表中第一个出现的指定元素。
   - `reverse`: 对列表进行就地逆序（修改原列表）。
   - `sort`: 对列表进行就地排序（修改原列表）。

# 十一、元组

## 11.1 元组 CRUD

### 11.1.1 创建 `( )`

```python
>>> tuple1 = ('w',13,"他")
>>> tuple1
('w', 13, '他')
>>> type(tuple1)
<class 'tuple'>
```

### 11.1.2 查看 `0 -1 [startindex : endindex] [startindex : ]`

- 0 索引 
  - 从左到右
  - 0 ~ len-1
- -1 索引
  - 从右到左
  - -1 ～ -len

```python
>>> tuple1[0]
'w'
>>> tuple1[-1]
'他'
>>> tuple1[1:2]
(13,)
>>> tuple1[1:]
(13, '他')
```



### 11.1.3 更新 

**元组中的元素值是不允许修改的**，但我们可以对元组进行连接组合，如下实例:

```python
#!/usr/bin/python3

tup1 = (12, 34.56);
tup2 = ('abc', 'xyz')

# 以下修改元组元素操作是非法的。
# tup1[0] = 100

# 创建一个新的元组
tup3 = tup1 + tup2;
print (tup3)
```

**关于元组是不可变的**

所谓元组的不可变指的是元组所指向的内存中的内容不可变。



```python
>>> tup = ('W', '3', 'C', 's', 'c', 'h','o','o','l')
>>> tup[0] = 'w'     # 不支持修改元素
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
>>> id(tup)     # 查看内存地址
4440687904
>>> tup = (1,2,3)
>>> id(tup)
4441088800    # 内存地址不一样了
```

**从以上实例可以看出，重新赋值的元组 tup，绑定到新的对象了，不是修改了原来的对象。**





### 11.1.4 删除

  				删除元组

​				  元组中的元素值是不允许删除的，但我们可以使用del语句来删除整个元组，如下实例:

```python
#!/usr/bin/python3

tup = ('Google', 'W3CSchool', 1997, 2020)

print (tup)
del tup;
print ("删除后的元组 tup : ")
print (tup)
```

​				以上实例元组被删除后，输出变量会有异常信息，输出如下所示：

```python
删除后的元组 tup : 
Traceback (most recent call last):
  File "test.py", line 8, in <module>
    print (tup)
NameError: name 'tup' is not defined



>>> del tuple1
>>> tuple1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'tuple1' is not defined
```

## 11.2 元组 函数

```python
>>> dir(tuple)
['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'count', 'index']
```

`tuple` 是 Python 中的内置数据类型之一，它表示一个不可变（immutable）的有序序列，一旦创建后就无法修改。当使用 `dir(tuple)` 时，我们可以查看 `tuple` 类所拥有的特殊方法（魔术方法）和其他常用方法。

下面是 `tuple` 类的一些主要方法和属性：

1. 特殊方法（魔术方法）：
   - `__add__`: 实现元组的加法运算，例如 `tuple1 + tuple2`。
   - `__class__`: 获取对象所属的类。
   - `__class_getitem__`: 用于支持类的泛型（Generics）。
   - `__contains__`: 判断元素是否在元组中，例如 `item in tuple_obj`。
   - `__delattr__`: 实现删除对象的属性，例如 `del tuple_obj.attr`。
   - `__dir__`: 获取对象的属性和方法列表。
   - `__doc__`: 获取类或函数的文档字符串（docstring）。
   - `__eq__`: 实现元组的相等性比较，例如 `tuple1 == tuple2`。
   - `__format__`: 格式化对象。
   - `__ge__`: 实现元组的大于等于比较，例如 `tuple1 >= tuple2`。
   - `__getattribute__`: 获取对象的属性。
   - `__getitem__`: 实现索引访问，例如 `tuple_obj[3]`。
   - `__getnewargs__`: 用于支持对象的序列化和反序列化。
   - `__gt__`: 实现元组的大于比较，例如 `tuple1 > tuple2`。
   - `__hash__`: 获取对象的哈希值。
   - `__init__`: 初始化对象，在创建对象时调用。
   - `__init_subclass__`: 在定义子类时调用。
   - `__iter__`: 获取可迭代对象。
   - `__le__`: 实现元组的小于等于比较，例如 `tuple1 <= tuple2`。
   - `__len__`: 获取元组的长度，例如 `len(tuple_obj)`。
   - `__lt__`: 实现元组的小于比较，例如 `tuple1 < tuple2`。
   - `__mul__`: 实现元组的乘法运算，例如 `tuple_obj * 3`。
   - `__ne__`: 实现元组的不等比较，例如 `tuple1 != tuple2`。
   - `__new__`: 创建对象时调用，用于实例化对象。
   - `__reduce__`: 支持对象的序列化和反序列化。
   - `__reduce_ex__`: 支持对象的序列化和反序列化（带扩展参数）。
   - `__repr__`: 获取对象的字符串表示，用于 `repr(obj)`。
   - `__rmul__`: 实现元组的右乘法运算，例如 `3 * tuple_obj`。
   - `__setattr__`: 设置对象的属性。
   - `__sizeof__`: 获取对象在内存中占用的字节数。
   - `__str__`: 获取对象的字符串表示，用于 `str(obj)`。
   - `__subclasshook__`: 支持类的继承。

2. 常用方法：
   - `count`: 返回指定元素在元组中出现的次数。
   - `index`: 返回指定元素第一次出现的位置。

```python
>>> tuple1 = ('w',13,"他")
>>> tuple1.index('w')
0
>>> tuple1.count('w')
1

```

# 十二、 集合（无序、无索引）

## 12.1 集合 CRDU

### 12.1.1 创建 `{ }, set() ` 添加  `add()` 合并 `union()`set中无重复值 

```python
>>> set1 = {1,1,1,22,1}
>>> set1
{1, 22}
>>> type(set1)
<class 'set'>
>>> str1 = 'adsdd'
>>> set(str1)
{'a', 's', 'd'}
>>> set2=set()  # set()创建空集合，{} 创建空字典
>>> set2
set() 


>>> set1.add('a')   # 添加是无序的
>>> set1
{'a', 1, 22}
>>> set1.add('b')
>>> set1
{'a', 1, 'b', 22}

>>> set3 = set.union(set1,set2)
>>> set3
{'a', 1, 'b', 22}
>>> set2
set()
>>> set1
{'a', 1, 'b', 22}
>>> 

```



### 12.1.2 查看  `char in setself;isdisjoint();issubset();issuperset()`



```python
>>> print('a' in set1)
False
>>> print(1 in set1)
True
# isdisjoint() 是否存在交集 无 True 有 False 
#
>>> set1 = {1, 2, 3}
>>> set2 = {4, 5, 6}
>>> set3 = {3, 6, 9}
>>> set1.isdisjoint(set2)
True
>>> set1.isdisjoint(set3)
False
>>> print(set1.isdisjoint(set3))
False

# issubset 是否 子集 是True 否 False

>>> set1.issubset(set3)
False
>>> set1.issubset(set2)
False
>>> set4={1,2}
>>> set4.issubset(set1)
True

# issuperset 是否父集 是True 否 False
>>> set4={1,2}
>>> set1.issuperset(set4)
True
>>> set1.issuperset(set2)
False




```

### 12.1.3 删除 `clear();discard();pop();remove();`

```python
# clear()
>>> set1
{'a', 'b', 22}
>>> set1.clear()
>>> set1
set()

# discard() # 指定参数
>>> set1
{'a', 1, 'b', 22}
>>> set1.discard(1)
>>> set1
{'a', 'b', 22}
>>> set1.discard(9)  # 值不存在 不操作
>>> set1
{'a', 'b', 22}

# pop() # 无需指定
>>> set3
{'a', 1, 'b', 22}
>>> set3.pop()
'a'
>>> set3
{1, 'b', 22}
>>> set3.pop()
1
>>> set3
{'b', 22}

# remove() 指定
>>> set3
{'b', 22}
>>> set3.remove(22)
>>> set3
{'b'}
>>> set3.remove(7)  # 值不存在 报错
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: 7
>>> set3
{'b'}

```



### 12.1.4 更新 `update();intersection();intersection_update();`

### `symmetric_difference();symmetric_difference_update();`

### `difference();difference_update();`

```python
# update()
>>> set1
{1, 2, 3}
>>> str1
'adsdd'
>>> set1.update(str1)
>>> set1
{1, 2, 3, 'a', 'd', 's'}


>>> set1
{1, 2, 3, 'a', 'd', 's'}
>>> set2
{4, 5, 6}
>>> set3
{9, 3, 6}
>>> set_new = set1.intersection(set2)  # 交集 n
>>> set_new
set()
>>> set2
{4, 5, 6}
>>> set_new2 = set1.intersection(set3) 
>>> set_new2
{3}


>>> set1.intersection_update(set3)
>>> set1   # set1 被更新
{3}
>>> set2
{4, 5, 6}
>>> set3
{9, 3, 6}


>>> set2
{'a', 4, 5, 6}
>>> set3
{9, 3, 6}
>>> set_new3 = set2.symmetric_difference(set3)  # 返回新set 合集去除交集  U - n
>>> set_new3
{3, 4, 5, 'a', 9}
>>> set2
{'a', 4, 5, 6}
>>> set3
{9, 3, 6}
>>> set2.symmetric_difference_update(set3)  #输出set2和set3各自独有 更新set2 
>>> set2
{3, 4, 5, 'a', 9}  
>>> set3
{9, 3, 6}


>>> set1
{3}
>>> set2
{3, 4, 5, 'a', 9}
>>> set3
{9, 3, 6}
>>> set_new_diff = set2.difference(set3)  # 差集
>>> set_new_diff
{'a', 4, 5}
>>> set2.difference(set3)  # 差集 不更新原集合
{'a', 4, 5}
>>> set2
{3, 4, 5, 'a', 9}
>>> set3
{9, 3, 6}


```





## 12.2 set 操作

```python
a = set('abracadabra')
b = set('alacazam')

print(a)
print(b)

print(a-b)

print(a|b)

print(a&b)

print(a^b)
```

尝试一下

运行结果：

```python
{'b', 'd', 'a', 'c', 'r'}
{'l', 'z', 'm', 'a', 'c'}
{'r', 'd', 'b'}
{'l', 'z', 'b', 'm', 'd', 'a', 'c', 'r'}
{'c', 'a'}
{'l', 'z', 'b', 'm', 'r', 'd'}
```

| a-b（a集合中b没有的元素）   | b    | d    | r    |      |      |      |      |      |
| --------------------------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 集合a                       | b    | d    | r    | a    | c    |      |      |      |
| a\|b(并集）                 | b    | d    | r    | a    | c    | l    | z    | m    |
| 集合b                       |      |      |      | a    | c    | l    | z    | m    |
| a&b(交集)                   |      |      |      | a    | c    |      |      |      |
| a^b(不同时包含于a和b的元素) | b    | d    | r    |      |      | l    | z    | m    |

类似列表推导式，同样集合支持集合推导式(Set comprehension):

## 12.3 set函数

```python
>>> dir(set)
['__and__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__iand__', '__init__', '__init_subclass__', '__ior__', '__isub__', '__iter__', '__ixor__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__rand__', '__reduce__', '__reduce_ex__', '__repr__', '__ror__', '__rsub__', '__rxor__', '__setattr__', '__sizeof__', '__str__', '__sub__', '__subclasshook__', '__xor__', 'add', 'clear', 'copy', 'difference', 'difference_update', 'discard', 'intersection', 'intersection_update', 'isdisjoint', 'issubset', 'issuperset', 'pop', 'remove', 'symmetric_difference', 'symmetric_difference_update', 'union', 'update']
```

这里列出的方法是 Python 中 `set` 类的一些特殊方法（魔术方法）以及其他常用方法。`set` 是一种无序且不重复的集合数据类型，它拥有以下方法和功能：

1. 特殊方法（魔术方法）：
   - `__and__`: 实现两个集合的交集操作，例如 `set1 & set2`。
   - `__class__`: 获取对象所属的类。
   - `__class_getitem__`: 用于支持类的泛型（Generics）。
   - `__contains__`: 判断元素是否在集合中，例如 `item in set_obj`。
   - `__delattr__`: 实现删除对象的属性，例如 `del set_obj.attr`。
   - `__dir__`: 获取对象的属性和方法列表。
   - `__doc__`: 获取类或函数的文档字符串（docstring）。
   - `__eq__`: 实现集合的相等性比较，例如 `set1 == set2`。
   - `__format__`: 格式化对象。
   - `__ge__`: 实现集合的大于等于比较，例如 `set1 >= set2`。
   - `__getattribute__`: 获取对象的属性。
   - `__gt__`: 实现集合的大于比较，例如 `set1 > set2`。
   - `__hash__`: 获取对象的哈希值。
   - `__iand__`: 就地实现两个集合的交集操作，例如 `set1 &= set2`。
   - `__init__`: 初始化对象，在创建对象时调用。
   - `__init_subclass__`: 在定义子类时调用。
   - `__ior__`: 就地实现两个集合的并集操作，例如 `set1 |= set2`。
   - `__isub__`: 就地实现两个集合的差集操作，例如 `set1 -= set2`。
   - `__iter__`: 获取可迭代对象。
   - `__ixor__`: 就地实现两个集合的对称差集操作，例如 `set1 ^= set2`。
   - `__le__`: 实现集合的小于等于比较，例如 `set1 <= set2`。
   - `__len__`: 获取集合的元素数量，例如 `len(set_obj)`。
   - `__lt__`: 实现集合的小于比较，例如 `set1 < set2`。
   - `__ne__`: 实现集合的不等比较，例如 `set1 != set2`。
   - `__new__`: 创建对象时调用，用于实例化对象。
   - `__or__`: 实现两个集合的并集操作，例如 `set1 | set2`。
   - `__rand__`: 实现两个集合的交集操作（反向运算），例如 `set1.__rand__(set2)`。
   - `__reduce__`: 支持对象的序列化和反序列化。
   - `__reduce_ex__`: 支持对象的序列化和反序列化（带扩展参数）。
   - `__repr__`: 获取对象的字符串表示，用于 `repr(obj)`。
   - `__ror__`: 实现两个集合的并集操作（反向运算），例如 `set1.__ror__(set2)`。
   - `__rsub__`: 实现两个集合的差集操作（反向运算），例如 `set1.__rsub__(set2)`。
   - `__rxor__`: 实现两个集合的对称差集操作（反向运算），例如 `set1.__rxor__(set2)`。
   - `__setattr__`: 设置对象的属性。
   - `__sizeof__`: 获取对象在内存中占用的字节数。
   - `__str__`: 获取对象的字符串表示，用于 `str(obj)`。
   - `__subclasshook__`: 支持类的继承。

2. 常用方法：
   - `add`: 添加元素到集合中，如果元素已存在，则不进行任何操作。
   - `clear`: 清空集合中的所有元素。
   - `copy`: 创建一个集合的浅拷贝（新的集合对象，但元素是原集合的引用）。
   - `difference`: 返回一个新集合，包含在第一个集合中但不在第二个集合中的元素。
   - `difference_update`: 在第一个集合中移除在第二个集合中也存在的元素。
   - `discard`: 从集合中移除指定元素，如果元素不存在，则不进行任何操作。
     - <img src="python基础md配图/image-20230731162010207.png" alt="image-20230731162010207" style="zoom:50%;" />
   - `intersection`: 返回一个新集合，包含同时在两个集合中的元素。
     - <img src="python基础md配图/image-20230731161333979.png" alt="image-20230731161333979" style="zoom:50%;" />
   - `intersection_update`: 保留在两个集合中都存在的元素，更新原始集合。
   - `isdisjoint`: 判断两个集合是否没有交集，即是否没有共同的元素。
   - `issubset`: 判断一个集合是否是另一个集合的子集。
   - `issuperset`: 判断一个集合是否是另一个集合的超集。
   - `pop`: 随机移除并返回集合中的一个元素，如果集合为空则抛出 KeyError。
   - `remove`: 从集合中移除指定元素，如果元素不存在则抛出 KeyError。
   - `symmetric_difference`: 返回一个新集合，包含在两个集合中出现的非共同元素。
     - <img src="python基础md配图/image-20230731161504054.png" alt="image-20230731161504054" style="zoom:50%;" />
   - `symmetric_difference_update`: 对称差集，更新原始集合。
   - `union`: 返回一个新集合，包含两个集合中的所有元素，不包含重复元素。
   - `update`: 将一个可迭代对象的所有元素添加到集合中。
   
   

# 十三 、字典 （不是序列）

## 13.1 字典 CRUD

### 13.1.1 创建 `dict = {'key':'value';....}; dict = {};fromkeys();`

~~~python
>>> dict1 = {1:2,'key1':'value','关键词':‘值’}
>>> dict1 = {1:2,'key1':'value',"关键词":"值"}
>>> dict1
{1: 2, 'key1': 'value', '关键词': '值'}
>>> dict_empty = {}  # 空字典
>>> dict_empty
{}


`set.fromkeys(iterable, value=None)` 是 `set` 类的一个类方法，用于创建一个新的集合，并初始化该集合的元素为指定的可迭代对象 `iterable` 中的元素，或者初始化为指定的默认值 `value`。

```python
# 使用列表初始化集合
fruits = set.fromkeys(['apple', 'banana', 'orange'])
print(fruits)  # 输出：{'banana', 'orange', 'apple'}，集合中的元素来自于列表

# 使用元组初始化集合，并设置默认值为 0
scores = set.fromkeys(('Alice', 'Bob', 'Charlie'), 0)
print(scores)  # 输出：{'Bob', 'Charlie', 'Alice'}，集合中的元素来自于元组，并且默认值为 0

# 使用字符串初始化集合
letters = set.fromkeys('hello')
print(letters)  # 输出：{'e', 'l', 'h', 'o'}，集合中的元素来自于字符串

~~~



### 13.1.2 查看 `dictself[key] (注意 引号);get();items();keys();values;`

### `setdefault()`



```python
>>> dict1 = {1:2,'key1':'value',"关键词":"值"}
>>> dict1
{1: 2, 'key1': 'value', '关键词': '值'}
>>> dict1[1] # 无引号
2
>>> dict1['key1'] # 单引号
'value'
>>> dict1["关键词"] # 双引号
'值'

## get 键存在返回值 键不存在 无报错则返回指定的默认值
>>> dict1
{1: 2, 'key1': 'value', '关键词': '值'}
>>> dict1.get(1)
2
>>> dict1.get(2)
>>> 

# items() 
# dict.items(dictselt)
# dictself.items()

>>> dict.items(dict1)
dict_items([(1, 2), ('key1', 'value'), ('关键词', '值')])  # 元素类型 为 元组类型的
>>> dict1.items()
dict_items([(1, 2), ('key1', 'value'), ('关键词', '值')])


# keys() 
# dict.keys(dictselt)
# dictself.keys()

>>> dict1.keys()
dict_keys([1, 'key1', '关键词'])
>>> dict.keys(dict1)
dict_keys([1, 'key1', '关键词'])

# values() 
# dict.values(dictselt)
# dictself.values()

>>> dict1.values()
dict_values([2, 'value', '值'])
>>> dict.values(dict1)
dict_values([2, 'value', '值'])


# setdefalut  
dict.setdefalut(dictself,key,defalut_value)

list1 = [13, 324, 42424, 4222, 24]

dict1 = dict.fromkeys(list1, 0)
print(dict1)
result1 = dict.setdefault(dict1, 21, 'wrong') 
result2 = dict.setdefault(dict1, 13, 'wrong')
print(result1) # wrong
print(result2)  # 0



```



### 13.1.3 更新 `update();`

~~~python


# 使用另一个字典更新当前字典
person = {'name': 'Alice', 'age': 30}
person_updates = {'age': 31, 'city': 'New York'}

person.update(person_updates)

print(person)  # 输出：{'name': 'Alice', 'age': 31, 'city': 'New York'}



# 使用元组列表更新当前字典
person = {'name': 'Alice', 'age': 30}
updates = [('age', 31), ('city', 'New York')]

person.update(updates)

print(person)  # 输出：{'name': 'Alice', 'age': 31, 'city': 'New York'}
```

在这个例子中，我们首先创建了一个字典 `person`，然后使用 `update()` 方法分别使用另一个字典 `person_updates` 和元组列表 `updates` 来更新 `person` 字典的内容。更新后，`person` 字典中的键 `'age'` 的值被更新为 31，而键 `'city'` 被添加，并设置为 `'New York'`。

需要注意的是，如果在更新过程中，如果有相同的键在当前字典和更新的字典或可迭代对象中都存在，那么更新字典中的键值对将会覆盖当前字典中的键值对。如果在更新过程中，某个键在更新字典中不存在，则该键值对将会被添加到当前字典中。
~~~



### 13.1.4 删除 `clear() ;pop();popitem();`

```python
# clear()
>>> dict1
{1: 2, 'key1': 'value', '关键词': '值'}
>>> dict1.clear()
>>> dict1
{}

# pop()  # 指定删除 需要指定key

>>> dict1
{1: 2, 'key1': 'value', '关键词': '值'}
>>> dict1.pop()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: pop expected at least 1 argument, got 0
>>> dict1.pop(1)   
2
>>> dict1
{'key1': 'value', '关键词': '值'}

# popitem()  # 无需指定 随机删除
>>> dict1
{'key1': 'value', '关键词': '值'}
>>> dict1.popitem()
('关键词', '值')
>>> dict1
{'key1': 'value'}

```



## 13. 2 字典函数

```python
>>> dir(dict)
['__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__ior__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__ror__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
```

`dict` 是 Python 中的内置数据类型之一，表示字典（键-值对）数据结构。当使用 `dir(dict)` 时，我们可以查看 `dict` 类所拥有的特殊方法（魔术方法）和其他常用方法。

下面是 `dict` 类的一些主要方法和属性：

1. 特殊方法（魔术方法）：
   - `__class__`: 获取对象所属的类。
   - `__class_getitem__`: 用于支持类的泛型（Generics）。
   - `__contains__`: 判断字典中是否包含指定的键，例如 `key in dict_obj`。
   - `__delattr__`: 实现删除对象的属性，例如 `del dict_obj.attr`。
   - `__delitem__`: 实现删除字典中指定键对应的键值对，例如 `del dict_obj[key]`。
   - `__dir__`: 获取对象的属性和方法列表。
   - `__doc__`: 获取类或函数的文档字符串（docstring）。
   - `__eq__`: 实现字典的相等性比较，例如 `dict1 == dict2`。
   - `__format__`: 格式化对象。
   - `__ge__`: 实现字典的大于等于比较，例如 `dict1 >= dict2`。
   - `__getattribute__`: 获取对象的属性。
   - `__getitem__`: 实现通过键获取字典中的值，例如 `dict_obj[key]`。
   - `__gt__`: 实现字典的大于比较，例如 `dict1 > dict2`。
   - `__hash__`: 获取对象的哈希值。
   - `__init__`: 初始化对象，在创建对象时调用。
   - `__init_subclass__`: 在定义子类时调用。
   - `__ior__`: 就地实现字典的并集操作，例如 `dict1 |= dict2`。
   - `__iter__`: 获取可迭代对象。
   - `__le__`: 实现字典的小于等于比较，例如 `dict1 <= dict2`。
   - `__len__`: 获取字典的键值对数量，例如 `len(dict_obj)`。
   - `__lt__`: 实现字典的小于比较，例如 `dict1 < dict2`。
   - `__ne__`: 实现字典的不等比较，例如 `dict1 != dict2`。
   - `__new__`: 创建对象时调用，用于实例化对象。
   - `__or__`: 实现字典的并集操作，例如 `dict1 | dict2`。
   - `__reduce__`: 支持对象的序列化和反序列化。
   - `__reduce_ex__`: 支持对象的序列化和反序列化（带扩展参数）。
   - `__repr__`: 获取对象的字符串表示，用于 `repr(obj)`。
   - `__reversed__`: 获取字典键的反向迭代器。
   - `__ror__`: 实现字典的并集操作（反向运算），例如 `dict1.__ror__(dict2)`。
   - `__setattr__`: 设置对象的属性。
   - `__setitem__`: 实现通过键设置字典中的值，例如 `dict_obj[key] = value`。
   - `__sizeof__`: 获取对象在内存中占用的字节数。
   - `__str__`: 获取对象的字符串表示，用于 `str(obj)`。
   - `__subclasshook__`: 支持类的继承。

2. 常用方法：
   - `clear`: 清空字典中的所有键值对。
   - `copy`: 创建一个字典的浅拷贝（新的字典对象，但键值对是原字典的引用）。
   - `fromkeys`: 使用指定的键列表和默认值创建一个新的字典。
   - `get`: 获取指定键对应的值，如果键不存在，则返回指定的默认值。
   - `items`: 返回一个包含所有键值对元组的可迭代对象。
   - `keys`: 返回一个包含所有键的可迭代对象。
   - `pop`: 删除并返回指定键对应的值，如果键不存在，则返回指定的默认值或抛出 KeyError。
   - `popitem`: 随机删除并返回一个键值对，如果字典为空则抛出 KeyError。
   - `setdefault`: 获取指定键对应的值，如果键不存在，则设置默认值并返回。
   - `update`: 更新字典，添加指定的键值对或用另一个字典更新当前字典。
   - `values`: 返回一个包含所有值的可迭代对象。



## 十四 、控制语句

| 控制语句   | 优点                                          | 缺点                                       | 使用场景                                               |
| ---------- | --------------------------------------------- | ------------------------------------------ | ------------------------------------------------------ |
| for循环    | 简洁、直观                                    | 无法灵活控制步长，不适合复杂循环条件       | 遍历可迭代对象中的元素                                 |
| while循环  | 可以动态控制循环次数                          | 需要手动维护计数器和循环终止条件，代码较长 | 处理复杂的循环条件，未知循环次数的情况                 |
| break      | 提前终止循环，提高代码执行效率                | 过度使用可能导致代码逻辑混乱               | 在循环中找到目标后立即终止循环                         |
| continue   | 跳过本次循环的剩余代码，节省资源              | 过度使用可能导致代码逻辑混乱               | 在某些条件下，跳过本次循环，继续下一次循环             |
| else       | 在循环正常结束后执行一段代码块，灵活性高      | 不常用，容易被忽略                         | 在循环正常结束后执行特定的代码块，用于执行一次收尾操作 |
| match case | 多条件匹配，代码可读性高，替代多重if-else语句 | 仅Python 3.10及以上版本支持                | 处理多个条件情况，根据不同模式执行相应代码块           |
| pass       | 作为占位符，可以暂时不做任何操作              | 有可能会被忘记移除，导致不必要的执行       | 在需要暂时保留代码结构但不执行任何操作时使用           |

总体来说，

for循环和while循环在不同的情况下都有其优点和使用场景。

break和continue语句可以在特定情况下提高代码执行效率和可读性，但过度使用可能导致代码逻辑混乱。

else语句可以在循环结束后执行一段特定代码块，增加代码的灵活性。

而pass语句则作为占位符暂时不做任何操作。

别是在Python 3.10及以上版本，推荐使用match case语句来处理多条件匹配，以提高代码的可读性和维护性。

在编写代码时，根据实际需求和逻辑，选择合适的控制语句，使代码更加清晰、高效。



## 14.1  if else 条件

`if-else`是Python中的条件语句，用于根据给定条件执行不同的代码块。它的基本语法如下：

```python
if 条件1:
    # 条件1为真时执行的代码块
elif 条件2:
    # 条件2为真时执行的代码块
else:
    # 如果以上条件都不满足时执行的代码块
```

在这个语法中：

- `条件1`是一个表达式，如果它的值为`True`，则执行条件1下的代码块。
- `elif`是`else if`的缩写，用于在第一个条件不满足时检查另一个条件。你可以使用多个`elif`来添加更多的条件检查。
- `条件2`是第二个条件，如果它的值为`True`，则执行条件2下的代码块。
- `else`用于处理所有其他情况，当之前的所有条件都不满足时，执行`else`下的代码块。

下面是一个使用`if-else`的简单示例：

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"得分：{score}，等级：{grade}")
```

在这个例子中，根据不同的分数范围，我们给出了相应的等级。

`if-else`语句使得代码可以根据不同的条件进行不同的处理，是编程中常用的控制结构，能够帮助我们实现更复杂的逻辑和决策。

## 14.2  for while break continue pass 循环

1. `for`循环的例子：

```python
# 遍历列表中的元素
fruits = ['apple', 'banana', 'orange']
for fruit in fruits:
    print(fruit)

# 遍历字符串中的字符
word = 'Hello'
for char in word:
    print(char)
```



看起来你想讨论一个代码片段中的 `for _ in` 部分。在 Python 中，`for _ in` 通常用于迭代，但使用下划线 `_` 作为循环变量名是一种惯例，表示在循环中不需要使用该变量的值。

这种做法在你只关心循环执行次数，而不关心迭代的具体元素值时很有用。例如：

```python
for _ in range(5):
    print("Hello")

# 输出：
# Hello
# Hello
# Hello
# Hello
# Hello
```

在这个例子中，我们使用了 `for _ in range(5)`，其中下划线 `_` 作为循环变量。在循环体中，我们只是简单地打印了 "Hello" 五次，而没有使用循环变量 `_` 的值。

请注意，虽然这是一种常见的惯例，但你也可以选择给循环变量一个有意义的名字，尤其是当循环的目的更具可读性时。



2. `while`循环的例子：

```python
# 使用while循环计算1到5的累加和
total = 0
num = 1
while num <= 5:
    total += num
    num += 1
print(total)
```

3. `break`语句的例子：

```python
# 使用break语句在列表中找到目标元素后终止循环
numbers = [10, 20, 30, 40, 50]
target = 30
for num in numbers:
    if num == target:
        print("目标元素找到！")
        break
```

4. `continue`语句的例子：

```python
# 使用continue语句跳过奇数，打印偶数
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
for num in numbers:
    if num % 2 != 0:
        continue
    print(num)
```

5. `else`语句的例子：

```python
# 使用for循环查找列表中是否有负数
numbers = [1, 2, 3, -4, 5, 6]
for num in numbers:
    if num < 0:
        print("列表中有负数！")
        break
else:
    print("列表中没有负数。")
```

6. `pass`语句的例子：

```python
# 使用pass语句作为占位符，暂时不执行任何操作
def some_function():
    pass

# 使用pass语句定义一个空的类
class MyClass:
    pass
```

以上例子展示了这些关键字在不同场景下的应用。`for`循环用于遍历容器，`while`循环用于在满足条件时循环执行，`break`和`continue`用于控制循环流程，`else`用于在循环结束时执行特定代码块，而`pass`用于占位或创建空实体。

## 14.3  match case 

在Python 3.10中，通过PEP 634引入了`match`语句，它提供了一种更强大且更简洁的方式来处理模式匹配。它类似于其他编程语言中的`switch`或`case`语句，但增加了一些功能。

`match`语句的语法如下：

```python
match 表达式:
    模式1 => 执行动作1
    模式2 => 执行动作2
    ...
    模式n => 执行动作n
    _ => 默认动作
```

在这个语法中：

- `表达式`是你要进行匹配的值。
- `模式i`是要与`表达式`进行比较的模式。
- `执行动作i`是当`表达式`与`模式i`匹配时要执行的代码块。
- `_`是一个特殊的通配符模式，它匹配任何值。通常用作最后一个模式，用于作为默认情况，当没有其他模式匹配时执行。
- `默认动作`是当之前的所有模式都不匹配时要执行的代码块。

下面是一个简单的使用`match`的示例：

```python
def calculate(operation, x, y):
    match operation:
        case "+":
            return x + y
        case "-":
            return x - y
        case "*":
            return x * y
        case "/":
            return x / y
        case _:
            raise ValueError("无效的操作")

result = calculate("+", 5, 3)
print(result)  # 输出：8
```

可以看到，`match`语句使得代码在处理多个不同情况时更易读和简洁，比使用多个`if`和`elif`语句更优雅。

请注意，`match`语句从Python 3.10版本开始引入，因此你需要使用这个版本或更高版本才能使用这个特性。





# 十五、补充位置











# 十六、 函数

## 16.1 函数概念

下面是使用表格表示的Python函数的重要概念：

|       概念       |                             描述                             |
| :--------------: | :----------------------------------------------------------: |
|     函数定义     |  使用 `def` 关键字定义函数，包括函数名、参数列表和函数体。   |
|   函数命名规则   |    函数名应遵循标识符规则，不能以数字开头，不使用关键字。    |
|  参数和参数传递  | 函数通过参数列表接收传递给它的输入值，可以是必需或可选的。(默认参数在函数中定义) |
|     函数调用     |       使用函数名和参数调用函数，执行函数体中的代码块。       |
|      返回值      | 函数可以使用 `return` 语句返回值给调用者，否则返回 `None`。  |
| 局部变量和作用域 |    在函数内部定义的变量是局部变量，函数外部的是全局变量。    |
|    文档字符串    | 函数可以使用文档字符串描述用途、参数和返回值，通过 `help()` 或 `.__doc__` 访问。 |



**1. 基本函数定义和调用：**

```python
def say_hello():
    print("Hello, world!")

say_hello()  # 调用函数
```

**2. 函数参数：**

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # 传递参数
```

**3. 函数返回值：**

```python
def add(a, b):
    return a + b

result = add(5, 3)
print("Sum:", result)
```

**4. 默认参数值：**

```python
def greet(name="Anonymous"):
    print(f"Hello, {name}!")

greet()          # 使用默认参数值
greet("Alice")   # 传递参数
```

**5. 不定数量的参数：**

```python
def print_numbers(*numbers):
    for num in numbers:
        print(num)

print_numbers(1, 2, 3)
```

**6. 匿名函数（Lambda函数）：**

```python
add = lambda x, y: x + y
result = add(3, 4)
print("Sum:", result)
```

**7. 全局变量和局部变量：**

```python
global_var = 10

def modify_global():
    global global_var
    global_var += 5
    local_var = 20
    print("Inside function:", global_var, local_var)

modify_global()
print("Outside function:", global_var)  # 全局变量已被修改
```

**8. 文档字符串：**

```python
def calculate_power(base, exponent):
    """Calculate the power of a number."""
    return base ** exponent

print(calculate_power(2, 3))
print(calculate_power.__doc__)  # 访问文档字符串
```

## 16.2  lambda 函数 （匿名）

`lambda` 函数，也称为匿名函数，是一种在Python中创建小型、一次性的函数的方式。它允许你创建一个函数，但不需要使用 `def` 关键字进行常规的函数定义。`lambda` 函数通常用于需要简单函数的地方，以便在一行代码中定义函数并使用。

以下是 `lambda` 函数的基本语法：

```python
lambda arguments: expression  # lambda 参数：表达式
```

在这里，`arguments` 是函数的参数，而 `expression` 是函数的返回值。`lambda` 函数仅包含一个表达式，该表达式的结果作为函数的返回值。

**示例：**

下面是一个简单的示例，演示如何使用 `lambda` 函数来定义并调用一个匿名函数，计算两个数字的和：

```python
add = lambda x, y: x + y
result = add(3, 4)
print("Sum:", result)  # 输出：Sum: 7
```

在这个示例中，`lambda x, y: x + y` 定义了一个接受两个参数 `x` 和 `y` 的 `lambda` 函数，它返回这两个参数的和。

**用途：**

`lambda` 函数通常在以下情况下使用：

- 作为短期的、一次性的函数定义，不需要使用 `def` 关键字创建函数。
- 在函数参数中需要一个函数作为参数，但只需要简单的操作。
- 在列表排序、映射（`map`）、过滤（`filter`）等需要函数作为参数的情况下使用。

**示例：**

```python
numbers = [1, 2, 3, 4, 5]
squared = map(lambda x: x ** 2, numbers)
print(list(squared))  # 输出：[1, 4, 9, 16, 25]
```

在这个示例中，`lambda` 函数被用于 `map` 函数，将每个数字平方。

尽管 `lambda` 函数在某些情况下非常有用，但对于复杂的函数逻辑，仍然建议使用常规的 `def` 函数来保持代码的可读性和可维护性。



## 16.3 闭包

### 16.3.1 闭包概念

	在 Python 中，闭包是一种函数的概念，它可以访问并操作其定义外部作用域中的变量，即使这些外部作用域的函数已经执行完毕。闭包是一种强大的编程概念，允许你在函数内部创建和使用局部变量，并将其保持在内存中，以便在函数调用结束后仍然可以使用。以下是关于 Python 闭包的一些重要概念：

1. **内部函数访问外部函数的变量：** 在闭包中，内部函数可以访问外部函数的局部变量、参数以及外部函数内部嵌套的其他函数。

2. **延迟绑定：** Python 中的闭包使用延迟绑定的方式，这意味着内部函数在执行时才确定其引用的外部变量。这种方式使得闭包可以捕获外部变量的最新值。

3. **保持状态：** 闭包允许在函数调用结束后继续保持状态。这对于需要记住某些状态或上下文的情况非常有用，比如回调函数。

4. **函数工厂：** 闭包可以用来创建函数工厂，即在外部函数内部动态地生成并返回内部函数，每个内部函数都可以具有不同的行为，但共享相同的外部作用域。

5. **数据封装：** 闭包可以用于实现数据的封装，将数据与操作它的函数捆绑在一起，形成一个更加高级的数据结构。

下面是一个简单的 Python 闭包示例：

```python
def outer_function(outer_variable):
    def inner_function():
        print("Value from outer function:", outer_variable)
    
    return inner_function

closure = outer_function("Hello, closure!")
closure()  # 输出 "Value from outer function: Hello, closure!"
```

在这个示例中，`inner_function` 是一个闭包，它可以访问外部函数 `outer_function` 中的局部变量 `outer_variable`，即使 `outer_function` 已经执行完毕。

总之，闭包是一种灵活且强大的编程概念，允许你在 Python 中创建具有持久状态和动态行为的函数。它在很多编程场景中都非常有用，例如回调函数、装饰器、工厂函数等。

### 16.3.2 闭包例子

		当涉及闭包的概念时，还有一些更复杂和实际的示例，展示了闭包在编程中的实际应用。以下是一些额外的 Python 闭包示例：

##### （1）建私有变量

```python
def create_counter():
    count = 0
    
    def increment():
        nonlocal count
        count += 1
        return count
    
    def get_count():
        return count
    
    return increment, get_count

increment_fn, get_count_fn = create_counter()
print(increment_fn())  # 输出 1
print(increment_fn())  # 输出 2
print(get_count_fn())  # 输出当前计数器值
```

在这个示例中，`create_counter` 函数返回两个闭包函数，`increment` 和 `get_count`。`count` 变量实际上变成了一个私有变量，只能通过这两个闭包函数来访问和修改。

##### （2）创建装饰器

```python
def uppercase_decorator(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return result.upper()
    return wrapper

@uppercase_decorator
def greet(name):
    return f"Hello, {name}"

print(greet("Alice"))  # 输出 "HELLO, ALICE"
```

在这个示例中，`uppercase_decorator` 是一个接受函数作为参数的闭包，它返回一个新的函数 `wrapper`，该函数会将原始函数的返回值转换为大写。

##### （3）缓存功能

```python
def memoize(func):
    cache = {}
    
    def wrapper(*args):
        if args in cache:
            return cache[args]
        result = func(*args)
        cache[args] = result
        return result
    
    return wrapper

@memoize
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

print(fibonacci(10))  # 输出斐波那契数列中第 10 项的值
```

在这个示例中，`memoize` 是一个闭包，它实现了一个简单的缓存功能，用于存储已经计算过的函数结果，从而避免重复计算。

这些示例展示了闭包在实际编程中的多种应用，包括创建私有变量、装饰器、缓存等。闭包允许你在函数内部创建具有持久状态和自定义行为的函数，从而增强了代码的灵活性和可重用性。

### 16.3.3 闭包作用



| 作用       | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| 保持状态   | 闭包允许函数保持外部作用域中的变量状态，多次调用之间共享状态。 |
| 数据封装   | 通过将数据与操作它的函数绑定在一起，形成更高层次的抽象。     |
| 函数工厂   | 在外部函数内部动态生成并返回内部函数，每个函数具有不同行为但共享相同的外部作用域。 |
| 装饰器     | 用于修改函数行为，添加额外逻辑或功能，而无需更改原始函数定义。 |
| 回调函数   | 在事件处理和异步编程中作为回调函数，传递处理逻辑给其他函数以在特定条件下调用。 |
| 缓存和优化 | 实现缓存功能，存储已计算结果以提高性能，避免重复计算。       |
| 私有变量   | 在闭包中定义变量，模拟私有变量，增加代码封装性和安全性。     |
| 柯里化     | 用于实现函数柯里化，将多参数函数转化为一系列接收单个参数的函数。 |



闭包在编程中有多种作用，它们使得代码更灵活、可重用并且更容易维护。以下是闭包的一些主要作用：

- **保持状态：** 闭包允许函数捕获并保持其定义外部作用域中的变量状态。这使得函数在多次调用之间可以共享状态，类似于对象的实例变量。

- **数据封装：** 闭包可以用于创建类似于面向对象编程中实例的封装数据结构。它允许你将数据与操作它的函数绑定在一起，从而形成更高层次的抽象。

- **函数工厂：** 闭包可以用于创建函数工厂，即在外部函数内部动态生成并返回内部函数。每个内部函数都可以具有不同的行为，但共享相同的外部作用域。

- **装饰器：** 闭包可以用于创建装饰器，用于修改函数的行为，添加额外的逻辑或功能，而不必修改原始函数的定义。

- **回调函数：** 闭包在事件处理和异步编程中常用作回调函数。它允许你将处理逻辑传递给其他函数，以便在某些条件满足时调用。

- **缓存和优化：** 闭包可以用于实现缓存功能，存储已计算的结果以避免重复计算，从而提高性能。

- **私有变量：** 通过在闭包中定义变量，你可以模拟私有变量，从而限制对变量的直接访问，增加代码的封装性和安全性。

- **柯里化：** 闭包可以用于实现函数柯里化，将接受多个参数的函数转换为一系列接受单个参数的函数。

  - 函数柯里化（Currying）是一种函数式编程的技术，它允许你将一个多参数的函数转化为一系列只接受单个参数的函数。这种转化使得函数变得更加灵活，可以部分应用参数，以及更方便地创建新的函数。

    在柯里化中，每个接受单个参数的函数都会返回一个新的函数，该函数进一步接受一个参数，然后返回另一个新函数，以此类推。这些新函数可以在不同的上下文中使用，部分应用参数，从而创建更多的复用和变化的可能性。

    以下是一个简单的 Python 示例，展示了如何使用函数柯里化：

    ```python
    def curried_add(x):
        def inner(y):
            return x + y
        return inner
    
    add_five = curried_add(5)
    add_ten = curried_add(10)
    
    print(add_five(3))  # 输出 8
    print(add_ten(3))   # 输出 13
    ```

    在这个示例中，`curried_add` 是一个柯里化函数，它接受一个参数 `x`，然后返回一个内部函数 `inner`，该函数接受另一个参数 `y`，并返回 `x + y`。通过调用 `curried_add` 函数，我们实际上创建了新的函数 `add_five` 和 `add_ten`，这些函数分别将 `5` 和 `10` 添加到传入的参数上。

    函数柯里化有助于创建更具可读性和可重用性的函数，它允许你动态地生成新的函数，根据实际需要提供不同的参数组合。这在某些情况下可以让代码更加清晰和模块化。


​				

## 16.4 迭代器、生成器和装饰器

### 16.4.1 对比

下面是对迭代器、生成器和装饰器在不同方面的比较：

| 特性     | 迭代器                            | 生成器                           | 装饰器                           |
| -------- | --------------------------------- | -------------------------------- | -------------------------------- |
| 定义     | 用于遍历集合元素的机制            | 逐步生成值的特殊迭代器           | 用于修改函数行为的函数           |
| 用途     | 循环遍历数据集合                  | 处理大量数据、节省内存           | 添加功能、逻辑或处理             |
| 工作原理 | `__iter__()` 和 `__next__()` 方法 | 函数和 `yield` 语句              | 函数嵌套和返回新函数             |
| 适用场景 | 遍历集合、数据处理                | 大数据集、延迟计算               | 功能扩展、日志记录等             |
| 示例     | 列表、字典、文件对象              | 斐波那契数列、文件逐行读取       | 输出转换、日志记录等             |
| 内存消耗 | 需要在内存中存储完整数据集        | 仅生成和返回一个值时，内存消耗小 | 通常不会增加内存消耗             |
| 可重复性 | 可重复遍历相同集合元素            | 仅能迭代一次                     | 可重复应用于多个函数             |
| 简介性   | 相对较简单                        | 相对简单，但可能涉及生成器表达式 | 通过函数嵌套和装饰器语法相对复杂 |

这个表格提供了关于迭代器、生成器和装饰器在不同方面的比较。请注意，每个概念都有其独特的用途和优势，根据具体的编程需求来选择合适的技术。

### 16.4.2 迭代器			

迭代器是一种用于遍历集合（如列表、元组、字典等）中元素的方式，它允许你逐个访问集合的元素而不需要提前将整个集合加载到内存中。迭代器在Python中的实现是通过实现两个特殊方法：`__iter__()` 和 `__next__()`。

- **优点：**
  - **内存效率高：** 迭代器逐个提供元素，不需要一次性加载整个集合到内存中，适用于处理大数据集。
  - **懒加载：** 只在需要时才生成下一个元素，减少了计算和内存开销。

- **缺点：**
  - **不可逆向：** 一旦迭代器开始，它不能回到前面的元素。
  - **无法获取长度：** 由于元素是按需生成的，无法直接获取迭代器的长度。

- **使用场景：**
  - **大数据集处理：** 当处理数据集太大无法一次性加载到内存时，使用迭代器逐个获取元素。
  - **延迟计算：** 当只在需要时才计算值的情况下，使用生成器可以避免不必要的计算。
  - **无限序列：** 可以用迭代器来表示无限的数列，如斐波那契数列等。

以下是一个迭代器的简单示例：

```python
class MyIterator:
    def __init__(self, max_value):
        self.max_value = max_value
        self.current = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.current < self.max_value:
            value = self.current
            self.current += 1
            return value
        else:
            raise StopIteration

# 使用迭代器遍历值
my_iter = MyIterator(5)
for num in my_iter:
    print(num)
```

在上面的例子中，`MyIterator` 是一个简单的迭代器类，它可以生成从0到`max_value-1`的整数。当我们通过`for`循环遍历迭代器时，它会逐个返回元素，直到达到上限后抛出`StopIteration`异常。

迭代器是一种访问集合内元素的方式，它逐个提供元素而不需一次性加载整个集合。

​				生成器是一种特殊的迭代器，它通过函数调用生成值，并使用`yield`来保持函数状态，从而实现逐个生成元素。

​				生成器在处理大量数据或需要按需生成数据时特别有用。

### 16.4.3 生成器

生成器（Generators）是一种特殊类型的迭代器，它们使用函数来逐个产生值，而不是一次性生成整个序列。这种惰性计算的方式使得生成器在处理大量数据或需要逐个产生值的情况下非常有效。

<img src="python基础md配图/image-20230802142958577.png" alt="image-20230802142958577" style="zoom:50%;" />

**优点：**

1. **惰性计算：** 生成器在需要时才会计算和生成值，避免了一次性加载和计算大量数据带来的内存和性能压力。
2. **节省内存：** 由于只在需要时生成值，生成器的内存消耗通常较低。
3. **适用于大数据集：** 生成器适用于处理大型数据集合，无需一次性将所有数据加载到内存中。
4. **简洁性：** 生成器函数通常比自定义迭代器实现更简洁，不需要显式定义 `__next__` 方法。

**缺点：**

1. **单向遍历：** 生成器通常只能在一个方向上遍历，遍历完后无法回到初始状态再次遍历。
2. **不可重复遍历：** 一旦生成器遍历完毕，通常不能重新遍历，需要重新创建生成器实例。

**适用场景：**

1. **处理大数据集：** 当需要处理大型数据集或无限序列时，生成器能够按需生成值，避免内存占用过多。
2. **惰性计算：** 在需要逐个生成值、避免一次性计算的情况下，如解析大文件、处理流数据等。
3. **代码简洁性：** 生成器函数通常相对简洁，能够更轻松地实现自定义的迭代逻辑。

**示例代码：**

以下是一个简单的生成器函数示例，用于生成斐波那契数列：

```python
def fibonacci_generator(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

# 使用生成器遍历斐波那契数列
fib_gen = fibonacci_generator(5)
for num in fib_gen:
    print(num)
```

总之，生成器是一种强大的工具，能够以惰性计算的方式处理大数据集合和逐个生成值的情况，以提高效率并降低内存消耗。



### 16.4.4 装饰器 （ 参数 返回值为函数）

装饰器（Decorators）是一种 Python 编程中的强大工具，用于修改函数或方法的行为，而不需要修改它们的原始定义。装饰器可以看作是“包装”了原始函数的函数，它可以添加额外的功能、逻辑或处理，从而在不改变函数代码的情况下，实现对函数的扩展和定制。

装饰器的主要特点是**接受一个函数作为参数，并返回一个新的函数**。这个新函数通常会在调用原始函数之前或之后执行一些额外的操作。装饰器可以应用于普通函数、方法甚至类，从而实现代码的重用和模块化。

以下是一个简单的装饰器示例：

```python
def uppercase_decorator(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return result.upper()
    return wrapper

@uppercase_decorator
def greet(name):
    return f"Hello, {name}"

print(greet("Alice"))  # 输出 "HELLO, ALICE"



```

在这个示例中，`uppercase_decorator` 是一个装饰器函数，它接受一个函数 `func` 作为参数，然后返回一个新的函数 `wrapper`。通过使用 `@uppercase_decorator` 将装饰器应用于 `greet` 函数，我们修改了 `greet` 函数的行为，使其返回的字符串变为大写。

**装饰器的应用范围非常广泛，包括但不限于：**

- **添加日志记录或调试信息。**
- **计时函数执行时间。**
- **输入验证或处理异常。**
- **授权检查和权限控制。**
- **缓存函数结果以提高性能**。

装饰器的使用使代码更具模块性、可读性和可维护性。Python 中有许多内置的装饰器，同时你也可以自己编写自定义的装饰器来满足特定的需求。



### 16.4.5 *args, **kwargs

​				`def wrapper(*args, **kwargs):` 是在装饰器中定义的内部函数，通常用于包装原始函数，并在调用原始函数之前或之后执行额外的操作。这里的 `*args` 和 `**kwargs` 是用于接收任意数量的位置参数和关键字参数的语法。

​			让我更详细地解释这段代码：

```python
def uppercase_decorator(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        return result.upper()
    return wrapper
```

​			在这个示例中，我们定义了一个名为 `uppercase_decorator` 的装饰器函数。这个装饰器接受一个函数 `func` 作为参数，并返回一个新的函数 `wrapper`。

​			在 `wrapper` 函数中，`*args` 和 `**kwargs` 是用来接受任意数量的位置参数和关键字参数。内部的 `func(*args, **kwargs)` 表达式调用了原始函数，并将传递给 `wrapper` 的参数传递给原始函数。

在调用原始函数后，我们可以对返回值 `result` 进行额外的操作。在这个示例中，我们使用 `result.upper()` 将原始函数的返回值转换为大写。

​			最终，`wrapper` 函数返回被修改后的结果，而 `uppercase_decorator` 装饰器返回 `wrapper` 函数，从而实现了对原始函数的扩展和定制。

​			使用类似于 `*args` 和 `**kwargs` 的参数语法，可以使装饰器更通用，适用于接受不同数量参数的函数。这是装饰器的强大之处，它允许你以一种灵活的方式修改函数行为，而不需要针对不同函数编写不同的装饰器。

### 16.4.6 生成器和普通函数对比

让我们通过一个具体示例，对比生成器代码和普通代码，来看看它们在处理数据时的区别。

假设我们需要生成一个包含一定数量斐波那契数列值的列表。

**普通代码（不使用生成器）：**

```python
def generate_fibonacci_list(n):
    fibonacci_list = []
    a, b = 0, 1
    for _ in range(n):
        fibonacci_list.append(a)
        a, b = b, a + b
    return fibonacci_list

fib_list = generate_fibonacci_list(5)
print(fib_list)
```

**生成器代码：**

```python
def fibonacci_generator(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b

fib_gen = fibonacci_generator(5)
fib_list = list(fib_gen)
print(fib_list)
```

**对比分析：**

- 优点

  - **内存消耗：**
    - 在普通代码中，我们在内存中创建了一个列表来存储所有的斐波那契数列值，
    - 而在生成器代码中，只有在需要时逐个生成值，从而减少了内存消耗。


  - **性能：** 生成器代码在每次生成值后，不需要保存所有的值，因此性能更高，尤其在处理大量数据时。

  - **简洁性：** 生成器代码相对简洁，因为不需要显式地管理列表的操作。

  - **惰性计算：** 生成器代码只在需要值时进行计算，而普通代码在一开始就计算所有值。

- 缺点

  - **可重复性：** 

    - 生成器通常只能遍历一次，

    - 而普通代码可以通过重新调用函数来重新生成列表。

总的来说，生成器代码更加高效，能够减少内存消耗并提高性能，尤其在处理大量数据时。然而，普通代码更适合需要重复遍历或修改值的情况。根据具体需求选择合适的方法。

## 16.5 高阶函数

#### 16.5.1 高阶函数分类

Python 中的高阶函数是指可以接受一个或多个函数作为参数，并/或返回一个函数作为结果的函数。高阶函数是函数式编程的一个核心概念，它可以用于创建更抽象、灵活和可复用的代码。

以下是一些关于高阶函数的常见概念和示例：

##### （1）接受函数作为参数：

```python
def apply_function(func, x):
    return func(x)

def square(x):
    return x ** 2

result = apply_function(square, 5)  # 将 square 函数应用于 5
print(result)  # 输出 25
```

在这个示例中，`apply_function` 是一个高阶函数，它接受一个函数 `func` 和一个参数 `x`，然后将 `func(x)` 的结果返回。我们将 `square` 函数作为参数传递给 `apply_function`，并将其应用于 5。

##### （2）返回函数作为结果：

```python
def power_function(exp):
    def raise_to_power(x):
        return x ** exp
    return raise_to_power

square_function = power_function(2)
cube_function = power_function(3)

print(square_function(4))  # 输出 16 (4^2)
print(cube_function(3))    # 输出 27 (3^3)
```

在这个示例中，`power_function` 是一个高阶函数，它返回内部定义的函数 `raise_to_power`。我们可以通过调用 `power_function` 并传递指数参数来获得不同次幂的函数。

##### （3） **内置高阶函数：**

​			Python 的内置函数 `map`、`filter` 和 `reduce` 也是高阶函数的例子。它们分别用于将函数应用于可迭代对象的每个元素、根据函数的条件筛选元素以及对序列中的元素进行累积操作。

```python
numbers = [1, 2, 3, 4, 5]
squared = list(map(lambda x: x ** 2, numbers))  # 对每个元素进行平方
evens = list(filter(lambda x: x % 2 == 0, numbers))  # 筛选偶数
total = reduce(lambda x, y: x + y, numbers)  # 累积求和
```

这些示例演示了高阶函数在 Python 中的应用。它们可以帮助你编写更加灵活和可重用的代码，将函数作为一等公民来处理，以及实现更高级的抽象。

#### 16.5.2 常用函数(map filter reduce)

- map （将元素按照指定函数 **转化** 成一个迭代器）

  - `map()` 是 Python 内置的高阶函数之一，它用于将一个函数应用于可迭代对象（如列表、元组等）中的每个元素，并返回一个新的迭代器，包含了应用函数后的结果。

    `map()` 函数的基本语法如下：

    ```python
    map(function, iterable, ...)
    ```

    - `function`：要应用的函数，可以是内置函数、自定义函数或匿名函数（lambda 表达式）。
    - `iterable`：一个或多个可迭代对象，如列表、元组等。
    - 返回值：返回一个迭代器，包含了将函数应用于每个可迭代对象元素的结果。

    以下是一些使用 `map()` 函数的示例：

    ```python
    # 将列表中的每个元素平方
    numbers = [1, 2, 3, 4, 5]
    squared = list(map(lambda x: x ** 2, numbers))
    # 输出: [1, 4, 9, 16, 25]
    
    # 将字符串列表转换为大写
    words = ['apple', 'banana', 'cherry']
    uppercased = list(map(str.upper, words))
    # 输出: ['APPLE', 'BANANA', 'CHERRY']
    ```

    在第一个示例中，我们使用 `map()` 将一个 lambda 函数应用于列表 `numbers` 中的每个元素，将它们平方，并将结果存储在 `squared` 列表中。

    在第二个示例中，我们使用 `map()` 将内置的 `str.upper` 函数应用于字符串列表 `words` 中的每个元素，将它们转换为大写。

    请注意，`map()` 返回一个迭代器，因此在使用结果之前，你可能需要将其转换为列表或其他形式的可迭代对象。`map()` 函数可以帮助你对可迭代对象的每个元素应用相同的操作，从而简化代码并提高可读性。

- filter (将元素按照函数 进行 **筛选** 返回一个迭代器)

  - `filter()` 是 Python 内置的高阶函数之一，它用于根据指定的条件筛选可迭代对象中的元素，并返回一个新的迭代器，包含满足条件的元素。

    `filter()` 函数的基本语法如下：

    ```python
    filter(function, iterable)
    ```

    - `function`：要用于筛选的函数，可以是内置函数、自定义函数或匿名函数（lambda 表达式）。
    - `iterable`：一个可迭代对象，如列表、元组等。
    - 返回值：返回一个迭代器，包含满足条件的元素。

    以下是一个使用 `filter()` 函数的示例：

    ```python
    # 筛选出列表中的偶数
    numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    evens = list(filter(lambda x: x % 2 == 0, numbers))
    # 输出: [2, 4, 6, 8, 10]
    
    # 筛选出字符串列表中长度大于等于 5 的字符串
    words = ['apple', 'banana', 'cherry', 'date', 'elderberry']
    long_words = list(filter(lambda word: len(word) >= 5, words))
    # 输出: ['banana', 'cherry', 'elderberry']
    ```

    在第一个示例中，我们使用 `filter()` 将一个 lambda 函数应用于列表 `numbers` 中的每个元素，筛选出偶数，并将结果存储在 `evens` 列表中。

    在第二个示例中，我们使用 `filter()` 将 lambda 函数应用于字符串列表 `words` 中的每个元素，筛选出长度大于等于 5 的字符串。

    与 `map()` 类似，`filter()` 也返回一个迭代器，因此可能需要将其转换为列表或其他可迭代对象以使用结果。`filter()` 函数可用于过滤出满足特定条件的元素，从而减少需要处理的数据量。

- reduce (将元素按照函数 进行 **累积** 返回一个迭代器)

  - <img src="python基础md配图/image-20230808135127917.png" alt="image-20230808135127917" style="zoom:50%;" />

  - `reduce()` 是 Python 标准库 `functools` 模块中的一个函数，它用于将一个二元函数作用于一个序列（如列表或元组）中的元素，以便逐个进行累积操作。在 Python 3 中，`reduce()` 函数已经从内置函数移到了 `functools` 模块中。

    `reduce()` 函数的基本语法如下：

    ```python
    functools.reduce(function, iterable[, initializer])
    ```

    - `function`：用于累积操作的二元函数，它接受两个参数。
    - `iterable`：一个可迭代对象，如列表、元组等。
    - `initializer`（可选）：初始值，如果指定，则将它作为累积的初始值。
    - 返回值：返回累积的最终结果。

    以下是一个使用 `reduce()` 函数的示例：

    ```python
    import functools
    
    # 使用 reduce 计算列表中所有元素的累积乘积
    numbers = [1, 2, 3, 4, 5]
    product = functools.reduce(lambda x, y: x * y, numbers)
    # 输出: 120 (1 * 2 * 3 * 4 * 5)
    ```

    在这个示例中，我们导入了 `functools` 模块并使用 `reduce()` 函数将 lambda 函数应用于列表 `numbers` 中的所有元素，计算它们的累积乘积。

    需要注意的是，在 Python 3 中，`reduce()` 函数已经不再是内置函数，因此在使用之前需要先导入 `functools` 模块。

    `reduce()` 函数对于需要将一个操作逐个应用到序列中的元素，并将结果累积起来的情况非常有用。然而，由于 Python 3 推崇函数式编程和可读性，使用显示的循环或内置函数（如 `sum()`、`max()`、`min()`）通常更易于理解和维护。

# 十七、 模块

​		当涉及到在 Python 中进行代码组织、重用和模块化时，模块是一个非常重要的概念。一个模块可以包含一组相关的函数、类、变量和语句，它们被封装在一起，以便于代码的管理和维护。

## 17.1 创建模块

​		在 Python 中，每个 `.py` 文件都可以被看作是一个模块。你可以在文件中定义函数、类、变量等。以下是一个简单的示例，创建了一个名为 `math_operations.py` 的模块：

```python
# math_operations.py

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

## 17.2 导入模块



​		你可以使用 `import` 关键字来导入一个模块，从而在其他地方使用其中定义的内容。以下是导入示例：

```python
import math_operations

sum_result = math_operations.add(5, 3)
print("Sum:", sum_result)

diff_result = math_operations.subtract(10, 4)
print("Difference:", diff_result)
```











**3. 别名：**

​		你可以为导入的模块创建别名，以便于使用。这在模块名很长或容易与其他名字冲突时很有用。

```python
import math_operations as math_ops

sum_result = math_ops.add(5, 3)
print("Sum:", sum_result)
```

**4. 从模块中导入特定内容：**

​		你也可以选择性地导入模块中的特定函数、类或变量，而不是全部导入。

```python
from math_operations import add

sum_result = add(5, 3)
print("Sum:", sum_result)
```

**5. 模块的命名空间：**

​		导入模块后，你可以通过模块名来访问其中定义的内容，以避免命名冲突。例如：`math_operations.add()`。

**6. 模块搜索路径：**

​		Python 会在特定的目录中搜索模块。标准库模块位于 Python 安装路径下，而你自己创建的模块应该位于 Python 能够找到的路径中。你可以通过 `sys.path` 来查看和修改搜索路径。

​		

**7. 标准库模块：**

​		Python 标准库提供了丰富的模块和库，涵盖了各种领域，从文件操作到网络编程，从数学计算到数据处理，从日期时间处理到图形用户界面等。以下是一些常见的 Python 标准库模块及其功能的示例列表（这里列出的只是一部分，实际上标准库更加广泛）：

|         模块名          |                     功能描述                     |
| :---------------------: | :----------------------------------------------: |
|          `os`           |           操作系统接口、文件和目录操作           |
|          `sys`          |      Python解释器相关功能、命令行参数处理等      |
|         `math`          |                数学运算函数、常量                |
|        `random`         |                   生成伪随机数                   |
|       `datetime`        |                  处理日期和时间                  |
|         `json`          |              JSON 数据的解析和生成               |
|          `re`           |                  正则表达式操作                  |
|          `csv`          |                  处理 CSV 文件                   |
|        `urllib`         |                网络请求、处理 URL                |
|         `http`          |                HTTP 协议相关功能                 |
|        `sqlite3`        |                操作 SQLite 数据库                |
|        `pickle`         |               对象序列化和反序列化               |
|          `xml`          |                  处理 XML 数据                   |
|      `collections`      | 额外的数据结构，如 Counter、deque、namedtuple 等 |
|       `itertools`       |                  迭代器和组合器                  |
|        `os.path`        |                   处理文件路径                   |
|        `logging`        |                     日志记录                     |
|       `argparse`        |                  命令行参数解析                  |
|         `time`          |                     处理时间                     |
|         `gzip`          |                处理 gzip 压缩文件                |
|        `hashlib`        |                     哈希算法                     |
|        `socket`         |                     网络编程                     |
|       `threading`       |                    多线程编程                    |
|      `subprocess`       |                 创建和管理子进程                 |
|       `unittest`        |                   单元测试框架                   |
| `xml.etree.ElementTree` |               解析和操作 XML 文档                |
|        `pathlib`        |              面向对象的文件路径操作              |
|         `email`         |                   处理电子邮件                   |

|     `zipfile`     |                处理 ZIP 压缩文件                 |
| :---------------: | :----------------------------------------------: |
|       `io`        |                 处理流和文件 I/O                 |
|    `functools`    |                提供函数式编程工具                |
|     `shutil`      |                文件和目录操作工具                |
| `multiprocessing` |                    多进程编程                    |
|  `configparser`   |                   解析配置文件                   |
|     `tkinter`     |               Python 的标准 GUI 库               |
|     `asyncio`     |               异步 I/O 和事件循环                |
|       `pdb`       |                 Python 的调试器                  |
|     `timeit`      |                 测试代码执行时间                 |
|      `uuid`       |        生成和操作 UUID（通用唯一标识符）         |
|    `calendar`     |              生成日历和处理日期事件              |
|   `collections`   | 额外的数据结构，如 Counter、deque、namedtuple 等 |
|      `enum`       |                   创建枚举类型                   |

**8. 文档字符串（Docstrings）：**

​         模块可以包含文档字符串，用于描述模块的用途、功能和使用方法。可以通过 `模块名.__doc__` 访问文档字符串。

**9. 模块的导入顺序：**

​		Python 会按照一定的顺序查找并导入模块，

- 首先在内置模块中查找，
- 然后在搜索路径中查找。
- 如果存在同名模块，Python 会按照搜索路径中的顺序导入第一个找到的模块。

​		模块是代码组织、重用和模块化的关键工具，它可以使代码更易于管理、维护和扩展。通过合理地使用模块，你可以有效地组织代码，提高代码的可读性和可维护性。

# 十八 、I/O操作

## 18.1 输出

在 Python 中，你可以使用内置的 `print()` 函数来输出信息到标准输出（通常是控制台）。`print()` 函数接受一个或多个参数，并将它们显示在屏幕上。以下是一些常见的 Python 输出信息的示例：

- **输出字符串：**

```python
print("Hello, World!")
```

- **输出变量值：**

```python
name = "Alice"
print("My name is", name)
```

- **输出多个参数：**

```python
age = 25
print("Name:", name, "Age:", age)
```

- **使用格式化字符串：**

```python
print("Name: {}, Age: {}".format(name, age))
```

- **使用 f-字符串（Python 3.6+）：**

```python
print(f"Name: {name}, Age: {age}")
```

- **输出数字和计算结果：**

```python
x = 5
y = 10
print("Sum:", x + y)
```

- **输出列表、元组等数据结构：**

```python
fruits = ["apple", "banana", "cherry"]
print("Fruits:", fruits)
```

**设置分隔符和结束符：**
```python
print("Hello", "World", sep=", ", end="!\n")
```

- **使用转义字符：**

```python
print("This is a new line.\nAnd this is another line.")
```

- **将输出写入文件：**

```python
with open("output.txt", "w") as f:
    print("This will be written to the file.", file=f)
```



## 18.2 输入      （字符串类型）

在 Python 3.x 版本中，`input()` 是一个内置函数，用于从用户获取输入，并将用户输入的内容作为字符串返回。它等待用户在标准输入（通常是控制台）中输入一行文本，然后将用户输入的内容作为字符串返回。

以下是一些在 Python 3.x 版本中使用 `input()` 函数的示例：

**获取用户输入并存储到变量：**
```python
name = input("Please enter your name: ")
print("Hello, " + name + "!")
```

**获取用户输入并转换为数字：**

```python
age = int(input("Please enter your age: "))
print("You are {} years old.".format(age))
```

**获取多个输入项：**
```python
first_name = input("First Name: ")
last_name = input("Last Name: ")
print("Full Name:", first_name, last_name)
```

**注意事项：**
- `input()` 函数返回的内容始终是字符串类型。
  - 如果你需要将用户输入转换为其他类型，如整数或浮点数，
  - 你需要使用适当的类型转换函数（如 `int()` 或 `float()`）来进行转换。

- 当用户输入时，`input()` 函数会等待用户按下回车键。
- 用户输入的内容将被返回给程序。如果用户输入多个词（用空格分隔），这些词将被视为单个字符串。

总之，`input()` 函数是用于与用户进行交互、获取输入以及实现简单交互式程序的一个重要工具。

## 18.3 File 文件操作

### 18.3.1 open 函数

​		`open()` 函数是 Python 的内置函数之一，用于打开文件并返回一个文件对象，从而可以对文件进行读取或写入操作。

​		`open()` 函数的基本语法如下：

```python
open(file, mode='r', buffering=-1, encoding=None, errors=None, newline=None, closefd=True, opener=None)
```

​		参数说明：
- `file`: 要打开的文件路径（字符串类型）。
- `mode`: 打开文件的模式，默认为 `'r'`（只读）。

  - 其他常用模式有 `'w'`（写入）、`'a'`（追加）、`'rb'`（以二进制模式读取）、`'wb'`（以二进制模式写入）等。
  - 下表总结了 `open()` 函数的 `mode` 参数及其含义：

    | Mode | 含义                   | 文件操作                                       |
    | ---- | ---------------------- | ---------------------------------------------- |
    | 'r'  | 只读模式。             | 读取文件内容。                                 |
    | 'w'  | 写入模式。             | 写入文件内容，如果文件已存在则清空。           |
    | 'a'  | 追加模式。             | 在文件末尾追加内容，如果文件不存在则创建。     |
    | 'b'  | 二进制模式。           | 以二进制格式读写文件。                         |
    | 't'  | 文本模式（默认）。     | 以文本格式读写文件。                           |
    | 'x'  | 独占创建模式。         | 创建新文件，如果文件已存在则引发错误。         |
    | 'r+' | 读写模式（可读可写）。 | 既可以读取也可以写入文件。                     |
    | 'w+' | 读写模式（可读可写）。 | 既可以读取也可以写入文件，会清空文件内容。     |
    | 'a+' | 读写模式（可读可写）。 | 既可以读取也可以写入文件，从文件末尾追加内容。 |

    <img src="python基础md配图/image-20230802200945932.png" alt="image-20230802200945932" style="zoom:50%;" />


<img src="python基础md配图/image-20230802201344559.png" alt="image-20230802201344559" style="zoom:50%;" />

**只读模式：**

```python
with open("example.txt", "r") as f:
    content = f.read()
```

**写入模式：**

```python
with open("output.txt", "w") as f:
    f.write("Hello, World!")
```

**追加模式：**
```python
with open("log.txt", "a") as f:
    f.write("New log entry\n")
```

**二进制读写模式：**
```python
with open("binary_data.bin", "rb") as f:
    data = f.read()
```

**文本读写模式：**
```python
with open("text_file.txt", "rt") as f:
    text = f.read()
```

请注意，`mode` 参数可以同时包含多个选项，例如 `'rb'` 或 `'w+'`，以适应不同的文件操作需求。在使用时，根据你的具体需求来选择合适的模式。

- `buffering`: 设置缓冲策略。如果为 0，表示无缓冲。如果为 1，表示行缓冲。如果为 -1 或更大的值，表示缓冲区大小（以字节为单位）。
- `encoding`: 指定文件的编码格式（仅在文本模式下使用）。
- `errors`: 指定编码错误处理策略。
- `newline`: 指定换行符的处理方式（仅在文本模式下使用）。
- `closefd`: 控制是否关闭底层的文件描述符。默认为 `True`。
- `opener`: 自定义打开文件的函数（用于高级用户）。

### 18.3.2 函数用法

以下是一些使用 `open()` 函数的示例：

**读取文件内容：**
```python
with open("example.txt", "r") as f: 
    content = f.read()
    print(content)
```

**写入文件内容：**
```python
with open("output.txt", "w") as f:
    f.write("Hello, World!")
```

**逐行读取文件内容：**
```python
with open("example.txt", "r") as f:
    for line in f:
        print(line)
```

```python
# 以读取模式打开文件
file = open('example.txt', 'r')
content = file.read()
print(content)
file.close()

# 以写入模式打开文件
file = open('output.txt', 'w')
file.write('Hello, world!')
file.close()

# 以追加模式打开文件
file = open('output.txt', 'a')
file.write('\nAppending more content!')
file.close()

with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
# 文件在退出 with 代码块后会自动关闭

```

请注意，在使用 `open()` 函数操作文件时，通常使用 `with` 语句来确保文件在使用完毕后会被正确关闭。

这样可以避免资源泄漏问题。文件对象提供了许多其他方法，例如 `readlines()`、`writelines()` 等，用于不同的文件操作需求。

### 18.3.3 文件技巧

| 功能                 | 函数                                                         |
| :------------------- | :----------------------------------------------------------- |
| 使用with语句         | with open('file.txt', 'r') as file:<br/>    content = file.read() |
| 指定文件编码         | with open('file.txt', 'r', encoding='utf-8') as file:<br/>    content = file.read() |
| 读取大文件           | with open('large_file.txt', 'r') as file:<br/>    for line in file:<br/>process_line(line) |
| 读取二进制文件(音频) | with open('image.jpg', 'rb') as file:<br/>    image_data = file.read() |
| 写入二进制文件       | with open('output.bin', 'wb') as file:<br/>    file.write(binary_data) |
| 异常处理             | try:<br/>    with open('file.txt', 'r') as file:<br/>        content = file.read()<br/>except FileNotFoundError:<br/>    print("File not found.")<br/>except PermissionError:<br/>    print("Permission denied.") |
| 使用readlines( )     | with open('file.txt', 'r') as file:<br/>    lines = file.readlines() |
| 使用writelines( )    | lines = ['Line 1\n', 'Line 2\n', 'Line 3\n']<br/>with open('output.txt', 'w') as file:<br/>    file.writelines(lines) |
| 移动文件指针         | with open('file.txt', 'r') as file:<br/>    content = file.read(100)  # 读取前100个字符<br/>    position = file.tell()    # 获取当前指针位置<br/>    file.seek(0)              # 将指针移动到文件开头 |
| 缓冲区               | with open('file.txt', 'r', buffering=1) as file:<br/>    content = file.read()  # 行缓冲模式 |
| 内容覆盖             | with open('file.txt', 'r+') as file:<br/>    file.truncate(0)  # 清空文件内容<br/>    file.write('New content') |
| 文件路径             | import os<br/><br/>   file_path = 'path/to/file.txt'<br/>   file_name = os.path.basename(file_path)<br/>   is_exists = os.path.exists(file_path) |
| 删除文件             | import os<br/>os.remove('file.txt')                          |
| 移动和重命名         | import os<br/>   import shutil<br/><br/>   os.rename('old.txt', 'new.txt')<br/>   shutil.move('file.txt', 'new_location/') |
| 复制文件             | import shutil<br/><br/>   shutil.copy('file.txt', 'copy_of_file.txt') |
| 获取文件信息         | import os<br/><br/>   file_info = os.stat('file.txt')<br/>   print("Size:", file_info.st_size, "bytes") |
| 临时文件             | import tempfile<br/><br/>   with tempfile.TemporaryFile() as temp_file:<br/>       temp_file.write(b"Temporary data") |
|                      |                                                              |
|                      |                                                              |



当使用 Python 中的 `open()` 函数来操作文件时，还有一些辅助函数可以帮助您更方便地处理文件操作。以下是一些常见的辅助函数和技巧：

1. **使用 `with` 语句：** 如前所述，使用 `with` 语句可以确保文件在使用完毕后被正确关闭，无需手动调用 `close()` 方法。这是一个非常重要的技巧，可以避免资源泄漏问题。

   ```python
   with open('file.txt', 'r') as file:
       content = file.read()
   # 文件会在这里自动关闭，无需调用 close()
   ```

2. **指定文件编码：** 在使用 `open()` 函数时，可以指定文件的编码，特别是在处理包含非ASCII字符的文本文件时。

   ```python
   with open('file.txt', 'r', encoding='utf-8') as file:
       content = file.read()
   ```

3. **读取大文件：** 如果需要处理大文件，避免一次性读取整个文件内容，可以逐行读取，或者使用迭代器的方式。

   ```python
   with open('large_file.txt', 'r') as file:
       for line in file:
           process_line(line)
   ```

4. **使用 `readlines()`：** `readlines()` 方法可以将文件的每一行读取为一个字符串，并返回一个列表。通常在处理文件的每一行时使用。

   ```python
   with open('file.txt', 'r') as file:
       lines = file.readlines()
   ```

5. **使用 `writelines()`：** `writelines()` 方法可以将一个字符串列表写入文件，每个字符串作为一个行。需要注意手动添加换行符。

   ```python
   lines = ['Line 1\n', 'Line 2\n', 'Line 3\n']
   with open('output.txt', 'w') as file:
       file.writelines(lines)
   ```

6. **读取二进制文件：** 使用 `'rb'` 模式打开文件可以读取二进制文件，如图像、音频等。

   ```python
   with open('image.jpg', 'rb') as file:
       image_data = file.read()
   ```

7. **写入二进制文件：** 使用 `'wb'` 模式打开文件可以写入二进制文件。

   ```python
   with open('output.bin', 'wb') as file:
       file.write(binary_data)
   ```

8. **异常处理：** 在使用 `open()` 函数时，要考虑文件可能不存在、权限问题等情况，可以使用异常处理来捕获这些问题。

   ```python
   try:
       with open('file.txt', 'r') as file:
           content = file.read()
   except FileNotFoundError:
       print("File not found.")
   except PermissionError:
       print("Permission denied.")
   ```

9. **使用 `seek()` 和 `tell()`：** `seek(offset, whence)` 可以移动文件指针到指定位置，`tell()` 可以返回当前文件指针的位置。


   ```python
   with open('file.txt', 'r') as file:
       content = file.read(100)  # 读取前100个字符
       position = file.tell()    # 获取当前指针位置
       file.seek(0)              # 将指针移动到文件开头
   ```

11. **缓冲区控制：** 可以使用 `buffering` 参数来控制读取或写入的缓冲行为。默认情况下，文件使用默认的缓冲行为，但您可以通过设置 `buffering=0`（无缓冲）或 `buffering=1`（行缓冲）来调整。

   ```python
   with open('file.txt', 'r', buffering=1) as file:
       content = file.read()  # 行缓冲模式
   ```

12. **文件截断：** 在写入文件时，如果希望将文件内容截断（清空）然后再写入，可以使用 `truncate()` 方法。

   ```python
   with open('file.txt', 'r+') as file:
       file.truncate(0)  # 清空文件内容
       file.write('New content')
   ```

13. **使用 `os.path` 模块：** 如果需要操作文件路径，可以使用 `os.path` 模块来处理路径的操作，例如拼接路径、获取文件名、判断路径是否存在等。

   ```python
   import os

   file_path = 'path/to/file.txt'
   file_name = os.path.basename(file_path)
   is_exists = os.path.exists(file_path)
   ```

15. **使用 `io` 模块：** Python 还提供了 `io` 模块，该模块提供了更丰富的文件对象，可用于处理文本和二进制文件。

   ```python
   import io

   with io.open('file.txt', 'r', encoding='utf-8') as file:
       content = file.read()
   ```



29. **删除文件：** 使用`os.remove()`函数可以删除文件。

   ```python
   import os
   os.remove('file.txt')
   ```

32. **移动和重命名文件：** 使用`os.rename()`函数可以重命名文件，使用`shutil.move()`可以移动文件到另一个目录。

   ```python
   import os
   import shutil

   os.rename('old.txt', 'new.txt')
   shutil.move('file.txt', 'new_location/')
   ```

33. **复制文件：** 使用`shutil.copy()`可以复制文件到指定目录。

   ```python
   import shutil

   shutil.copy('file.txt', 'copy_of_file.txt')
   ```

34. **获取文件信息：** 使用`os.stat()`函数可以获取文件的详细信息，如大小、修改时间等。

   ```python
   import os

   file_info = os.stat('file.txt')
   print("Size:", file_info.st_size, "bytes")
   ```

35. **创建临时文件：** 使用`tempfile`模块可以创建临时文件，这些文件在使用后会被自动删除。

   ```python
   import tempfile

   with tempfile.TemporaryFile() as temp_file:
       temp_file.write(b"Temporary data"
   ```

# 十九 、时间和日历

## 19.1 时间

### 19.1.1 时间元组

时间元组（time tuple）是 Python 中用于表示时间的一种数据结构，通常使用一个包含年、月、日、时、分、秒等时间信息的元组来表示。时间元组是不可变的，其结构为：

```python
(time_year, time_month, time_day, time_hour, time_minute, time_second, time_weekday, time_yearday, time_isdst)
```

其中：

|     字段     |                 描述                 |         范围          |
| :----------: | :----------------------------------: | :-------------------: |
|  time_year   |                 年份                 |        4位数字        |
|  time_month  |                 月份                 |        1 到 12        |
|   time_day   |                  日                  |        1 到 31        |
|  time_hour   |                 小时                 |        0 到 23        |
| time_minute  |                 分钟                 |        0 到 59        |
| time_second  |                  秒                  |        0 到 59        |
| time_weekday |                星期几                | 0（周一）到 6（周日） |
| time_yearday |             年内的第几天             |       1 到 366        |
|  time_isdst  | 是否为夏令时（Daylight Saving Time） |      -1、0 或 1       |

您可以使用 Python 的 `time` 模块来获取当前时间的时间元组：

```python
import time

current_time_tuple = time.localtime()
print(current_time_tuple)
```

注意，时间元组的月份范围是 1 到 12，星期范围是 0 到 6，因此需要根据实际情况进行转换。此外，时间元组中的其他字段在某些情况下可能会是 -1 或其他特殊值。



### 19.1.2 时间函数



- **time模块**

  ```python
  >>> import time
  >>> dir(time)
  ['_STRUCT_TM_ITEMS', '__doc__', '__loader__', '__name__', '__package__', '__spec__', 'altzone', 'asctime', 'ctime', 'daylight', 'get_clock_info', 'gmtime', 'localtime', 'mktime', 'monotonic', 'monotonic_ns', 'perf_counter', 'perf_counter_ns', 'process_time', 'process_time_ns', 'sleep', 'strftime', 'strptime', 'struct_time', 'time', 'time_ns', 'timezone', 'tzname', 'tzset']
  ```

  - 下面是关于时间模块（`time` 模块）中的常用函数和属性的列表：

    | 名称             | 描述                                               |
    | :--------------- | :------------------------------------------------- |
    | _STRUCT_TM_ITEMS | 与 `struct_time` 相关的字段的索引                  |
    | altzone          | 当前地点的非夏令时时区的UTC偏移（单位为秒）        |
    | asctime          | 将 `struct_time` 对象转换为可读的字符串形式        |
    | ctime            | 将时间戳转换为可读的字符串形式                     |
    | daylight         | 是否启用夏令时，如果启用为非零，否则为0            |
    | get_clock_info   | 获取系统时钟的信息                                 |
    | gmtime           | 将时间戳转换为UTC时间的 `struct_time` 对象         |
    | localtime        | 将时间戳转换为本地时间的 `struct_time` 对象        |
    | mktime           | 将 `struct_time` 对象转换为时间戳                  |
    | monotonic        | 返回一个单调递增的时钟时间，用于测量时间间隔       |
    | monotonic_ns     | 类似于 `monotonic`，但以纳秒为单位                 |
    | perf_counter     | 返回一个性能计数器的值，用于测量短时间间隔         |
    | perf_counter_ns  | 类似于 `perf_counter`，但以纳秒为单位              |
    | process_time     | 返回进程运行时间（包括睡眠时间），用于性能分析     |
    | process_time_ns  | 类似于 `process_time`，但以纳秒为单位              |
    | sleep            | 使程序休眠指定的时间                               |
    | strftime         | 格式化 `struct_time` 对象为字符串                  |
    | strptime         | 解析字符串为 `struct_time` 对象                    |
    | struct_time      | 表示时间的元组结构                                 |
    | time             | 获取当前时间戳                                     |
    | time_ns          | 类似于 `time`，但以纳秒为单位                      |
    | timezone         | 当前地点的时区的UTC偏移（单位为秒）                |
    | tzname           | 当前地点的标准时区和夏令时时区的名称               |
    | tzset            | 根据操作系统环境设置 `tzname` 和 `timezone` 等属性 |

- **datetime 模块**

  - 下面是 `datetime` 模块的属性和类的表格总结：

    | 属性/类         | 描述                                                   |
    | --------------- | ------------------------------------------------------ |
    | `MAXYEAR`       | `datetime` 支持的最大年份常量。                        |
    | `MINYEAR`       | `datetime` 支持的最小年份常量。                        |
    | `__all__`       | 应该被导入的公共符号的名称列表。                       |
    | `__builtins__`  | 内置命名空间，包含内置函数、异常等。                   |
    | `__cached__`    | 缓存的模块文件的路径。                                 |
    | `__doc__`       | 模块的文档字符串。                                     |
    | `__file__`      | 模块文件的路径。                                       |
    | `__loader__`    | 加载器对象，用于加载模块。                             |
    | `__name__`      | 模块的名称。                                           |
    | `__package__`   | 模块的包名。                                           |
    | `__spec__`      | 模块的规范，包含有关模块的信息。                       |
    | `date`          | 日期对象类，表示年、月、日。                           |
    | `datetime`      | 日期时间对象类，表示日期和时间的组合。                 |
    | `time`          | 时间对象类，表示时、分、秒、微秒。                     |
    | `timedelta`     | 时间差对象类，表示两个日期或时间之间的差异。           |
    | `timezone`      | 时区对象类，表示时区的基本信息。                       |
    | `tzinfo`        | 时区信息对象类，提供有关特定时区的详细信息。           |
    | `datetime_CAPI` | C语言API的文档，通常不会在Python代码中使用。           |
    | `sys`           | Python 内置的 `sys` 模块，提供与系统交互的函数和属性。 |

  

  

  - 下面是 `datetime` 模块的属性和类按照功能分类的总结：

    **时间和日期类：**
    | 属性/类     | 描述                                         |
    | ----------- | -------------------------------------------- |
    | `date`      | 日期对象类，表示年、月、日。                 |
    | `datetime`  | 日期时间对象类，表示日期和时间的组合。       |
    | `time`      | 时间对象类，表示时、分、秒、微秒。           |
    | `timedelta` | 时间差对象类，表示两个日期或时间之间的差异。 |
    | `timezone`  | 时区对象类，表示时区的基本信息。             |
    | `tzinfo`    | 时区信息对象类，提供有关特定时区的详细信息。 |

    **常量和属性：**
    | 属性/类        | 描述                                 |
    | -------------- | ------------------------------------ |
    | `MAXYEAR`      | `datetime` 支持的最大年份常量。      |
    | `MINYEAR`      | `datetime` 支持的最小年份常量。      |
    | `__all__`      | 应该被导入的公共符号的名称列表。     |
    | `__builtins__` | 内置命名空间，包含内置函数、异常等。 |
    | `__cached__`   | 缓存的模块文件的路径。               |
    | `__doc__`      | 模块的文档字符串。                   |
    | `__file__`     | 模块文件的路径。                     |
    | `__loader__`   | 加载器对象，用于加载模块。           |
    | `__name__`     | 模块的名称。                         |
    | `__package__`  | 模块的包名。                         |
    | `__spec__`     | 模块的规范，包含有关模块的信息。     |

    **其他：**
    | 属性/类         | 描述                                                   |
    | --------------- | ------------------------------------------------------ |
    | `datetime_CAPI` | C语言API的文档，通常不会在Python代码中使用。           |
    | `sys`           | Python 内置的 `sys` 模块，提供与系统交互的函数和属性。 |





### 19.1.3 获取当前时间

- time()       获取当前时间戳（1970年1.1至今 以秒为单位）

  - ```python
    import time
    
    ct = time.time()
    print(ct)
    
    # 1691024836.86139
    ```

- ctime()     获取 **可读** 的当前时间

  - ```python
    import time
    
    ct = time.time()
    cr_ct = time.ctime(ct)
    print(cr_ct)
    
    # Thu Aug  3 09:10:00 2023
    ```

- localtime()  获取时间元组

  - ```python
    import time
    
    local_time = time.localtime()
    print("本地时间元组：", local_time)
    print('年', local_time.tm_year)
    print('月', local_time.tm_mon)
    print("日：", local_time.tm_mday)
    print("时：", local_time.tm_hour)
    print("分：", local_time.tm_min)
    print("秒：", local_time.tm_sec)
    
    
    本地时间元组： time.struct_time(tm_year=2023, tm_mon=8, tm_mday=3, tm_hour=9, tm_min=13, tm_sec=51, tm_wday=3, tm_yday=215, tm_isdst=0)
    年 2023
    月 8
    日： 3
    时： 9
    分： 13
    秒： 51
    
    ```

    

- asctime()  将时间元组 转化成字符串形式 

  - ```python
    import time
    
    local_time = time.localtime()
    a_t = time.asctime(local_time)
    print(a_t)
    
    #Thu Aug  3 09:23:06 2023
    ```

    

- datetime()   获取当前时间

  - ```python
    import datetime
    
    c_t = datetime.datetime.now()
    
    print(c_t)
    
    #2023-08-03 09:38:05.833396
    ```

- gmtime () utc 时间

  - ```python
    import time
    
    c_t = time.gmtime()
    cr_c_t = time.asctime(c_t)
    
    print(cr_c_t)
    
    #Thu Aug  3 01:43:52 2023
    ```

    

### 19.1.4 格式化时间

- 规则

  - | 占位符 | 含义              | 示例                     |
    | ------ | ----------------- | ------------------------ |
    | `%Y`   | 四位数的年份      | 2023                     |
    | `%y`   | 两位数的年份      | 23                       |
    | `%m`   | 月份（01 到 12）  | 08                       |
    | `%d`   | 日期（01 到 31）  | 02                       |
    | `%H`   | 小时（00 到 23）  | 10                       |
    | `%M`   | 分钟（00 到 59）  | 45                       |
    | `%S`   | 秒（00 到 59）    | 30                       |
    | `%A`   | 星期的完整名称    | Monday                   |
    | `%a`   | 星期的简写名称    | Mon                      |
    | `%B`   | 月份的完整名称    | January                  |
    | `%b`   | 月份的简写名称    | Jan                      |
    | `%c`   | 日期和时间的表示  | Tue Aug  2 10:45:30 2023 |
    | `%x`   | 仅日期的表示      | 08/02/23                 |
    | `%X`   | 仅时间的表示      | 10:45:30                 |
    | `%%`   | 表示一个 '%' 字符 | %                        |

- `strftime()`         字符串转换成时间     

  - ```python
    import time
    
    c_t = time.localtime()
    f_c_t = time.strftime('%Y-%m', c_t)
    print(f_c_t)
    
    # 2023-08
    ```

- `strptime()`         时间转成字符串

  

  - ```python
    import time
    
    Time_Str = '2020-11-1 12:10:30'
    Str_C_time = time.strptime(Time_Str, "%Y-%m-%d %H:%M:%S")
    print(Str_C_time)
    
    
    # time.struct_time(tm_year=2020, tm_mon=11, tm_mday=1, tm_hour=12, tm_min=10, tm_sec=30, tm_wday=6, tm_yday=306, tm_isdst=-1)
    ```

### 19.1.4 总结

| 函数                    | 生成类型       | 后续操作                                                     | 功能                     |
| ----------------------- | -------------- | ------------------------------------------------------------ | ------------------------ |
| time.time()             | 时间戳         | time.ctime(timeself) 转为可读                                | 获取当前时间戳           |
| time.localtime          | 时间元组       | time.asctime(timeself) 转化为可读<br>time.strftime('%Y-%m-%d-%H:%M:%S',timeself)            转化为可读 | 获取当前时间的时间元组   |
| datetime.datetime.now() | 可读格式化时间 |                                                              | 获取当前时间的格式化形式 |
| time.gmtime()           | 时间元组       | time.asctime(timeself) 转化为可读<br/>time.strftime('%Y-%m-%d-%H:%M:%S',timeself)            转化为可读 | 获取当前UTC时间          |



## 19.2 日历

```python
>>> import calendar

>>> dir(calendar)

['Calendar', 'EPOCH', 'FRIDAY', 'February', 'HTMLCalendar', 'IllegalMonthError', 'IllegalWeekdayError', 'January', 'LocaleHTMLCalendar', 'LocaleTextCalendar', 'MONDAY', 'SATURDAY', 'SUNDAY', 'THURSDAY', 'TUESDAY', 'TextCalendar', 'WEDNESDAY', '_EPOCH_ORD', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '_colwidth', '_locale', '_localized_day', '_localized_month', '_monthlen', '_nextmonth', '_prevmonth', '_spacing', 'c', 'calendar', 'datetime', 'day_abbr', 'day_name', 'different_locale', 'error', 'firstweekday', 'format', 'formatstring', 'isleap', 'leapdays', 'main', 'mdays', 'month', 'month_abbr', 'month_name', 'monthcalendar', 'monthrange', 'prcal', 'prmonth', 'prweek', 'repeat', 'setfirstweekday', 'sys', 'timegm', 'week', 'weekday', 'weekheader']
```



下面是对`calendar`模块中列出的各个属性、类和函数的详细解释：

- `Calendar`：基础的日历类，提供了生成日历的基本功能。

- `EPOCH`：一个元组，表示UNIX时间戳的起始时间。

- `FRIDAY`、`SATURDAY`、`SUNDAY`、`THURSDAY`、`TUESDAY`、`WEDNESDAY`：这些是表示星期几的常量。

- `February`、`January`：这些是表示月份的常量。

- `HTMLCalendar`：HTML格式的日历类，用于生成包含HTML标记的日历。

- `IllegalMonthError`、`IllegalWeekdayError`：自定义的异常类，用于处理不合法的月份和星期。

- `LocaleHTMLCalendar`、`LocaleTextCalendar`：本地化的HTML和文本日历类，可以生成基于不同地区设置的日历。

- `MONDAY`：表示星期一的常量。

- `TextCalendar`：文本格式的日历类，用于生成纯文本格式的日历。

- `_EPOCH_ORD`：UNIX时间戳的起始日期，表示为一年中的第几天。

- `__all__`：一个列表，包含了`calendar`模块中所有导出的对象的名称。

- `_colwidth`、`_locale`、`_localized_day`、`_localized_month`、`_monthlen`、`_nextmonth`、`_prevmonth`、`_spacing`：这些是模块内部使用的变量，用于控制日历的显示和布局。

- `c`：一个别名，用于创建`TextCalendar`对象。

- `calendar`：生成各种类型的日历的主要函数。

- `datetime`：处理日期和时间的模块。

- `day_abbr`、`day_name`：包含星期的缩写和全名。

- `different_locale`：内部函数，根据指定区域设置生成本地化的日历。

- `error`：自定义异常类，用于处理日历模块中的异常。

- `firstweekday`：表示一周的第一天是星期几的属性。

- `format`、`formatstring`：内部使用的格式化字符串。

- `isleap`：判断给定年份是否为闰年。

- `leapdays`：返回在两个年份之间的闰年的个数。

- `mdays`：包含每个月的天数的元组。

- `month`、`month_abbr`、`month_name`：返回一个多行字符串格式的月历。

- `monthcalendar`：返回一个表示给定年份和月份的月历的嵌套列表。

- `monthrange`：返回一个元组，表示给定年份和月份的第一天是星期几，以及该月的天数。

- `prcal`、`prmonth`、`prweek`：用于打印指定年份、月份、星期的日历。

- `repeat`：用于重复一个序列的迭代器。

- `setfirstweekday(weekday)`：设置一周的第一天是星期几。

- `sys`：与Python解释器和运行时环境交互的模块。

- `timegm`：类似于`time.gmtime()`，但返回UNIX时间戳。

- `week`：用于生成一个星期的日期。

- `weekday(year, month, day)`：返回指定日期的星期几。

- `weekheader(n)`：返回一个包含指定长度的星期头字符串。



下面是对`calendar`模块中列出的各个属性、类和函数的分类总结，并转换成表格：

| 分类     | 对象或函数                                                   | 描述                                                   |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------ |
| 常量     | EPOCH, FRIDAY, SATURDAY, SUNDAY, THURSDAY, TUESDAY, WEDNESDAY, February, January, ... | 表示日期、星期、月份等的常量。                         |
| 异常     | IllegalMonthError, IllegalWeekdayError, error                | 自定义异常类，用于处理不合法的月份和星期。             |
| 类       | Calendar, TextCalendar, HTMLCalendar, LocaleTextCalendar, LocaleHTMLCalendar | 生成不同格式和本地化的日历类。                         |
| 函数     | calendar, setfirstweekday, timegm, isleap, leapdays, monthcalendar, monthrange, ... | 生成、操作和处理日历的函数。                           |
| 属性     | day_abbr, day_name, mdays, firstweekday                      | 包含星期缩写、星期全名、月份天数、一周的第一天等属性。 |
| 内部变量 | _colwidth, _locale, _localized_day, _localized_month, _monthlen, _nextmonth, _prevmonth, _spacing | 控制日历布局和显示的内部变量。                         |
| 时间处理 | datetime, datetime_CAPI                                      | 用于处理日期和时间的模块和内部函数。                   |
| 辅助函数 | different_locale, format, formatstring, repeat               | 内部使用的辅助函数，用于格式化和重复迭代。             |
| 打印函数 | prcal, prmonth, prweek                                       | 打印日历的函数，用于输出日历信息。                     |
| 系统交互 | sys, _EPOCH_ORD                                              | 与Python解释器和运行时环境交互的模块和变量。           |

请注意，以上表格只是对`calendar`模块中的一些重要对象、函数和属性进行了分类总结，并不包含所有内容。



在Python中，使用`calendar`模块可以进行日历相关的操作。下面是一些常见的日历操作示例：

```python
import calendar

# 获取指定年份的整个年历
year_calendar = calendar.calendar(2023)
print(year_calendar)

# 获取指定年份和月份的日历
month_calendar = calendar.month(2023, 8)
print(month_calendar)

# 获取指定年份和月份的日历，以嵌套列表形式
month_matrix = calendar.monthcalendar(2023, 8)
print(month_matrix)

# 获取指定年份和月份的第一天是星期几和该月的总天数
first_weekday, total_days = calendar.monthrange(2023, 8)
print("First weekday:", first_weekday)  # 2代表星期三
print("Total days:", total_days)

# 判断指定年份是否为闰年
is_leap = calendar.isleap(2023)
print("Is leap year:", is_leap)

# 获取在指定年份范围内的闰年数量
leap_years = calendar.leapdays(2000, 2023)
print("Leap years:", leap_years)

# 设置一周的第一天为周一
calendar.setfirstweekday(calendar.MONDAY)

# 获取指定日期的星期几
weekday = calendar.weekday(2023, 8, 2)  # 0代表周一
print("Weekday:", weekday)
```

这些示例展示了如何使用`calendar`模块来进行日历相关的操作，包括获取年历、月历、判断闰年、计算闰年数量、设置周的第一天和获取星期几等功能。

## 19.3 程序计时

- `time.sleep()`

  - 在Python中，`time`模块还提供了一个`sleep()`函数，可以用于让程序暂停执行一段时间，模拟等待或延时操作。`sleep()`函数接受一个参数，表示要暂停的时间（以秒为单位）。以下是一个示例：

    ```python
    import time
    
    print("Start")
    time.sleep(2)  # 暂停2秒
    print("End")
    ```

    在这个示例中，程序会打印"Start"，然后暂停2秒，最后再打印"End"。这就是使用`sleep()`函数来实现程序暂停执行的效果。这在一些需要控制程序流程，或者需要在某些情况下引入延时的场景中非常有用。需要注意的是，`sleep()`函数可能会引入阻塞，所以在某些情况下需要谨慎使用，以免影响程序的响应性。

- `perf_counter()`

  - Python 中的 `perf_counter` 函数。是位于 `time` 模块中的函数，用于性能测量和计时。`perf_counter` 返回一个高精度的时间戳，通常用于测量代码块的执行时间。

    下面是 `perf_counter` 的简单用法示例：

    ```python
    import time
    
    # 记录起始时间
    start_time = time.perf_counter()
    
    # 执行一些代码或操作
    for _ in range(1000000):
        _ = 2 * 2
    
    # 记录结束时间
    end_time = time.perf_counter()
    
    # 计算代码执行时间
    execution_time = end_time - start_time
    print("Execution time:", execution_time, "seconds")
    ```

    在这个例子中，`start_time` 和 `end_time` 分别记录了代码块的起始和结束时间，然后通过计算它们的差值得到了代码的执行时间。

    `perf_counter` 提供了高分辨率的时间计数，适用于测量短暂的时间间隔，例如性能测试和代码优化的时候。







# 二十 、面向对象

Python 是一种支持面向对象编程（OOP）范式的编程语言。在面向对象编程中，程序被组织成对象的集合，每个对象都具有数据和操作数据的方法。这有助于提高代码的可维护性、可重用性和可扩展性。

以下是 Python 中面向对象编程的基本概念和要素：

| 概念                                        | 解释                                                         |
| ------------------------------------------- | ------------------------------------------------------------ |
| 类（Class）                                 | 用于创建对象的蓝图，定义了对象的属性和方法。                 |
| 对象（Object）                              | 类的实例，具有特定数据和方法。                               |
| 属性（Attribute）                           | 类中的变量，用于存储对象的状态。                             |
| 方法（Method）                              | 类中的函数，用于操作对象的数据和实现对象的行为。             |
| 封装（Encapsulation）                       | 封装将数据和方法组合到一个单元中，隐藏了内部实现细节，只暴露必要的接口。 |
| 继承（Inheritance）                         | 子类可以从父类继承属性和方法，促进了代码重用和层次化的结构。 |
| 多态（Polymorphism）                        | 不同的类可以实现相同的方法名称，但具有不同的实现，允许以统一的方式处理不同类的对象。 |
| 构造函数（Constructor）                     | 初始化对象的特性和状态，通常在对象创建时调用。               |
| 成员变量（Instance Variable）               | 对象特有的变量，存储在类的实例中，每个对象有自己的副本。     |
| 类变量（Class Variable）                    | 类共享的变量，存储在类本身中，被所有实例共享。               |
| 调用父类方法（Calling Parent Class Method） | 子类中可以通过 super() 调用父类的方法。                      |

## 20.1 基本概念

### 20.1.1 类和对象



- **类（Class）和对象（Object）示例：**

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

car1 = Car("Toyota", "Camry")
car2 = Car("Honda", "Civic")
```

​		在这个示例中，`Car` 是一个类，`car1` 和 `car2` 是从 `Car` 类创建的两个不同的对象。每个对象都有一个 `make` 属性和一个 `model` 属性。

### 20.1.2 属性和方法



​		**属性（Attribute）和方法（Method）示例：**



```python
class Circle:
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2

circle = Circle(5)
print(circle.radius)  # 输出 5
print(circle.area())  # 输出 78.53975
```

​			在这个示例中，`Circle` 类有一个 `radius` 属性和一个 `area` 方法。`area` 方法用于计算圆的面积，基于 `radius` 属性的值。



​			`self` 是面向对象编程中的一个非常重要的概念，它用于在类的方法内部引用当前对象的实例。理解 `self` 的作用对于正确使用类和对象以及实现面向对象编程的核心思想至关重要。

在 Python 中，当你调用一个对象的方法时，Python 会自动传递该对象的引用作为第一个参数给方法。这个参数通常被称为 `self`，但实际上你可以使用任何合法的变量名。



**以下是 `self` 的作用：**





1. **访问属性：** 通过 `self`，你可以在类的方法内部访问对象的属性。这允许你在方法中使用和修改对象的状态。

2. **调用其他方法：** 使用 `self`，你可以在类的方法内部调用其他方法。这样可以促进代码的模块化和重用。

3. **区分不同实例：** 在类的方法内部，`self` 代表当前实例。这使得不同的实例可以具有不同的属性值，并且可以在方法中执行特定于实例的操作。

4. **初始化属性：** 在类的构造函数 `__init__` 中，使用 `self` 可以初始化实例的属性。它帮助你将输入参数赋值给对象的属性。

5. **创建对象：** 在类中，通过 `self` 可以引用正在创建的对象。这使得你可以在初始化过程中设置对象的属性。

下面是一个更详细的示例来解释 `self` 的作用：

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def introduce(self):
        return f"My name is {self.name} and I am {self.age} years old."

person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

print(person1.introduce())  # 输出 "My name is Alice and I am 30 years old."
print(person2.introduce())  # 输出 "My name is Bob and I am 25 years old."
```

在这个示例中，`self` 在 `__init__` 构造函数和 `introduce` 方法中使用。在构造函数中，`self` 帮助我们初始化 `name` 和 `age` 属性。在 `introduce` 方法中，`self` 允许我们在返回介绍的字符串时引用对象的属性。

总之，`self` 是面向对象编程中用于引用当前对象实例的特殊参数。它允许你在类的方法内部操作和访问对象的属性，以及在方法之间建立联系。

### 20.1.3 封装

**封装（Encapsulation）示例：**



```python
class BankAccount:
    def __init__(self):
        self.balance = 0
    
    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
    
    def withdraw(self, amount):
        if 0 < amount <= self.balance:
            self.balance -= amount

account = BankAccount()
account.deposit(1000)
account.withdraw(500)
print(account.balance)  # 输出 500
```

​		在这个示例中，`BankAccount` 类封装了账户余额，`deposit` 和 `withdraw` 方法用于操作余额。这样可以确保只有合法操作可以改变账户的余额。





### 20.1.4 继承

以下是单继承和多继承的对比，转化为表格形式：

| 特性       | 单继承                             | 多继承                             |
| ---------- | ---------------------------------- | ---------------------------------- |
| 定义       | 一个类继承自一个基类               | 一个类可以同时继承多个基类         |
| 类之间关系 | 简单线性关系                       | 类之间的关系可以更加灵活           |
| 优点       | 层次结构清晰，维护简单             | 可以从多个基类中继承不同的功能     |
| 缺点       | 代码复用受限，无法同时继承多个基类 | 可能引发命名冲突和继承链复杂性     |
| 方法冲突   | 不会产生方法冲突                   | 可能产生方法冲突，需要处理命名冲突 |
| 代码可读性 | 较高，继承关系清晰                 | 可能降低代码可读性                 |
| 灵活性     | 较低，不能继承多个不同的功能       | 较高，可以创建具有多种特性的复杂类 |

单继承（Single Inheritance）：

单继承指的是一个类只能继承自一个基类（父类），每个子类只有一个直接父类。这种模式的特点是类之间的关系比较简单，继承链是线性的。

优点：
- 易于理解和维护，类的层次结构相对清晰。
- 避免了多继承可能引发的命名冲突和复杂性。

缺点：
- 无法直接从多个基类中继承不同的功能。
- 限制了代码复用，每个子类只能继承一个基类的功能。

继承（Multiple Inheritance）：

多继承指的是一个类可以同时继承自多个基类，从而继承多个基类的属性和方法。这种模式的特点是类之间的关系可以更灵活，但也可能引发一些复杂性和冲突问题。

优点：
- 可以从多个基类中继承不同的功能，实现更大的代码复用。
- 允许创建具有多种特性的复杂类。

缺点：
- 可能引发命名冲突，特别是在基类之间存在相同方法或属性名时。
- 多继承的继承链可能变得很复杂，导致代码可读性降低。
- 对于新手开发者来说，可能不易理解和维护。

Python 中允许多继承，但开发者需要注意避免潜在的问题，如方法冲突、继承链的混乱和代码可读性问题。在选择单继承还是多继承时，需要根据具体情况权衡利弊。在许多情况下，单继承可以提供更清晰、简单的类结构，而多继承则允许更大的灵活性和代码复用。



#### 20.1.4.1 单继承

```python
class Shape:
    def __init__(self, name):
        self.name = name
    
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, name, radius):
        super().__init__(name)
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2

circle = Circle("My Circle", 5)
print(circle.area())  # 输出 78.53975
```

​		

​		在这个示例中，`Circle` 类继承了 `Shape` 类，从而继承了 `name` 属性和 `area` 方法，

​		并根据自己的需要实现了自己的 `area` 方法。



我明白你想要一个更复杂的例子。让我们考虑一个虚拟的学校管理系统，其中有多个类以展示更多复杂的函数继承。

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def display_info(self):
        return f"Name: {self.name}, Age: {self.age}"

class Student(Person):
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id
    
    def display_info(self):
        return f"Student ID: {self.student_id}, {super().display_info()}"

class Teacher(Person):
    def __init__(self, name, age, employee_id):
        super().__init__(name, age)
        self.employee_id = employee_id
    
    def display_info(self):
        return f"Employee ID: {self.employee_id}, {super().display_info()}"

class Course:
    def __init__(self, course_name, teacher):
        self.course_name = course_name
        self.teacher = teacher
        self.students = []
    
    def add_student(self, student):
        self.students.append(student)
    
    def display_info(self):
        student_list = "\n".join([student.display_info() for student in self.students])
        return f"Course: {self.course_name}\nTeacher: {self.teacher.display_info()}\nStudents:\n{student_list}"

teacher = Teacher("John Smith", 35, "T123")
student1 = Student("Alice Johnson", 20, "S101")
student2 = Student("Bob Williams", 22, "S102")

math_course = Course("Mathematics", teacher)
math_course.add_student(student1)
math_course.add_student(student2)

print(math_course.display_info())
```

在这个示例中，我们有四个类：`Person`、`Student`、`Teacher` 和 `Course`。每个类都继承了父类的方法，并实现了自己的属性和行为。

1. `Person` 类是基类，表示一个人，包含姓名和年龄。
2. `Student` 类继承自 `Person`，表示学生，还有一个学生 ID。
3. `Teacher` 类继承自 `Person`，表示教师，还有一个员工 ID。
4. `Course` 类表示课程，包括课程名称、授课教师和学生列表。

在这个例子中，我们展示了如何使用函数继承来构建一个更复杂的系统，各个类之间通过继承建立关联，使得代码更有组织和可扩展性。

#### 20.1.4.2 多继承

以下是一个使用多继承的简单示例，展示了如何在 Python 中创建一个具有多个基类的子类：

```python
class Animal:
    def speak(self):
        pass

class Mammal(Animal):
    def feed_milk(self):
        pass

class Bird(Animal):
    def lay_eggs(self):
        pass

class Bat(Mammal, Bird):  ## Bat 类多重继承了 Animal类
    def speak(self):
        return "Screech!"

bat = Bat()
print(bat.speak())  # 输出 "Screech!"
bat.feed_milk()     # 可以调用 Mammal 类的方法
bat.lay_eggs()      # 可以调用 Bird 类的方法
```

在这个示例中，我们定义了三个基类：`Animal`、`Mammal` 和 `Bird`。然后，我们创建了一个名为 `Bat` 的子类，它同时继承自 `Mammal` 和 `Bird` 两个基类。

这样，`Bat` 类具有了 `Mammal` 和 `Bird` 两个基类的方法和属性。在调用 `speak()` 方法时，由于 `Bat` 类覆盖了 `speak()` 方法，所以返回了 "Screech!"。

需要注意的是，多继承的情况下可能会出现命名冲突或继承链复杂性的问题，因此在使用多继承时需要谨慎考虑。在实际应用中，应当根据代码的复杂性和可读性来决定是否使用多继承。





**继承的传递**  ： **多重继承**



是的，子类1继承子类2，而子类2继承了父类，那么子类1会继承子类2和父类的功能。这种继承关系被称为多层继承（Multilevel Inheritance）。在多层继承中，子类通过继承关系，可以获得它的直接父类和父类的所有功能。

让我们通过一个示例来说明这个概念：

```python
class Animal:
    def speak(self):
        return "Animal speaks"

class Mammal(Animal):
    def feed_milk(self):
        return "Mammal feeds milk"

class Dog(Mammal):
    def bark(self):
        return "Dog barks"

dog = Dog()

print(dog.speak())     # 输出 "Animal speaks"，来自 Animal 类
print(dog.feed_milk()) # 输出 "Mammal feeds milk"，来自 Mammal 类
print(dog.bark())      # 输出 "Dog barks"，来自 Dog 类
```

在这个示例中，`Dog` 类继承了 `Mammal` 类，而 `Mammal` 类继承了 `Animal` 类。因此，`Dog` 类不仅继承了自己的方法 `bark()`，还继承了 `Mammal` 类的方法 `feed_milk()` 和 `Animal` 类的方法 `speak()`。

这种多层继承使得子类能够在整个继承链中获得功能，但需要注意继承链过于复杂可能导致代码难以维护。因此，在设计继承关系时，需要考虑继承链的层次和复杂性，以确保代码的可读性和可维护性。

### 20.1.5 多态

​		**多态（Polymorphism）示例：**

​	

```python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

def animal_sound(animal):
    return animal.speak()

dog = Dog()
cat = Cat()

print(animal_sound(dog))  # 输出 "Woof!"
print(animal_sound(cat))  # 输出 "Meow!"
```

​		在这个示例中，`Animal` 类有一个 `speak` 方法，而 `Dog` 和 `Cat` 类都重写了 `speak` 方法。`animal_sound` 函数接受一个动物对象并调用它的 `speak` 方法，实现了多态性。





## 20.2  封装问题

### 20.2.1 封装

​		封装原则是面向对象编程中的一个重要概念，也是 SOLID 原则中的一部分。它指的是将对象的状态（属性）和行为（方法）包装在一个单元中，同时隐藏内部实现细节，只暴露必要的接口供外部访问。封装的目的是将对象的内部状态与外部世界隔离开，以提高代码的可维护性、安全性和可扩展性。

封装原则的核心思想包括：

* **隐藏实现细节：** 封装通过隐藏对象的内部实现细节，使外部代码不需要了解对象是如何实现的，只需要知道如何使用对象的公有接							口。
* **限制访问权限：** 通过访问修饰符（公有、保护、私有）来控制哪些成员可以在类外部访问，从而防止不受控制的外部访问和修改。
* **提供公有接口：** 封装通过提供公有方法来定义对象的操作接口，从而实现控制对内部状态的访问和修改。
* **隔离变化：** 封装使对象的内部实现细节与外部代码分离，当内部实现发生变化时，外部代码不受影响。

​		封装原则在面向对象编程中具有重要的意义，它有助于构建模块化、可维护和可扩展的代码。通过隐藏内部细节，封装可以减少意外的错误和代码的耦合度，同时提高了代码的安全性，因为外部代码无法直接操纵对象的状态。

​		总之，封装原则是面向对象编程的基石之一，它强调将数据和行为封装在一个单元中，通过明确定义的接口来控制对象的访问和操作。



### 20.2.2 私有属性、函数 继承

​		

​		在 Python 中，私有成员（包括属性和方法）是可以被继承的，但是在子类中仍然无法直接访问这些私有成员。这是因为 Python 使用名称重整（name mangling）来模拟私有性，使得私有成员的名称在编译时被改变，以防止在子类中意外覆盖父类的成员。

下面是一个示例，说明私有成员在继承中的行为：

```python
class Parent:
    def __init__(self):
        self.public_var = "I'm public"
        self.__private_var = "I'm private"
    
    def public_method(self):
        return "This is a public method"
    
    def __private_method(self):
        return "This is a private method"

class Child(Parent):
    def __init__(self):
        super().__init__()

child = Child()

print(child.public_var)          # 可以访问父类的公有属性
print(child.public_method())     # 可以调用父类的公有方法

# 以下代码会产生 AttributeError，因为子类不能直接访问父类的私有属性和方法
# print(child.__private_var)
# print(child.__private_method())
```

​		在这个示例中，`Parent` 类有一个公有属性 `public_var` 和一个私有属性 `__private_var`，以及一个公有方法 `public_method` 和一个私有方法 `__private_method`。子类 `Child` 继承了 `Parent` 类。

​		尝试直接访问 `child.__private_var` 或调用 `child.__private_method()` 会导致 AttributeError。这是因为私有成员在编译时被名称重整，变成了 `_Parent__private_var` 和 `_Parent__private_method`，所以在子类中的访问与父类中的定义不匹配。



* **继承公用函数调用私有类**



​		在Python中，子类无法直接访问父类的私有属性（包括私有属性和方法）。私有属性和方法在父类中经过名称重整，以在编译时防止子类直接访问。然而，你可以通过一些方式来间接地访问父类的私有成员，例如使用父类的公有方法来获取私有属性的值。

以下是一个示例，演示如何通过公有方法间接地访问父类的私有属性：

```python
class Parent:
    def __init__(self):
        self.__private_var = "Parent's private"
    
    def get_private_var(self):
        return self.__private_var

class Child(Parent):
    def __init__(self):
        super().__init__()

child = Child()

# 通过子类的公有方法间接访问父类的私有属性
private_var_value = child.get_private_var()
print(private_var_value)  # 输出 "Parent's private"
```

​		在这个示例中，`Parent` 类有一个私有属性 `__private_var`，并提供了一个公有方法 `get_private_var()` 来获取私有属性的值。子类 `Child` 继承了 `Parent` 类，并可以通过调用 `get_private_var()` 方法来间接访问父类的私有属性。

​		请注意，这种方式是通过公有接口访问私有成员，遵循了封装的原则。直接访问私有成员是不推荐的，因为它会破坏封装性和代码的安全性。



   * **私有函数** 
     * 在 Python 中，私有方法（以及属性）在名称前面加上两个下划线 `__`，这样的方法将被视为私有的，不能直接在类外部调用。然而，你可以通过一些技巧来间接地调用私有方法，尽管这样做不被推荐，因为它破坏了封装的原则。

​				下面是一种方式，可以通过类的实例来间接地调用私有方法：

```python
class MyClass:
    def __private_method(self):
        print("This is a private method")

    def call_private_method(self):
        self.__private_method()

obj = MyClass()
obj.call_private_method()  # 输出 "This is a private method"
```

​			在这个示例中，`MyClass` 类有一个私有方法 `__private_method`。为了在类外部调用它，我们创建了一个名为 `call_private_method` 的公有方法，内部调用了私有方法。通过调用公有方法，我们间接地调用了私有方法。

​			这种方式虽然可行，但并不推荐，因为它违反了封装的原则。私有方法被设计为仅在类的内部使用，直接或间接地在类外部调用都可能引起意外行为或错误。最好的做法是使用公有方法作为接口，以控制类的外部访问。

* 我理解你想要另一种方式来调用私有方法。在 Python 中，虽然不推荐直接调用私有方法，但你可以使用 `getattr()` 函数来实现间接调用

  * 以下是一个例子，演示如何使用 `getattr()` 来调用私有方法：

  ```python
  class MyClass:
      def __private_method(self):
          print("This is a private method")
  
  obj = MyClass()
  
  # 通过使用 getattr() 间接调用私有方法
  method_name = "_MyClass__private_method"
  method = getattr(obj, method_name)
  method()  # 输出 "This is a private method"
  ```

  在这个示例中，我们使用了 `getattr()` 函数来获取类实例的私有方法对象，然后通过调用这个对象来间接地调用私有方法。需要注意的是，这种方式依然违背了封装的原则，不推荐在实际代码中使用。

  请记住，私有方法是为了限制访问和防止外部直接调用，以确保类的内部实现细节不受破坏。最佳实践是在类中提供公有方法来进行操作，而不是绕过私有性。

 



### 20.2.3 保护属性

​			保护属性是一种访问修饰符，用于限制属性的访问范围。在Python中，通过在属性名前面加上一个下划线 `_` 来表示这个属性是受保护的。虽然Python并没有强制限制保护属性的访问，但这种约定告诉其他开发人员这些属性应该被视为类的内部实现细节，而不是公有接口。

​			保护属性具有以下特点：

* **命名约定：** 使用一个下划线 `_` 作为前缀，例如 `_protected_var`。
* **约定性访问：** 这种属性的命名约定告诉其他人这是一个受保护的属性，应该在类的内部使用。
* **限制性访问：** 在类的外部，保护属性可以被访问，但开发者应该尽量避免直接访问保护属性，而是使用公有方法进行操作。

​		下面是一个示例，展示了如何定义和使用保护属性：

```python
class MyClass:
    def __init__(self):
        self._protected_var = "This is a protected attribute"
    
    def display_protected(self):
        print(self._protected_var)

obj = MyClass()

# 在类的外部可以访问保护属性
print(obj._protected_var)  # 输出 "This is a protected attribute"

# 但最好使用类的公有方法来操作保护属性
obj.display_protected()    # 输出 "This is a protected attribute"
```

​		在这个示例中，`_protected_var` 是一个保护属性。尽管我们在类的外部可以访问它，但最好通过公有方法 `display_protected()` 来访问它，以保持封装性和安全性。

​		请注意，保护属性只是一种约定，而不是强制。**在Python中，没有真正的私有性或保护性，**因此开发者仍然可以在类的外部访问和修改保护属性。然而，遵循这种命名约定可以帮助保持代码的整洁性和可维护性。









# 二十一 、 正则表达式

## 21.1 正则

正则表达式（Regular Expression，简称正则或正规表达式）的主要目的是在文本中进行模式匹配、查找、替换和处理操作。它是一种强大的工具，用于在字符串中寻找满足特定模式的文本片段。正则表达式在文本处理、数据提取、验证和替换等任务中非常有用。

正则表达式的主要目的包括：

1. **模式匹配：** 正则表达式允许你定义一种模式，用于匹配文本中符合该模式的部分。例如，你可以使用正则表达式来匹配电子邮件地址、URL、日期等特定格式的文本。

2. **查找和提取：** 通过在文本中执行正则表达式搜索，你可以找到满足特定条件的子串。这对于从大量文本中提取特定信息非常有用，比如从日志中提取错误信息，从HTML中提取链接等。

3. **替换：** 正则表达式允许你在文本中查找满足特定模式的部分，并将其替换为其他内容。这对于批量修改文本、格式化数据等操作非常方便。

4. **验证和过滤：** 正则表达式可以用于验证输入是否符合特定的格式要求，如检查电话号码、邮政编码、密码等是否满足规定。

5. **分割：** 你可以使用正则表达式将文本分割成子串，比如将句子拆分成单词。

6. **清理和处理：** 正则表达式可以帮助你清理文本，去除不需要的空白、特殊字符等。

总之，正则表达式提供了一种强大的工具，用于处理各种文本处理任务。它可以在字符串中识别和操作模式，使得处理复杂的文本操作变得更加高效和便捷。无论是在编程中还是在文本编辑工具中，正则表达式都是一项非常有用的技能。



## 21.2 函数

```python
>>> import re

\>>> dir (re)

['A', 'ASCII', 'DEBUG', 'DOTALL', 'I', 'IGNORECASE', 'L', 'LOCALE', 'M', 'MULTILINE', 'Match', 'Pattern', 'RegexFlag', 'S', 'Scanner', 'T', 'TEMPLATE', 'U', 'UNICODE', 'VERBOSE', 'X', '_MAXCACHE', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '__version__', '_cache', '_compile', '_compile_repl', '_expand', '_locale', '_pickle', '_special_chars_map', '_subx', 'compile', 'copyreg', 'enum', 'error', 'escape', 'findall', 'finditer', 'fullmatch', 'functools', 'match', 'purge', 'search', 'split', 'sre_compile', 'sre_parse', 'sub', 'subn', 'template']
```

它们代表了 `re` 模块的各种功能和特性。以下是这些属性、类和函数的全部解释：

- `'A', 'ASCII'`: 正则表达式标志，用于匹配 ASCII 字符。

- `'DEBUG'`: 正则表达式标志，用于显示调试信息。

- `'DOTALL'`: 正则表达式标志，让 `.` 匹配任何字符，包括换行符。

- `'I', 'IGNORECASE'`: 正则表达式标志，用于在匹配时忽略大小写。

- `'L', 'LOCALE'`: 正则表达式标志，用于启用地区（locale）特定的行为。

- `'M', 'MULTILINE'`: 正则表达式标志，用于启用多行模式，影响 `^` 和 `$` 的行为。

- `'Match'`: `re` 模块中的一个类，表示匹配的结果。

- `'Pattern'`: `re` 模块中的一个类，表示编译的正则表达式模式。

- `'RegexFlag'`: `re` 模块中的一个类，表示正则表达式的标志。

- `'S', 'Scanner'`: 正则表达式标志，用于启用扫描模式。

- `'T', 'TEMPLATE'`: 正则表达式标志，用于启用模板匹配模式。

- `'U', 'UNICODE'`: 正则表达式标志，用于启用 Unicode 匹配。

- `'VERBOSE'`: 正则表达式标志，用于启用详细的正则表达式模式，允许包含空白和注释。

- `'X'`: 正则表达式标志，等同于 `VERBOSE`。

- `'_MAXCACHE'`: 内部缓存的大小。

- `'__all__'`: 模块中的公有属性列表。

- `'__builtins__'`: Python 内置命名空间。

- `'__cached__'`: 缓存的模块路径。

- `'__doc__'`: 模块的文档字符串。

- `'__file__'`: 模块的文件名。

- `'__loader__'`: 加载模块的加载器。

- `'__name__'`: 模块的名称。

- `'__package__'`: 包名。

- `'__spec__'`: 模块规范。

- `'__version__'`: `re` 模块的版本信息。

- `'_cache'`: 正则表达式缓存。

- `'_compile'`, `'_compile_repl'`, `'_expand'`, `'_locale'`, `'_pickle'`, `_special_chars_map`, `_subx`: 内部使用的辅助函数。

- `'compile'`: 函数，将正则表达式编译为模式对象。
  - <img src="python基础md配图/image-20230803184955869.png" alt="image-20230803184955869" style="zoom:50%;" />

- `'copyreg'`: Python 内部模块，用于支持对象的持久化存储。

- `'enum'`: 枚举类，用于表示正则表达式标志。

- `'error'`: 正则表达式模块的异常基类。

- `'escape'`: 函数，用于对字符串中的特殊字符进行转义。
  - <img src="python基础md配图/image-20230803183141503.png" alt="image-20230803183141503" style="zoom:50%;" />

- `'findall'`: 函数，查找字符串中所有匹配的子串，返回一个列表。

- `'finditer'`: 函数，返回一个迭代器，每次迭代返回一个匹配对象。

- `'fullmatch'`: 函数，尝试完全匹配整个字符串。

- `'functools'`: Python 内置模块，用于高阶函数和操作。

- `'match'`: 函数，尝试从字符串开头匹配正则表达式。

- `'purge'`: 函数，清除正则表达式缓存。
  - <img src="python基础md配图/image-20230803183039206.png" alt="image-20230803183039206" style="zoom:50%;" />

- `'search'`: 函数，用于在字符串中查找第一个匹配的子串。

- `'split'`: 函数，根据正则表达式将字符串分割成子串。

- `'sre_compile'`, `'sre_parse'`: 内部使用的正则表达式编译和解析函数。

- `'sub', 'subn'`: 函数，用于替换字符串中匹配的子串。

- `'template'`: 函数，用于创建模板正则表达式。
  - <img src="python基础md配图/image-20230803183211950.png" alt="image-20230803183211950" style="zoom:50%;" />




## 21.3 符号



下面是一个用表格表示常见的正则表达式符号和它们的含义：

| 符号     | 含义                                           |
| -------- | ---------------------------------------------- |
| `.`      | 匹配任意字符（除了换行符 `\n`）                |
| `*`      | 匹配前一个字符零次或多次                       |
| `+`      | 匹配前一个字符一次或多次                       |
| `?`      | 匹配前一个字符零次或一次                       |
| `[]`     | 定义字符集，匹配其中任意一个字符               |
| `()`     | 用于分组，可以对多个字符进行操作               |
| `|`      | 逻辑 OR，匹配其中一个表达式                    |
| `^`      | 匹配字符串的开头                               |
| `$`      | 匹配字符串的结尾                               |
| `\`      | 转义字符，用于匹配特殊字符本身                 |
| `\d`     | 匹配任意数字字符，等同于 `[0-9]`               |
| `\w`     | 匹配任意字母数字字符，等同于 `[a-zA-Z0-9_]`    |
| `\s`     | 匹配任意空白字符，包括空格、制表符、换行符等   |
| `\b`     | 匹配单词的边界                                 |
| `\D`     | 匹配任意非数字字符，等同于 `[^0-9]`            |
| `\W`     | 匹配任意非字母数字字符，等同于 `[^a-zA-Z0-9_]` |
| `\S`     | 匹配任意非空白字符                             |
| `\B`     | 匹配非单词边界                                 |
| `{n}`    | 匹配前一个字符恰好 n 次                        |
| `{n,}`   | 匹配前一个字符至少 n 次                        |
| `{n,m}`  | 匹配前一个字符至少 n 次，但不超过 m 次         |
| `[...]`  | 匹配方括号中的任意一个字符                     |
| `[^...]` | 匹配不在方括号中的任意字符                     |
| `(?i)`   | 在括号内启用忽略大小写的匹配                   |
| `(?m)`   | 在括号内启用多行模式                           |
| `(?s)`   | 在括号内启用 dot 匹配所有字符模式              |
| `(?x)`   | 在括号内启用详细模式，可以包含空格和注释       |



## 21.4 使用

- 模式匹配 comile  findall  

  - 正则模式匹配是指使用正则表达式来查找符合特定模式的文本片段。通过定义一个正则表达式，你可以指定要匹配的模式，然后在给定的文本中搜索匹配的内容。以下是正则模式匹配的基本步骤和示例：

    1. **定义正则表达式：** 首先，你需要定义一个正则表达式，这个表达式描述了你想要匹配的模式。正则表达式是由一系列字符和特殊符号组成的字符串，表示一种匹配规则。

    2. **编译正则表达式：** 在大多数编程语言中，你需要使用语言提供的正则表达式库来编译你的正则表达式。这将会把你的正则表达式编译成一个可供程序使用的内部数据结构。

    3. **执行匹配：** 一旦你编译了正则表达式，你可以使用它在给定的文本中进行匹配操作。根据你的需求，可以选择执行不同类型的匹配，如查找所有匹配、查找第一个匹配等。

    4. **获取匹配结果：** 匹配操作会返回一个或多个匹配对象，每个匹配对象包含了匹配到的文本片段以及关于匹配位置等信息。

    以下是一个示例，演示如何使用 Python 中的 `re` 模块进行正则模式匹配：

    ```python
    import re
    
    # 定义正则表达式模式
    pattern = r'\d{2}-\d{2}-\d{4}'  # 匹配 dd-mm-yyyy 格式的日期
    
    # 要匹配的文本
    text = 'Today is 31-07-2023 and tomorrow is 01-08-2023.'
    
    # 编译正则表达式
    regex = re.compile(pattern)
    
    # 执行匹配
    matches = regex.findall(text)
    
    # 输出匹配结果
    for match in matches:
        print("Match:", match)
    ```

    在这个示例中，我们定义了一个正则表达式模式，用于匹配 `dd-mm-yyyy` 格式的日期。然后，我们使用 `re.compile()` 编译了正则表达式，使用 `regex.findall()` 在给定的文本中执行匹配操作，并输出了匹配结果。

    正则模式匹配在文本处理和数据提取中非常有用，它允许你以灵活和强大的方式查找和操作文本中的信息。

- 查找和提取 findall match

  - 正则表达式在文本处理中常用于查找和提取符合特定模式的文本片段。查找操作用于寻找所有匹配的子串，而提取操作则是从匹配的子串中提取出特定的部分。以下是查找和提取操作的示例：

    **查找操作示例：**

    假设我们要从一段文本中查找所有的日期格式（yyyy-mm-dd）：

    ```python
    import re
    
    text = "Meeting is scheduled on 2023-08-10 and event is on 2023-08-15."
    
    pattern = r'\d{4}-\d{2}-\d{2}'
    matches = re.findall(pattern, text)
    
    print(matches)  # 输出 ['2023-08-10', '2023-08-15']
    ```

    **提取操作示例：**

    现在假设我们想要从这些日期中提取出年份部分：

    ```python
    import re
    
    text = "Meeting is scheduled on 2023-08-10 and event is on 2023-08-15."
    
    pattern = r'(\d{4})-\d{2}-\d{2}'
    matches = re.findall(pattern, text)
    
    years = [match for match in matches]
    
    print(years)  # 输出 ['2023', '2023']
    ```

    在上述示例中，`(\d{4})` 使用圆括号来定义一个捕获组，以便我们可以从匹配的日期中提取年份部分。

    正则表达式的查找和提取操作可以根据具体的需求进行调整和扩展。它们在从文本中提取信息、数据处理和转换等任务中非常有用。在实际应用中，你可能需要根据实际情况设计适合的正则表达式模式和提取方法。

- 替换  sub

  - 正则表达式在文本处理中经常用于替换操作，你可以使用正则表达式来查找匹配特定模式的文本片段，并将这些匹配项替换为其他内容。以下是替换操作的示例：

    假设我们要将文本中的所有手机号码替换为 `[PHONE]`：

    ```python
    import re
    
    text = "Contact me at 123-456-7890 or 987-654-3210 for more information."
    
    pattern = r'\d{3}-\d{3}-\d{4}'
    replacement = '[PHONE]'
    
    new_text = re.sub(pattern, replacement, text)
    
    print(new_text)
    # 输出 "Contact me at [PHONE] or [PHONE] for more information."
    ```

    在上述示例中，我们使用 `re.sub()` 函数来执行替换操作。`pattern` 是匹配手机号码的正则表达式模式，`replacement` 是要替换成的内容。

    通过修改正则表达式模式和替换内容，你可以根据不同的需求进行灵活的文本替换操作。正则表达式的替换功能在数据清理、文本格式转换等方面非常有用。需要注意的是，不同编程语言或工具中的正则表达式替换函数可能略有不同，具体用法可能会有些差异，需要查阅相应的文档。

- 验证和过滤  fullmatch  sub

  - 正则表达式在验证和过滤文本中非常有用。你可以使用正则表达式来验证一个字符串是否符合特定的模式，也可以将一个字符串中不符合特定模式的部分过滤掉。以下是验证和过滤操作的示例：

    **验证操作示例：**

    假设我们要验证一个字符串是否是有效的邮箱地址：

    ```python
    import re
    
    def validate_email(email):
        pattern = r'\w+@\w+\.\w+'
        return re.fullmatch(pattern, email) is not None
    
    email1 = "user@example.com"
    email2 = "invalid.email"
    
    print(validate_email(email1))  # 输出 True
    print(validate_email(email2))  # 输出 False
    ```

    **过滤操作示例：**

    现在假设我们要过滤掉一段文本中的所有非字母数字字符：

    ```python
    import re
    
    text = "Hello, 123! How are you? #GoodTimes"
    
    pattern = r'[^a-zA-Z0-9\s]'
    filtered_text = re.sub(pattern, '', text)
    
    print(filtered_text)  # 输出 "Hello 123 How are you GoodTimes"
    ```

    在上述示例中，我们使用 `re.fullmatch()` 函数来验证邮箱地址是否符合模式。对于过滤操作，我们使用 `re.sub()` 函数将非字母数字字符替换为空字符串。

    正则表达式在验证用户输入、过滤特定格式的数据、清理文本等方面非常有用。你可以根据实际需求设计不同的正则表达式模式来进行验证和过滤操作。需要注意的是，正则表达式的模式和用法可能因编程语言或工具而有所不同。

- 分割 split  字符串分割算法 split(seq,maxsplitnum)

  - 正则表达式在文本分割中也是非常有用的工具。你可以使用正则表达式来指定分割文本的模式，然后根据这个模式将文本分割成多个部分。以下是正则分割的示例：

    假设我们要根据逗号分隔符 `,` 将一串逗号分隔的数字分割成列表：

    ```python
    import re
    
    text = "1,2,3,4,5"
    
    pattern = r','
    result = re.split(pattern, text)
    
    print(result)  # 输出 ['1', '2', '3', '4', '5']
    ```

    在上述示例中，我们使用 `re.split()` 函数来进行分割操作。`pattern` 是用于匹配分隔符的正则表达式模式。

    正则分割在处理具有特定分隔符或模式的文本数据时非常有用。你可以根据不同的分割需求设计合适的正则表达式模式，以便将文本分割成适当的部分。需要注意的是，正则表达式的分割函数在不同的编程语言或工具中可能有一些差异，具体用法可能会有所不同。

- 清理和处理

  - 正则表达式在文本清除和处理方面非常有用。你可以使用正则表达式来查找和替换不需要的文本，进行数据清理、格式化等操作。以下是一些正则清除和处理的示例：

    **清除操作示例：**

    假设我们要清除一段文本中的所有非字母数字字符和空白字符：

    ```python
    import re
    
    text = "Hello, 123! How are you? #GoodTimes"
    
    pattern = r'[^a-zA-Z0-9\s]'
    cleaned_text = re.sub(pattern, '', text)
    
    print(cleaned_text)  # 输出 "Hello 123 How are you GoodTimes"
    ```

    **处理操作示例：**

    现在假设我们要将一段文本中的所有 URL 替换为 `[URL]`：

    ```python
    import re
    
    text = "Visit our website at https://www.example.com or http://example.net for more info."
    
    pattern = r'https?://\S+'
    replacement = '[URL]'
    
    processed_text = re.sub(pattern, replacement, text)
    
    print(processed_text)
    # 输出 "Visit our website at [URL] or [URL] for more info."
    ```

    在上述示例中，我们使用 `re.sub()` 函数进行文本清除和处理操作。`pattern` 是用于匹配不需要的文本的正则表达式模式，`replacement` 是用于替换成的内容。

    正则表达式的清除和处理操作可以根据实际需求来设计不同的模式和处理方式。它们在数据清理、文本格式转换等方面非常有用。需要注意的是，正则表达式的模式和用法可能因编程语言或工具而有所不同。

# 二十二、CGI 编程

## 22.1 CGI简介

​		在 Python 中，CGI（Common Gateway Interface）是一种用于在 Web 服务器和外部程序之间传递数据的标准接口。它允许开发人员编写脚本或程序，这些程序可以通过 Web 服务器来处理 HTTP 请求，并返回动态生成的内容作为响应。Python 提供了用于编写 CGI 脚本的库和模块，使开发人员能够创建与 Web 服务器交互的动态 Web 应用程序。

![cgiarch](https://atts.w3cschool.cn/attachments/image/Cgi01.png)

​		

## 22.2 CGI 创建步骤

```python
# 1. 环境
# 2. 倒入模块
# 3. http头部
# 4. 表单数据
# 5. 输出html
# 6. 页面逻辑处理
# 7. 输出内容
```

当在Python中创建一个简单的CGI程序时，你可以按照以下步骤进行：

1. 创建一个新文件，例如 `my_cgi_script.py`。

2. 在文件的开头添加指定Python解释器的Shebang（`#!/usr/bin/env python`）。

3. 导入CGI模块：`import cgi`

4. 输出HTTP头部：使用 `print()` 函数输出HTTP头部，指定内容类型为 `text/html`。

5. 获取表单数据：使用 `cgi.FieldStorage()` 来获取表单数据。

6. 输出HTML页面的其余部分，包括`<html>`、`<head>`和`<body>`。

7. 使用表单数据生成页面内容，或执行其他逻辑。

8. 输出生成的内容。

9. 保存文件，并确保文件在Web服务器的CGI目录中，并具有执行权限。

10. 通过浏览器访问CGI程序的URL，以查看输出。

以下是一个用Python编写的简单CGI程序示例：

```python
#!/usr/bin/env python

import cgi

# 输出HTTP头部
print("Content-type: text/html\n")

# 获取表单数据
form = cgi.FieldStorage()

# 输出HTML页面的其余部分
print("<html>")
print("<head><title>My CGI Script</title></head>")
print("<body>")
print("<h1>CGI Program in Python</h1>")

# 如果表单包含名为 "name" 的字段，则获取其值并输出
if "name" in form:
    name = form["name"].value
    print("<p>Hello, {}!</p>".format(name))
else:
    print("<p>Hello, CGI!</p>")

print("</body>")
print("</html>")
```

​		保存这个脚本，将其放置在支持CGI的Web服务器目录中，并确保文件有执行权限。然后，通过访问相应的URL（例如 `http://yourserver.com/cgi-bin/my_cgi_script.py`）在浏览器中查看输出。根据表单中是否存在名为 "name" 的字段，它将显示不同的问候消息。

### 22.2.1 http表头

在Python CGI 脚本中，HTTP 头部（HTTP Headers）是非常重要的，它们提供了关于请求和响应的元信息。以下是一些常见的 HTTP 头部信息，你可以在 CGI 脚本中使用 `print()` 函数来输出它们：

1. **Content-Type：** 指定响应主体的媒体类型。常见的类型有：
   - `text/html`：HTML 页面
   - `text/plain`：纯文本
   - `application/json`：JSON 数据
   - `application/xml`：XML 数据
   - 等等

   例如：
   ```python
   print("Content-type: text/html")
   ```

2. **Content-Length：** 指定响应主体的长度（字节数）。这在传输非文本数据时非常重要。
   ```python
   print("Content-Length: 12345")
   ```

3. **Location：** 用于重定向浏览器到另一个 URL。这在实现页面重定向时很有用。
   ```python
   print("Location: http://example.com/new_page.html")
   ```

4. **Cache-Control：** 控制缓存策略，指定是否缓存响应以及缓存的方式。
   ```python
   print("Cache-Control: no-cache, no-store, must-revalidate")
   ```

5. **Expires：** 指定响应的到期时间，用于缓存控制。
   ```python
   print("Expires: Tue, 01 Jan 2024 00:00:00 GMT")
   ```

6. **Set-Cookie：** 设置一个 HTTP Cookie。
   ```python
   print("Set-Cookie: username=john; Expires=Wed, 21 Jul 2023 00:00:00 GMT;")
   ```

7. **Content-Disposition：** 控制浏览器如何显示响应，常用于下载文件。
   ```python
   print("Content-Disposition: attachment; filename=myfile.txt")
   ```

8. **Access-Control-Allow-Origin：** 设置允许跨域请求的源。
   ```python
   print("Access-Control-Allow-Origin: *")
   ```

9. **HTTP 状态码：** 在响应的起始行中指定状态码和状态描述，如 200 OK、404 Not Found 等。
   ```python
   print("Status: 200 OK")
   ```

10. **其他自定义头部：** 你还可以定义自己的 HTTP 头部，用于传递自定义的元信息。
    ```python
    print("X-My-Header: Custom Value")
    ```



| 响应头           | 说明                           | 示例                                         |
| ---------------- | ------------------------------ | -------------------------------------------- |
| Content-Type     | 响应的内容类型                 | Content-Type: text/html                      |
| Content-Length   | 响应正文的字节数               | Content-Length: 12345                        |
| Content-Encoding | 响应内容的压缩方式             | Content-Encoding: gzip                       |
| Location         | 执行重定向操作时的目标位置     | Location: http://www.example.com/newpage     |
| Status           | 响应的状态码和状态消息         | Status: 200 OK                               |
| Cache-Control    | 缓存控制，指定如何缓存响应内容 | Cache-Control: no-cache, max-age=0           |
| Expires          | 响应内容的过期时间             | Expires: Wed, 21 Jul 2023 10:30:00 GMT       |
| Last-Modified    | 资源的上次修改时间             | Last-Modified: Mon, 15 Jun 2023 15:45:00 GMT |

### 22.2.2 CGI环境变量

以下是常见的 CGI 环境变量以及它们的含义，按照表格形式呈现：

| 环境变量        | 含义与用途                                                |
| --------------- | --------------------------------------------------------- |
| CONTENT_TYPE    | 指示请求的内容类型，适用于 POST 请求。                    |
| CONTENT_LENGTH  | 对于 POST 请求，指示请求正文的字节数。                    |
| HTTP_COOKIE     | 包含客户端发送的 Cookie 数据，如果有的话。                |
| HTTP_USER_AGENT | 包含客户端浏览器的用户代理字符串。                        |
| HTTP_REFERER    | 如果请求是从另一个页面链接过来的，包含引用页面的 URL。    |
| HTTP_HOST       | 包含客户端请求的主机名。                                  |
| PATH_INFO       | 包含额外的路径信息，通常用于 URL 到脚本的特定操作的映射。 |
| QUERY_STRING    | 包含 URL 中的查询字符串部分，通常用于获取 GET 请求参数。  |
| REQUEST_METHOD  | 指示请求的 HTTP 方法，如 GET、POST、PUT 等。              |
| REMOTE_ADDR     | 客户端的 IP 地址。                                        |
| REMOTE_PORT     | 客户端连接的端口号。                                      |
| SERVER_NAME     | 服务器的主机名。                                          |
| SERVER_PORT     | 服务器的端口号。                                          |
| SERVER_SOFTWARE | 服务器软件的名称和版本。                                  |

​		这些环境变量提供了与客户端请求和服务器环境相关的元数据，使 CGI 脚本能够获取必要的信息以生成适当的响应。在 CGI 脚本中，您可以根据需要使用编程语言的相关方法来访问这些环境变量。



### 22.2.3 数据传输方法

| 名称                 | 描述                                | 用途和特点                         |
| -------------------- | ----------------------------------- | ---------------------------------- |
| GET                  | HTTP 请求方法，通过 URL 传输数据    | 请求数据，显示在 URL，长度限制     |
| POST                 | HTTP 请求方法，通过请求正文传输数据 | 提交数据，不显示在 URL，无长度限制 |
| JSON                 | 数据格式，表示结构化数据            | 用于 API 数据交换，支持复杂结构    |
| 复选框（Checkbox）   | HTML 表单元素，多选                 | 从多个选项中选择一个或多个         |
| 单选按钮（Radio）    | HTML 表单元素，单选                 | 从多个选项中选择一个               |
| 文本区域（Textarea） | HTML 表单元素，多行文本输入         | 接受多行文本输入，如评论、描述等   |
| 下拉列表（Select）   | HTML 表单元素，从预定义选项中选择   | 单选从预定义选项中选择一个         |
| Cookie               | 服务器在客户端保存的小型数据片段    | 存储用户信息，跨请求共享           |

这个表格展示了每个数据传输方式和输入元素的主要用途和特点，有助于您理解它们在 Web 开发中的应用。



区别：

- **数据传输方式（GET vs. POST vs. JSON）：** GET 和 POST 是不同的 HTTP 请求方法，用于传输数据，其中 GET 将数据放在 URL 中，而 POST 将数据放在请求正文中。JSON 是一种数据格式，通常用于 API 数据交换。
- **数据传输方式与数据类型：** GET 和 POST 主要用于传输表单数据，而 JSON 可以传输结构化数据。
- **复选框 vs. 单选按钮：** 复选框允许多选，单选按钮只能单选。
- **文本区域 vs. 输入框：** 文本区域适合多行文本输入，输入框适合单行文本。
- **下拉列表 vs. 复选框/单选按钮：** 下拉列表提供有限的选项供用户选择，复选框和单选按钮可以有多个选项。
- **Cookie：** Cookie 用于在客户端存储小量数据，而 GET、POST 和 JSON 用于在客户端和服务器之间传输数据。





![User](https://chat.openai.com/_next/image?url=https%3A%2F%2Fs.gravatar.com%2Favatar%2F6f93a6e3074398946ebfe3233eeea90b%3Fs%3D480%26r%3Dpg%26d%3Dhttps%253A%252F%252Fcdn.auth0.com%252Favatars%252F86.png&w=96&q=75)



用表格表示这些信息



ChatGPT



下面是关于不同数据传输方式和输入元素的信息，以表格形式呈现：

| 名称                 | 描述                                | 用途和特点                         |
| -------------------- | ----------------------------------- | ---------------------------------- |
| GET                  | HTTP 请求方法，通过 URL 传输数据    | 请求数据，显示在 URL，长度限制     |
| POST                 | HTTP 请求方法，通过请求正文传输数据 | 提交数据，不显示在 URL，无长度限制 |
| JSON                 | 数据格式，表示结构化数据            | 用于 API 数据交换，支持复杂结构    |
| 复选框（Checkbox）   | HTML 表单元素，多选                 | 从多个选项中选择一个或多个         |
| 单选按钮（Radio）    | HTML 表单元素，单选                 | 从多个选项中选择一个               |
| 文本区域（Textarea） | HTML 表单元素，多行文本输入         | 接受多行文本输入，如评论、描述等   |
| 下拉列表（Select）   | HTML 表单元素，从预定义选项中选择   | 单选从预定义选项中选择一个         |
| Cookie               | 服务器在客户端保存的小型数据片段    | 存储用户信息，跨请求共享           |

这个表格展示了每个数据传输方式和输入元素的主要用途和特点，有助于您理解它们在 Web 开发中的应用。



这是有关在 Web 开发中不同数据传输方式和输入元素之间的区别：

| 方式/元素            | 描述与用途                           | 区别与特点                                                  |
| -------------------- | ------------------------------------ | ----------------------------------------------------------- |
| GET                  | 使用 URL 将数据附加到请求中          | 数据在 URL 中，有长度限制，通常用于请求数据，如查询页面内容 |
| POST                 | 将数据放在请求的正文中               | 数据不在 URL 中，无长度限制，通常用于提交数据，如表单提交   |
| JSON                 | 使用 JSON 格式传输结构化数据         | 适用于 API 数据交换，支持复杂结构                           |
| 复选框（Checkbox）   | 表单元素，允许选择多个选项           | 从多个选项中选择一个或多个                                  |
| 单选按钮（Radio）    | 表单元素，只能选择一个选项           | 从多个选项中选择一个                                        |
| 文本区域（Textarea） | 表单元素，用于多行文本输入           | 接受多行文本输入，如评论、描述等                            |
| 下拉列表（Select）   | 表单元素，从预定义选项中选择一个选项 | 单选从预定义选项中选择一个                                  |
| Cookie               | 服务器在客户端保存的小型数据片段     | 存储用户信息，跨请求共享                                    |

这个表格列出了不同数据传输方式和输入元素的主要区别和特点。根据您的应用需求，您可以选择适当的方式和元素来实现所需的功能。

- 1. get

  - "GET" 是一种在 Web 开发中常用的 HTTP 请求方法。**它用于从服务器获取数据**，通常将数据附加到 URL 的查询参数中。当用户在浏览器中访问一个链接、点击按钮或提交表单时，可能会发出 GET 请求。以下是关于 "GET" 方法的一些关键点：

    - **请求方式：** GET 是一种 HTTP 请求方法，用于向服务器请求数据。它是最常见的请求方法之一。

    - **数据传输：** 在 GET 请求中，数据通过 URL 的查询参数传递给服务器。查询参数以 `?` 开头，多个参数使用 `&` 连接。

    - **数据可见性：** 因为数据显示在 URL 中，所以可以在浏览器的地址栏中看到。这意味着数据对于用户和其他人都是可见的。

    - **数据长度限制：** GET 请求的数据长度有限制，不同浏览器和服务器可能会有不同的限制。因此，GET 请求适用于较小的数据传输。

    - **安全性：** 因为数据可见且显示在 URL 中，GET 请求不适合传输敏感信息，如密码。敏感信息可能会被泄露。

    - **幂等性：** GET 请求是幂等的，这意味着多次连续相同的 GET 请求将产生相同的结果，不会对服务器状态产生影响。

    - **缓存：** GET 请求可能会被浏览器缓存，以提高性能。但是，缓存可能导致服务器端更新不及时。

    - **使用场景：** GET 请求适用于获取数据，如页面内容、搜索结果等。它通常用于展示信息，而不涉及对服务器数据的更改。

    下面是一个使用 HTML 表单和 "GET" 请求的简单示例：

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>GET Request Example</title>
    </head>
    <body>
        <h1>GET Request Example</h1>
        <form action="server.php" method="GET">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name"><br><br>
            <label for="age">Age:</label>
            <input type="text" id="age" name="age"><br><br>
            <input type="submit" value="Submit">
        </form>
    </body>
    </html>
    ```

    在这个示例中，当用户提交表单时，浏览器会将输入的数据作为查询参数附加到 URL，并向服务器发出 GET 请求。服务器可以通过解析查询参数来获取用户输入的数据。

  - 例如，以下是一个简单的使用 GET 方法的 URL 示例：

    ```
    https://example.com/api/data?param1=value1&param2=value2
    ```

    在这个 URL 中，`param1` 和 `param2` 是查询参数，它们将被服务器解析并用于响应相应的数据。

    总之，GET 方法是一种常用的 HTTP 请求方法，适用于获取数据。但需要注意数据的可见性、长度限制和安全性等方面的问题。

- 2. post

  - POST 方法是一种 HTTP 请求方法，与 GET 方法相反，**它用于向服务器提交数据**。以下是有关 POST 方法的更多详细信息：

    1. **数据传输方式：** 在 POST 请求中，数据放在请求的正文中，而不是像 GET 请求那样附加在 URL 上。这使得 POST 方法适合用于传输较大的数据。

    2. **数据可见性：** 由于数据不会显示在 URL 中，因此 POST 请求的数据对于用户来说是不可见的。这有助于保护敏感信息。

    3. **数据长度限制：** POST 请求没有像 GET 请求那样的 URL 长度限制。因此，您可以更自由地传输较大量的数据。

    4. **请求性质：** POST 请求不一定是幂等的，即多次相同的 POST 请求可能会对服务器状态产生不同的影响。因此，POST 请求常用于修改数据。

    5. **安全性：** 由于数据不会显示在 URL 中，POST 请求相对更安全，适合用于处理敏感信息，如密码。

    6. **缓存：** 默认情况下，POST 请求不会被浏览器缓存，这意味着每次请求都会从服务器获取最新的数据。

    7. **使用场景：** POST 请求适合提交数据，如通过表单提交数据、向服务器发送命令等。它适合会对服务器状态产生影响的请求。

    例如，以下是一个简单的使用 POST 方法的表单提交示例：

    ```html
    <form action="https://example.com/api/submit" method="post">
      <input type="text" name="username" placeholder="Username">
      <input type="password" name="password" placeholder="Password">
      <button type="submit">Submit</button>
    </form>
    ```

    在这个表单中，当用户点击提交按钮时，表单数据将以 POST 请求的方式发送到指定的 URL。

    总之，POST 方法用于向服务器提交数据，适合传输敏感信息和修改数据。与 GET 方法相比，它提供了更好的数据保护和更大的数据传输灵活性。

- 3. json

  - 提交

    - 要在 Web 开发中提交 JSON 数据，您可以使用 HTTP 请求（通常是 POST 请求）来发送 JSON 数据到服务器。这可以通过多种方式实现，包括 JavaScript、命令行工具、Postman 等。

      以下是一些常见的提交 JSON 数据的方法：

      1. **使用 JavaScript（浏览器端）：** 在浏览器中，您可以使用 JavaScript 发起 AJAX 请求来提交 JSON 数据。下面是使用 `fetch` API 的简单示例：

         ```javascript
         const jsonData = {
           key1: 'value1',
           key2: 'value2'
         };

         fetch('https://example.com/api/endpoint', {
           method: 'POST',
           headers: {
             'Content-Type': 'application/json'
           },
           body: JSON.stringify(jsonData)
         })
         .then(response => response.json())
         .then(data => {
           console.log(data);
         });
         ```

      2. **使用 cURL（命令行工具）：** 在命令行中，您可以使用 cURL 工具来提交 JSON 数据。以下是一个示例：

         ```bash
         curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1","key2":"value2"}' https://example.com/api/endpoint
         ```

      3. **使用 Postman：** Postman 是一个流行的 API 测试工具，它可以帮助您轻松地发送各种类型的请求，包括提交 JSON 数据。您可以在 Postman 中配置请求头和请求体，然后发送请求并查看响应。

      4. **使用编程语言库：** 如果您在后端使用编程语言（如 Python、Node.js、Java 等），您可以使用相应的库来发送 HTTP 请求并提交 JSON 数据。每种语言都有适用于此目的的库和模块。

      请注意，无论您选择哪种方法，都需要确保您的服务器端能够正确解析和处理收到的 JSON 数据。您的服务器端代码应该能够读取请求的正文，然后使用相应的方法（如在 Python 中使用 `json.loads()`）来解析 JSON 数据。

  - 获取

    - **在 CGI 脚本中获取 JSON 数据：** 在 CGI 脚本中，您可以通过读取标准输入流来获取 POST 数据。具体的步骤可能因所使用的编程语言而异。

      下面是一个 Python CGI 脚本示例，演示如何获取和处理提交的 JSON 数据：


    ```python
    #!/usr/bin/env python
    
    import cgi
    import sys
    import json
    
    # 从标准输入流读取 POST 数据
    post_data = sys.stdin.read()
    
    # 设置响应头，指定内容类型为 JSON
    print("Content-Type: application/json\n")
    
    try:
        # 解析 JSON 数据
        data = json.loads(post_data)
        # 在这里可以对数据进行处理
        result = {"success": True, "message": "JSON data received and processed"}
    except json.JSONDecodeError:
        result = {"success": False, "message": "Invalid JSON data"}
    
    # 将处理结果返回给客户端
    print(json.dumps(result))
    ```
    
    在这个示例中，`sys.stdin.read()` 用于从标准输入流读取 POST 数据，然后使用 `json.loads()` 解析 JSON 数据。
    
    1. **处理和返回结果：** 在脚本中，您可以根据需要处理解析的 JSON 数据。在这个示例中，我们简单地返回一个包含处理结果的 JSON 对象。
    
    2. **获取响应：** 在客户端中，您可以解析 CGI 脚本返回的 JSON 响应，并根据需要进行处理。
    
    请注意，这个示例是一个基本的演示，实际应用中可能需要更多的错误处理和逻辑。不同的编程语言和 CGI 环境可能有不同的方式来处理 JSON 数据，但基本原理是类似的：提交 JSON 数据，从标准输入流中获取数据，处理数据，然后生成相应的 JSON 响应。

- 4. 单选框 Radio Buttons

  - 单选按钮（Radio Buttons）是一种常见的 HTML 表单元素，允许用户从一组选项中选择一个选项。每个单选按钮都有一个相关联的值，当用户选择其中一个单选按钮时，该按钮的值将被提交到服务器或可以通过 JavaScript 获取。

    以下是使用 HTML 创建单选按钮的示例：

    ```html
    <form action="process_form.cgi" method="POST">
      <p>请选择性别：</p>
      <input type="radio" id="male" name="gender" value="male">
      <label for="male">男性</label><br>
      <input type="radio" id="female" name="gender" value="female">
      <label for="female">女性</label><br>
      <input type="radio" id="other" name="gender" value="other">
      <label for="other">其他</label><br>
      <br>
      <input type="submit" value="提交">
    </form>
    ```

    在这个示例中，`input` 元素的 `type` 属性设置为 "radio"，`name` 属性指定了单选按钮组的名称，每个单选按钮通过 `value` 属性来定义其关联的值。`label` 元素用于显示文本标签，并通过 `for` 属性与相应的单选按钮关联起来。

    在用户提交表单时，所选的单选按钮的值将通过表单的 POST 请求传递到服务器端（在 `name` 属性的名称下）。服务器端的脚本可以读取这个值并采取相应的操作。

    要在 JavaScript 中获取用户选择的单选按钮的值，可以使用以下方法：

    ```javascript
    const selectedGender = document.querySelector('input[name="gender"]:checked').value;
    console.log(selectedGender);
    ```

    这将选择名为 "gender" 的单选按钮组中被选中的按钮的值。

    总之，单选按钮是一种允许用户从一组选项中选择一个选项的 HTML 表单元素，适用于收集用户的单一选择。

- 5. 复选框 

  - 复选框（Checkboxes）是另一种常见的 HTML 表单元素，允许用户从多个选项中选择一个或多个选项。每个复选框都有一个相关联的值，当用户选中一个或多个复选框时，这些复选框的值将被提交到服务器或可以通过 JavaScript 获取。

    以下是使用 HTML 创建复选框的示例：

    ```html
    <form action="process_form.cgi" method="POST">
      <p>请选择您的爱好：</p>
      <input type="checkbox" id="reading" name="hobbies[]" value="reading">
      <label for="reading">阅读</label><br>
      <input type="checkbox" id="swimming" name="hobbies[]" value="swimming">
      <label for="swimming">游泳</label><br>
      <input type="checkbox" id="painting" name="hobbies[]" value="painting">
      <label for="painting">绘画</label><br>
      <br>
      <input type="submit" value="提交">
    </form>
    ```

    在这个示例中，`input` 元素的 `type` 属性设置为 "checkbox"，`name` 属性指定了复选框组的名称，每个复选框通过 `value` 属性来定义其关联的值。`label` 元素用于显示文本标签，并通过 `for` 属性与相应的复选框关联起来。注意 `name` 属性的值以 `[]` 结尾，这样多个选中的复选框的值会被作为数组传递给服务器端。

    在用户提交表单时，选中的复选框的值将通过表单的 POST 请求传递到服务器端（在 `name` 属性的名称下，作为数组）。

    要在 JavaScript 中获取用户选中的复选框的值，可以使用以下方法：

    ```javascript
    const selectedHobbies = Array.from(document.querySelectorAll('input[name="hobbies[]"]:checked')).map(checkbox => checkbox.value);
    console.log(selectedHobbies);
    ```

    这将选择名为 "hobbies[]" 的复选框组中被选中的复选框的值，并将它们存储在一个数组中。

    复选框适用于让用户从多个选项中选择一个或多个选项，如选择兴趣爱好、勾选多个选项等。

- 6. 文本区域

  - 文本区域（Textarea）是一个 HTML 表单元素，允许用户输入多行文本。它通常用于用户评论、描述、消息等需要大段文字输入的场景。

    以下是使用 HTML 创建文本区域的示例：

    ```html
    <form action="process_form.cgi" method="POST">
      <p>请在下面输入您的评论：</p>
      <textarea id="comment" name="comment" rows="4" cols="50"></textarea><br>
      <br>
      <input type="submit" value="提交">
    </form>
    ```

    在这个示例中，`textarea` 元素被用来创建一个文本区域。它有一个 `name` 属性来标识输入的名称，以及 `rows` 和 `cols` 属性来设置文本区域的行数和列数。

    在用户提交表单时，文本区域中输入的文本将通过表单的 POST 请求传递到服务器端（在 `name` 属性的名称下）。

    要在 JavaScript 中获取用户在文本区域中输入的文本，可以使用以下方法：

    ```javascript
    const commentValue = document.getElementById('comment').value;
    console.log(commentValue);
    ```

    这将获取具有 `id` 为 "comment" 的文本区域中输入的文本内容。

    总之，文本区域是一个适用于用户输入多行文本的 HTML 表单元素，常用于收集用户的评论、描述等。

- 7. 下拉列表

  - 下拉列表（Select）是一种 HTML 表单元素，它允许用户从预定义的选项列表中选择一个选项。下拉列表通常用于需要用户从一组固定选项中选择一个选项的情况，如选择国家、城市、产品等。

    以下是使用 HTML 创建下拉列表的示例：

    ```html
    <form action="process_form.cgi" method="POST">
      <p>请选择您所在的国家：</p>
      <select id="country" name="country">
        <option value="usa">美国</option>
        <option value="canada">加拿大</option>
        <option value="uk">英国</option>
        <option value="australia">澳大利亚</option>
      </select><br>
      <br>
      <input type="submit" value="提交">
    </form>
    ```

    在这个示例中，`select` 元素用于创建一个下拉列表。每个选项都使用 `option` 元素定义，其中的 `value` 属性指定了选项的值，显示在下拉列表中的文本由 `option` 元素的内容定义。

    在用户选择一个选项并提交表单时，所选选项的值将通过表单的 POST 请求传递到服务器端（在 `name` 属性的名称下）。

    要在 JavaScript 中获取用户选择的选项的值，可以使用以下方法：

    ```javascript
    const selectedCountry = document.getElementById('country').value;
    console.log(selectedCountry);
    ```

    这将获取具有 `id` 为 "country" 的下拉列表中被选中的选项的值。

    总之，下拉列表是一种用于从预定义选项中选择一个选项的 HTML 表单元素，适用于需要用户在有限选项中进行选择的情况。

- 8. cooike

  - 我相信您可能想询问关于 Cookie（HTTP Cookie）的信息。Cookie 是一种用于在 Web 浏览器和服务器之间传递状态信息的小型数据片段。

    以下是关于 Cookie 的详细信息：

    1. **用途：** Cookie 主要用于跟踪用户在网站上的活动，存储用户首选项，以及在不同请求之间传递一些数据。它们可以用于保持用户登录状态、记录购物车内容、跟踪用户浏览历史等。

    2. **工作原理：** 服务器通过 HTTP 响应头将 Cookie 发送给客户端浏览器，然后浏览器会将 Cookie 存储在用户的计算机上。每次用户访问相同的域名时，浏览器会在请求头中包含相应的 Cookie，以便服务器可以读取和处理。

    3. **属性：** Cookie 有各种属性，如名称、值、过期时间、路径、域等。过期时间可以设置为会话级别（当浏览器关闭时过期）或具体的日期时间。

    4. **安全性：** Cookie 在用户计算机上存储，因此可以被用户或其他应用程序访问。对于敏感信息，可以使用 HTTPS 连接来加密传输。

    5. **限制：** 每个域名下的浏览器一般会限制 Cookie 的数量和大小。

    6. **JavaScript 操作：** 使用 JavaScript，您可以在浏览器中创建、读取和删除 Cookie。

    以下是一个使用 JavaScript 操作 Cookie 的简单示例：

    ```javascript
    // 设置 Cookie
    document.cookie = "username=John Doe; expires=Thu, 31 Dec 2023 23:59:59 UTC; path=/";
    
    // 读取 Cookie
    const cookies = document.cookie.split('; ');
    for (const cookie of cookies) {
      const [name, value] = cookie.split('=');
      console.log(name, value);
    }
    
    // 删除 Cookie
    document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/";
    ```

    总之，Cookie 是一种在客户端浏览器和服务器之间传递状态信息的常用机制。它在 Web 开发中扮演着重要角色，用于维护用户状态和存储临时数据。

- 9. session

  - `Session`（会话）是在Web开发中用于跟踪用户在一系列请求和响应之间的状态和数据的机制。它允许服务器在不同的HTTP请求之间保持某些信息，以便在整个用户会话中持久保存数据。

    会话通常用于以下情况：

    1. **用户认证和授权：** 当用户登录到网站时，服务器可以创建一个会话，将用户的登录状态保存在会话中，以便在后续的请求中验证用户身份并授予适当的权限。

    2. **购物车功能：** 在电子商务网站中，会话可以用于跟踪用户将要购买的商品列表，以及管理购物车中的商品数量和选项。

    3. **用户首选项：** 网站可以使用会话来存储用户的偏好设置，如语言、主题等，以便在用户访问其他页面时保持一致。

    4. **表单数据：** 当用户在多个页面之间填写表单时，会话可以用于存储表单数据，以便用户在提交表单时可以轻松访问之前输入的数据。

    5. **临时数据存储：** 如果需要在多个请求之间共享临时数据，会话可以用于存储这些数据，而不必将数据存储在数据库或文件中。

    在Web开发中，会话通常通过在客户端浏览器上设置一个唯一的标识符（通常是一个会话ID）来实现。这个标识符被用于将用户的数据关联到相应的会话。会话数据可以存储在服务器端的内存、数据库中，或者在一些分布式存储系统中，具体取决于应用程序的需求和架构。

    在Python中，有许多库和框架可以帮助你实现会话管理，如Flask中的`session`对象、Django中的`request.session`等。这些工具简化了会话的创建、管理和存储。

    以下是一个使用Python的Flask框架实现会话（Session）的简单示例代码。Flask提供了一个内置的`session`对象，可以方便地处理会话数据。

    首先，确保你已经安装了Flask。可以使用以下命令安装：

    ```bash
    pip install flask
    ```

    然后，创建一个名为 `app.py` 的文件，将以下代码添加到文件中：

    ```python
    from flask import Flask, request, session, redirect, url_for, render_template
    
    app = Flask(__name__)
    
    # 设置一个秘密的密钥，用于加密会话数据
    app.secret_key = "mysecretkey"
    
    # 路由：首页
    @app.route("/")
    def index():
        if "username" in session:
            return f"Hello, {session['username']}! <a href='/logout'>Logout</a>"
        return "Welcome! <a href='/login'>Login</a>"
    
    # 路由：登录页面
    @app.route("/login", methods=["GET", "POST"])
    def login():
        if request.method == "POST":
            username = request.form["username"]
            session["username"] = username
            return redirect(url_for("index"))
        return render_template("login.html")
    
    # 路由：登出
    @app.route("/logout")
    def logout():
        session.pop("username", None)
        return redirect(url_for("index"))
    
    if __name__ == "__main__":
        app.run(debug=True)
    ```

    接下来，在同级目录下创建一个名为 `templates` 的文件夹，并在其中创建一个名为 `login.html` 的文件，将以下代码添加到文件中：

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Login</title>
    </head>
    <body>
        <h1>Login</h1>
        <form method="post">
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required>
            <button type="submit">Login</button>
        </form>
    </body>
    </html>
    ```

    这个示例创建了一个简单的Flask应用，实现了用户会话的基本功能。当用户访问首页时，如果已经登录，则显示欢迎消息和登出链接。如果没有登录，则显示欢迎消息和登录链接。用户可以通过访问 `/login` 路由来登录，登录后会将用户名存储在会话中。用户可以通过访问 `/logout` 路由来登出，登出后会话数据被移除。

    要运行这个示例，运行以下命令：

    ```bash
    python app.py
    ```

    然后在浏览器中访问 `http://127.0.0.1:5000/` 来查看效果。

    

- cookie 和 session的区别

  

  - `Cookie` 和 `Session` 都是在Web开发中用于管理用户状态和数据的机制，但它们在实现和使用上有一些不同之处。

  **Cookie：**

  1. **存储位置：** Cookie 是存储在用户的浏览器中的小文本文件。当服务器向浏览器发送响应时，可以通过设置 `Set-Cookie` 头部将Cookie发送到浏览器，浏览器会将其存储在本地。

  2. **数据存储：** Cookie 可以存储少量的数据，通常不超过几KB。它们主要用于存储短期数据，如用户的偏好设置、购物车内容等。

  3. **持久性：** Cookie 可以设置过期时间，可以是会话级别的（浏览器关闭后失效）或持久性的（在指定时间内有效）。

  4. **隐私：** Cookie 存储在用户的浏览器中，可能会引发隐私问题，因为用户可以查看和删除它们。还有可能出现跨站点请求伪造（CSRF）等安全问题。

  **Session：**

  1. **存储位置：** 会话数据存储在服务器端，通常存储在内存、数据库或其他分布式存储中。

  2. **数据存储：** 会话可以存储较大量的数据，因为数据存储在服务器上。它们通常用于存储用户认证信息、购物车内容、用户首选项等。

  3. **持久性：** 会话可以设置为在用户关闭浏览器后失效，也可以在一段时间内保持活动。

  4. **隐私：** 会话数据存储在服务器端，对用户不可见。这减少了隐私和安全问题，但需要服务器来管理会话数据。

  在实际应用中，通常会根据需求选择使用Cookie还是Session。例如，对于较小的数据（如用户偏好设置），可以使用Cookie。而对于敏感信息（如用户登录状态），通常使用Session更安全，因为敏感信息不会被存储在用户浏览器中。许多Web框架和库提供了对Cookie和Session的支持，使其更易于使用和管理。

### 22.2.4 文件处理

- 文件上传

  - 在CGI脚本中实现文件上传是一种常见的任务，可以通过使用Python的CGI模块来完成。以下是一个简单的示例，演示了如何在CGI脚本中处理文件上传：

    首先，创建一个名为 `upload.html` 的HTML文件，用于显示文件上传表单：

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>File Upload</title>
    </head>
    <body>
        <h1>File Upload</h1>
        <form method="post" action="upload_cgi.py" enctype="multipart/form-data">
            <label for="file">Select a file:</label>
            <input type="file" id="file" name="file">
            <button type="submit">Upload</button>
        </form>
    </body>
    </html>
    ```

    然后，创建一个名为 `upload_cgi.py` 的CGI脚本，用于处理文件上传：

    ```python
    #!/usr/bin/env python
    
    import cgi
    import os
    
    # 输出HTTP头部
    print("Content-type: text/html\n")
    
    # 获取表单数据
    form = cgi.FieldStorage()
    
    # 检查是否有文件上传
    if "file" in form:
        file_item = form["file"]
    
        # 如果文件项是文件类型
        if file_item.file:
            # 获取文件名和保存路径
            filename = os.path.basename(file_item.filename)
            save_path = os.path.join("/path/to/save/folder", filename)
    
            # 保存文件到指定路径
            with open(save_path, "wb") as save_file:
                save_file.write(file_item.file.read())
    
            print("<h2>File uploaded successfully: {}</h2>".format(filename))
        else:
            print("<h2>No file uploaded.</h2>")
    else:
        print("<h2>No file uploaded.</h2>")
    ```

    确保将 `/path/to/save/folder` 替换为实际希望保存上传文件的文件夹路径。

    这个示例中的HTML文件创建了一个文件上传表单，用户可以选择并上传文件。在 `upload_cgi.py` 脚本中，使用CGI模块获取表单数据，检查是否有文件上传，然后将上传的文件保存到指定路径中。

    要运行这个示例，将 `upload.html` 和 `upload_cgi.py` 放置在支持CGI的Web服务器目录中，并确保具有执行权限。然后，通过浏览器访问 `upload.html` 来访问文件上传页面。上传的文件将保存在指定的文件夹中。

- 文件下载

  - 在CGI脚本中实现文件下载也是一个常见的任务。以下是一个简单的示例，演示了如何在CGI脚本中提供文件下载：

    首先，创建一个名为 `download.html` 的HTML文件，用于显示下载链接：

    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>File Download</title>
    </head>
    <body>
        <h1>File Download</h1>
        <p><a href="download_cgi.py?filename=myfile.txt">Download myfile.txt</a></p>
    </body>
    </html>
    ```

    然后，创建一个名为 `download_cgi.py` 的CGI脚本，用于处理文件下载请求：

    ```python
    #!/usr/bin/env python
    
    import cgi
    import os
    
    # 输出HTTP头部
    print("Content-type: application/octet-stream")
    print("Content-Disposition: attachment; filename=\"myfile.txt\"\n")
    
    # 读取文件内容并输出
    with open("/path/to/myfile.txt", "rb") as file:
        data = file.read()
        print(data)
    ```

    确保将 `/path/to/myfile.txt` 替换为实际的文件路径和文件名。

    在这个示例中，`download.html` 创建了一个下载链接，指向 `download_cgi.py` 脚本。在 `download_cgi.py` 脚本中，首先输出了适当的HTTP头部，告诉浏览器该文件是要下载的，并设置了文件名。然后，使用 `open()` 函数读取文件内容，并使用 `print()` 函数将文件内容输出到响应中。

    要运行这个示例，将 `download.html` 和 `download_cgi.py` 放置在支持CGI的Web服务器目录中，并确保具有执行权限。然后，通过浏览器访问 `download.html` 来显示下载链接。当用户点击链接时，浏览器将提示用户下载文件。

    

##     22.3 CGI函数



```python
>>> import cgi
>>> dir(cgi)
['BytesIO', 'FeedParser', 'FieldStorage', 'Mapping', 'Message', 'MiniFieldStorage', 'StringIO', 'TextIOWrapper', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '__version__', '_parseparam', 'closelog', 'dolog', 'html', 'initlog', 'locale', 'log', 'logfile', 'logfp', 'maxlen', 'nolog', 'os', 'parse', 'parse_header', 'parse_multipart', 'print_arguments', 'print_directory', 'print_environ', 'print_environ_usage', 'print_exception', 'print_form', 'sys', 'tempfile', 'test', 'urllib', 'valid_boundary']
```



下面是将提供的信息转换成表格的示例，其中包含了简要的描述和一个示例：

| 名称                | 描述                                         | 示例                                               |
| ------------------- | -------------------------------------------- | -------------------------------------------------- |
| BytesIO             | 在内存中处理二进制数据的类                   | 用于将二进制数据读取到内存或从内存中写入二进制数据 |
| FeedParser          | 解析邮件和其他数据流的类                     | 解析电子邮件的原始数据                             |
| FieldStorage        | 处理HTTP POST请求中的表单数据的类            | 处理通过HTTP表单提交的用户数据                     |
| Mapping             | 提供映射操作的基本接口                       | 用于创建自定义的映射类                             |
| Message             | 处理电子邮件消息的模块                       | 创建、解析和处理电子邮件消息                       |
| MiniFieldStorage    | 类似于FieldStorage，处理HTTP请求中的表单数据 | 处理较小规模的HTTP表单数据                         |
| StringIO            | 在内存中处理文本数据的类                     | 用于将文本数据读取到内存或从内存中写入文本数据     |
| TextIOWrapper       | 在文本模式下包装字节流的类                   | 处理二进制文件数据的文本包装器                     |
| \_\_all\_\_         | 模块级别的变量，定义import *时应导入的符号   | from module import * 导入的符号                    |
| \_\_builtins\_\_    | 包含内置函数和异常的命名空间                 | 内置函数例如print、len等                           |
| \_\_cached\_\_      | 缓存模块的路径                               | 保存模块文件的缓存路径                             |
| \_\_doc\_\_         | 模块的文档字符串                             | 模块的说明文档                                     |
| \_\_file\_\_        | 当前模块文件的路径                           | 模块文件的完整路径                                 |
| \_\_loader\_\_      | 加载当前模块的加载器                         | 加载模块的对象                                     |
| \_\_name\_\_        | 模块的名称                                   | 模块的名称，例如当前模块的名称为模块名             |
| \_\_package\_\_     | 模块所属的包                                 | 包的名称，例如模块位于my_package子包中             |
| \_\_spec\_\_        | 模块的规范                                   | 模块的规范，包括名称、路径等信息                   |
| \_\_version\_\_     | 模块的版本信息                               | 模块的版本号                                       |
| _parseparam         | 解析HTTP头部参数的函数                       | 解析Content-Type头部中的参数                       |
| closelog            | 关闭日志记录的函数                           | 停止记录日志                                       |
| dolog               | 执行日志记录的函数                           | 记录操作日志                                       |
| html                | HTML相关功能的模块                           | 处理HTML相关的操作                                 |
| initlog             | 初始化日志记录的函数                         | 初始化日志记录                                     |
| locale              | 处理本地化操作的模块                         | 设置和管理本地化信息                               |
| log                 | 日志记录相关功能的模块                       | 记录和管理日志                                     |
| logfile             | 日志文件的路径                               | 指定日志记录的文件路径                             |
| logfp               | 日志文件的文件指针                           | 操作日志文件的文件指针                             |
| maxlen              | 最大长度限制                                 | 设置允许的最大长度                                 |
| nolog               | 禁止日志记录的函数                           | 阻止记录日志                                       |
| os                  | 提供与操作系统交互的函数                     | 操作文件、目录等                                   |
| parse               | 解析URL的函数                                | 解析给定的URL                                      |
| parse_header        | 解析HTTP头部的函数                           | 解析HTTP请求头部                                   |
| parse_multipart     | 解析多部分HTTP请求的函数                     | 解析包含多部分内容的HTTP请求                       |
| print_arguments     | 打印参数的函数                               | 输出给定参数的信息                                 |
| print_directory     | 打印目录内容的函数                           | 列出目录中的文件和子目录                           |
| print_environ       | 打印环境变量的函数                           | 输出当前系统环境变量                               |
| print_environ_usage | 打印环境变量使用方法的函数                   | 显示环境变量的使用方法                             |
| print_exception     | 打印异常信息的函数                           | 输出异常的详细信息                                 |
| print_form          | 打印表单内容的函数                           | 显示表单提交的数据                                 |
| sys                 | 提供与Python解释器交互的函数                 | 访问和操作Python解释器的功能                       |
| tempfile            | 创建临时文件和目录的模块                     | 生成临时文件和目录                                 |
| test                | 包含测试相关的功能                           | 编写和运行测试                                     |
| urllib              | 用于处理URL的模块                            | 处理URL相关的操作                                  |
| valid_boundary      | 验证HTTP请求中的有效边界的函数               | 检查HTTP请求中的边界是否有效                       |

# 二十三、数据库

## 23.1 数据库基础

​		数据库是用于存储、管理和检索数据的系统。在Python中，你可以使用各种库来进行数据库操作。以下是数据库基础的一些概念和在Python中进行数据库操作的基本步骤：

**数据库基础概念：**

1. **数据库管理系统（DBMS）：** 数据库管理系统是一种软件，用于管理数据库，包括数据存储、检索、更新和管理等功能。常见的DBMS包括MySQL、SQLite、PostgreSQL等。

2. **表：** 表是数据库中数据的结构化存储方式，类似于电子表格中的工作表。每个表由多个列组成，每列定义了数据的类型。

3. **列：** 列是表中的一个字段，定义了数据的类型。每一行（记录）包含了不同列的数据。

4. **行（记录）：** 表中的每个数据项都存储在一行中，这个行被称为记录。

5. **主键：** 主键是表中的唯一标识符，用于唯一地标识表中的每一行。

6. **SQL：** 结构化查询语言（SQL）是用于与数据库交互的语言，包括查询、插入、更新和删除数据等操作。

**在Python中进行数据库操作的基本步骤：**

1. **导入数据库库：** 根据你使用的数据库类型，导入相应的数据库库，如`sqlite3`、`pymysql`等。

2. **连接数据库：** 使用库提供的函数连接到数据库。

3. **创建游标：** 创建一个游标对象，用于执行SQL查询和操作。

4. **执行SQL操作：** 使用游标执行SQL查询和操作，如SELECT、INSERT、UPDATE、DELETE等。

5. **获取结果：** 如果是查询操作，使用游标获取查询结果。

6. **提交更改（如果有）：** 如果进行了数据修改操作，记得使用提交命令来保存更改。

7. **关闭游标和连接：** 执行完数据库操作后，关闭游标和数据库连接。

​		以下是一个简单的示例，演示如何在Python中使用`sqlite3`库来创建一个数据库表并插入数据：

```python
import sqlite3

# 连接到数据库（如果不存在则创建）
conn = sqlite3.connect('mydatabase.db')

# 创建游标
cursor = conn.cursor()

# 创建表
cursor.execute('''
    CREATE TABLE IF NOT EXISTS users (
        id INTEGER PRIMARY KEY,
        name TEXT,
        age INTEGER
    )
''')

# 插入数据
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 25))
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Bob", 30))

# 提交更改
conn.commit()

# 关闭游标和连接
cursor.close()
conn.close()
```

​		以上示例演示了如何使用`sqlite3`库连接数据库、创建表、插入数据，并最终关闭连接。对于其他类型的数据库，操作的步骤类似，但可能需要使用不同的库和语法。



​		当使用`pymysql`库连接到MySQL数据库时，你可以按照以下步骤创建一个数据库表并插入数据：

1. 首先，确保你已经安装了`pymysql`库。可以使用以下命令安装：

```bash
pip install pymysql
```

2. 使用下面的代码示例来创建数据库表和插入数据：

```python
import pymysql

# 连接数据库
connection = pymysql.connect(
    host='localhost',      # 数据库主机地址
    user='username',       # 用户名
    password='password',   # 密码
    database='mydb'        # 数据库名称
)

# 创建游标对象
cursor = connection.cursor()

# 创建表
create_table_query = '''
    CREATE TABLE IF NOT EXISTS users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(50),
        age INT
    )
'''
cursor.execute(create_table_query)

# 插入数据
insert_query = "INSERT INTO users (name, age) VALUES (%s, %s)"
data_to_insert = [("Alice", 25), ("Bob", 30), ("Charlie", 28)]
cursor.executemany(insert_query, data_to_insert)

# 提交更改
connection.commit()

# 关闭游标和连接
cursor.close()
connection.close()
```

以上示例演示了如何使用`pymysql`库连接到MySQL数据库、创建表、插入数据，并最终关闭连接。确保将`host`、`user`、`password`和`database`替换为你的实际数据库连接信息。

## 23.2 CRDU

### 23.2.1 Creat

- 创建操作

  - **创建表：**

    创建表是存储数据的一种方式。以下示例展示了如何在SQLite数据库中创建一个名为`users`的表：

    ```python
    pythonCopy code
    create_table_query = '''
        CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY,
            name TEXT,
            age INTEGER
        )
    '''
    cursor.execute(create_table_query)
    ```

- 插入操作

  - **插入数据：**

    插入数据可以将新数据添加到表中。以下示例展示了如何在`users`表中插入数据：

  ```python
  pythonCopy code
  insert_query = "INSERT INTO users (name, age) VALUES (?, ?)"
  data_to_insert = ("Alice", 25)
  cursor.execute(insert_query, data_to_insert)
  connection.commit()  # 提交更改
  ```

### 23.2.2 Read

- 查询操作

  - 在Python中执行SQL查询通常涉及使用数据库库连接到数据库，执行查询语句并处理查询结果。以下是使用`sqlite3`和`pymysql`库进行SQL查询的示例：

    **使用sqlite3库查询：**

    ```python
    import sqlite3
    
    # 连接数据库
    connection = sqlite3.connect('mydatabase.db')
    
    # 创建游标
    cursor = connection.cursor()
    
    # 执行查询语句
    select_query = "SELECT * FROM users"
    cursor.execute(select_query)
    
    # 获取查询结果
    result = cursor.fetchall()
    
    # 处理查询结果
    for row in result:
        print(row)
    
    # 关闭游标和连接
    cursor.close()
    connection.close()
    ```

    **使用pymysql库查询：**

    ```python
    import pymysql
    
    # 连接数据库
    connection = pymysql.connect(
        host='localhost',
        user='username',
        password='password',
        database='mydb'
    )
    
    # 创建游标
    cursor = connection.cursor()
    
    # 执行查询语句
    select_query = "SELECT * FROM users"
    cursor.execute(select_query)
    
    # 获取查询结果
    result = cursor.fetchall()
    
    # 处理查询结果
    for row in result:
        print(row)
    
    # 关闭游标和连接
    cursor.close()
    connection.close()
    ```

    上述示例中，`SELECT`语句用于执行查询操作。执行后，可以使用`fetchall()`方法获取查询结果，并对结果进行处理。请注意，不同的数据库库可能会有一些差异，但基本的连接、执行查询、获取结果和关闭连接的步骤是类似的。

- 查询函数

  - 在 `pymysql` 库中，以下是 `fetchone()`、`fetchall()` 和 `rowcount` 的用法：

    - <img src="python基础md配图/image-20230809082427665.png" alt="image-20230809082427665" style="zoom:50%;" />

    - `fetchone()`: 这个方法用于从查询结果中获取一行数据，返回一个元组。如果没有更多的行可供获取，它将返回 `None`。通常用于遍历查询结果的一行一行。

    - `fetchall()`: 这个方法用于从查询结果中获取所有行的数据，返回一个包含元组的列表。如果没有更多的行可供获取，它将返回一个空列表。通常用于获取整个查询结果集。

    - `rowcount`: 这是游标对象的一个属性，表示最后一次执行的查询所影响的行数（包括插入、更新和删除操作）。对于 `SELECT` 查询语句，`rowcount` 返回结果的行数。

    以下是一个示例，展示了如何使用这些方法：

    ```python
    import pymysql
    
    def execute_query(query, db_name):
        connection = pymysql.connect(host='localhost', user='username', password='password', db=db_name)
        cursor = connection.cursor()
    
        cursor.execute(query)
        
        # 使用 fetchone() 获取一行数据
        one_row = cursor.fetchone()
        print("One Row:", one_row)
        
        # 使用 fetchall() 获取所有行数据
        all_rows = cursor.fetchall()
        print("All Rows:")
        for row in all_rows:
            print(row)
        
        # 获取受影响的行数（适用于插入、更新和删除操作）
        affected_rows = cursor.rowcount
        print("Affected Rows:", affected_rows)
    
        cursor.close()
        connection.close()
    
    # 调用查询操作函数
    query = "SELECT * FROM users"
    db_name = 'my_database'
    execute_query(query, db_name)
    ```

    在这个示例中，首先使用 `fetchone()` 获取一行数据，然后使用 `fetchall()` 获取所有行数据。最后，使用 `rowcount` 获取受影响的行数。注意，`fetchone()` 和 `fetchall()` 在查询之后被调用，而 `rowcount` 在执行完插入、更新或删除操作后才能获取到正确的值。

### 23.2.3 Delete

- 删除操作

  - **删除数据：**

    删除数据可以从表中移除数据项。以下示例展示了如何从`users`表中删除数据：

    ```python
    pythonCopy code
    delete_query = "DELETE FROM users WHERE name = ?"
    data_to_delete = ("Alice",)
    cursor.execute(delete_query, data_to_delete)
    connection.commit()  # 提交更改
    ```

### 23.2.4 Update

- 更新操作

  - **更新数据：**

    更新数据可以修改表中已有的数据。以下示例展示了如何更新`users`表中的数据：

    ```python
    pythonCopy code
    update_query = "UPDATE users SET age = ? WHERE name = ?"
    data_to_update = (30, "Alice")
    cursor.execute(update_query, data_to_update)
    connection.commit()  # 提交更改
    ```

### 23.2.5 操作函数

#### 23.2.5.1 数据库连接函数

- 创建数据库连接 

  - `connectself = pymsyql.connect(host,user,password,database)`

  - ```python
    import pymysql
    
    # 连接数据库
    connection = pymysql.connect(
        host='localhost',      # 数据库主机地址
        user='username',       # 用户名
        password='password',   # 密码
        database='mydb'        # 数据库名称
    )
    
    ```

- 提交更改

  - `connectself.commit()`

  - ```python
    # 提交更改
    conn.commit()
    ```

- 连接关闭

  - `connectself.close()`

  - ```python
    # 关闭连接
    
    conn.close()
    ```

    

#### 23.2.5.1 数据库游标函数

<img src="python基础md配图/image-20230809084728077.png" alt="image-20230809084728077" style="zoom:50%;" />

- 创建游标操作

  - `cursor = connectself.cursor()`

  - ```python
    cursor = connection.cursor()
    ```

- 游标提交操作

  - `cursor.execute('操作')`

  - ```python
    # 执行查询
    cursor.execute("SELECT * FROM users")
    results = cursor.fetchall()
    # 执行查询语句
    select_query = "SELECT * FROM users"
    cursor.execute(select_query)
    
    ## 增
    create_table_query = '''
        CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY,
            name TEXT,
            age INTEGER
        )
    '''
    cursor.execute(create_table_query)
    
    insert_query = "INSERT INTO users (name, age) VALUES (?, ?)"
    data_to_insert = ("Alice", 25)
    cursor.execute(insert_query, data_to_insert)
    connection.commit()  # 提交更改
    
    # 删
    delete_query = "DELETE FROM users WHERE name = ?"
    data_to_delete = ("Alice",)
    cursor.execute(delete_query, data_to_delete)
    connection.commit()  # 提交更改
    
    # 改
    update_query = "UPDATE users SET age = ? WHERE name = ?"
    data_to_update = (30, "Alice")
    cursor.execute(update_query, data_to_update)
    connection.commit()  # 提交更改
    ```

    

- 游标查询操作

  - 在 `pymysql` 库中，以下是 `fetchone()`、`fetchall()` 和 `rowcount` 的用法：

    - <img src="python基础md配图/image-20230809082427665.png" alt="image-20230809082427665" style="zoom:50%;" />

    - `fetchone()`: 这个方法用于从查询结果中获取一行数据，返回一个元组。如果没有更多的行可供获取，它将返回 `None`。通常用于遍历查询结果的一行一行。

    - `fetchall()`: 这个方法用于从查询结果中获取所有行的数据，返回一个包含元组的列表。如果没有更多的行可供获取，它将返回一个空列表。通常用于获取整个查询结果集。

    - `rowcount`: 这是游标对象的一个属性，表示最后一次执行的查询所影响的行数（包括插入、更新和删除操作）。对于 `SELECT` 查询语句，`rowcount` 返回结果的行数。

    以下是一个示例，展示了如何使用这些方法：

    ```python
    import pymysql
    
    def execute_query(query, db_name):
        connection = pymysql.connect(host='localhost', user='username', password='password', db=db_name)
        cursor = connection.cursor()
    
        cursor.execute(query)
        
        # 使用 fetchone() 获取一行数据
        one_row = cursor.fetchone()
        print("One Row:", one_row)
        
        # 使用 fetchall() 获取所有行数据
        all_rows = cursor.fetchall()
        print("All Rows:")
        for row in all_rows:
            print(row)
        
        # 获取受影响的行数（适用于插入、更新和删除操作）
        affected_rows = cursor.rowcount
        print("Affected Rows:", affected_rows)
    
        cursor.close()
        connection.close()
    
    # 调用查询操作函数
    query = "SELECT * FROM users"
    db_name = 'my_database'
    execute_query(query, db_name)
    ```

    在这个示例中，首先使用 `fetchone()` 获取一行数据，然后使用 `fetchall()` 获取所有行数据。最后，使用 `rowcount` 获取受影响的行数。注意，`fetchone()` 和 `fetchall()` 在查询之后被调用，而 `rowcount` 在执行完插入、更新或删除操作后才能获取到正确的值。

- 游标关闭操作

  - `cursor.close()`

  - ```python
    # 关闭连接
    cursor.close()
    ```

    

### 23.3.1 数据处理和分析

​		数据库数据处理和分析是指在数据库中存储的大量数据中，通过查询、统计、分析等方法，从中获取有价值的信息和洞察，以支持业务决策、趋势预测、问题解决等活动。以下是数据库数据处理和分析的一些常见方法和步骤：

- **数据查询：** 使用SQL语句查询数据库中的数据，从中获取特定条件下的记录。可以使用SELECT语句来选择需要的数据。

- **数据过滤和排序：** 使用WHERE子句进行数据过滤，选择满足特定条件的数据。使用ORDER BY子句对结果进行排序，以便更好地分析和展示数据。

- **聚合和统计：** 使用聚合函数如SUM、AVG、COUNT、MAX、MIN等进行数据统计。通过GROUP BY子句对数据进行分组，从而进行分组统计分析。

- **数据透视表：** 在支持的数据库系统中，可以使用数据透视表来汇总和分析数据，以展示数据的不同维度和指标。

- **窗口函数：** 使用窗口函数来在数据集内执行计算，如计算排名、累计求和等，以支持更复杂的数据分析需求。

- **数据可视化：** 使用图表、图形和报表等方式将数据可视化，以更直观地呈现数据分析结果。常见的数据可视化工具包括Matplotlib、Seaborn、Tableau等。

- **数据挖掘：** 在数据中寻找隐藏的模式、关联和规律，以发现有用的信息。数据挖掘技术包括聚类、分类、预测等。

- **业务分析：** 将数据分析与业务需求结合，以支持业务决策和战略规划。通过对数据的深入分析，提供有关市场趋势、客户行为等方面的洞察。

- **趋势分析：** 通过对历史数据的分析，预测未来的趋势和发展方向。可以使用时间序列分析等方法进行趋势预测。

- **异常检测：** 分析数据中的异常值，寻找数据中的异常模式和异常行为，以及可能的数据质量问题。

​		数据库数据处理和分析需要灵活运用SQL查询、数据处理工具和分析算法，以适应不同的业务场景和数据特点。有效的数据处理和分析可以帮助企业更好地理解其数据，做出更明智的决策，并发现潜在的机会和挑战。

### 23.3.2 查询处理和分析

#### 23.3.2.1 操作方式	

这些操作是在数据库中进行数据处理和分析时常用的操作，下面我将为每个操作提供简要的说明：

- **聚合（Aggregation）：**

​		聚合操作用于计算多行数据的统计值，如求和、平均值、最大值、最小值等。在SQL中，使用聚合函数（如SUM、AVG、MAX、MIN）对数据进行聚合操作。

示例：
```sql
SELECT SUM(salary) FROM employees;
```

- **分组（Grouping）：**

​		分组操作将数据按照指定的列进行分组，并对每个分组应用聚合函数。这常用于统计每个组的汇总信息。

示例：
```sql
SELECT department, AVG(salary) FROM employees GROUP BY department;
```

- **关联（Joining）：**

​		关联操作将多个表中的数据连接在一起，基于某些条件关联数据。这常用于从多个表中获取关联的信息。

示例：
```sql
SELECT employees.name, departments.name
FROM employees
INNER JOIN departments ON employees.department_id = departments.id;
```

- **排序（Sorting）：**

​		排序操作用于按照指定的列对数据进行排序，可以是升序或降序排列。

示例：
```sql
SELECT name, age FROM users ORDER BY age DESC;
```

这些操作在数据库中非常常见，可以帮助你有效地查询和分析数据。根据不同的业务需求，你可以使用这些操作来获取所需的数据。

#### 23.3.2.2 举例 （薪资 职员）

当使用 `pymysql` 连接 MySQL 数据库时，可以利用 SQL 查询语句来进行聚合、分组、关联和排序操作。以下是这些操作的示例代码：

- **聚合操作示例**：

```python
import pymysql

# 连接数据库
connection = pymysql.connect(host='localhost', user='username', password='password', db='my_database')
cursor = connection.cursor()

# 使用 SUM 函数进行聚合操作
query = "SELECT SUM(salary) FROM employees"
cursor.execute(query)
total_salary = cursor.fetchone()[0]
print("Total Salary:", total_salary)

# 关闭数据库连接
cursor.close()
connection.close()
```

- **分组操作示例**：

```python
# 连接数据库
connection = pymysql.connect(host='localhost', user='username', password='password', db='my_database')
cursor = connection.cursor()

# 使用 GROUP BY 子句进行分组操作
query = "SELECT department, AVG(salary) FROM employees GROUP BY department"
cursor.execute(query)
department_avg_salary = cursor.fetchall()
for row in department_avg_salary:
    print("Department:", row[0], "Average Salary:", row[1])

# 关闭数据库连接
cursor.close()
connection.close()
```

- **关联操作示例**：

```python
# 连接数据库
connection = pymysql.connect(host='localhost', user='username', password='password', db='my_database')
cursor = connection.cursor()

# 使用 INNER JOIN 进行关联操作
query = "SELECT employees.name, departments.name FROM employees INNER JOIN departments ON employees.department_id = departments.id"
cursor.execute(query)
employee_department = cursor.fetchall()
for row in employee_department:
    print("Employee:", row[0], "Department:", row[1])

# 关闭数据库连接
cursor.close()
connection.close()
```

- **排序操作示例**：
  - <img src="python基础md配图/image-20230809090812975.png" alt="image-20230809090812975" style="zoom:50%;" />
  - <img src="python基础md配图/image-20230809090844744.png" alt="image-20230809090844744" style="zoom:50%;" />

```python
# 连接数据库
connection = pymysql.connect(host='localhost', user='username', password='password', db='my_database')
cursor = connection.cursor()

# 使用 ORDER BY 子句进行排序操作
  query = "SELECT name, salary FROM employees ORDER BY salary DESC"
cursor.execute(query)
sorted_employees = cursor.fetchall()
for row in sorted_employees:
    print("Name:", row[0], "Salary:", row[1])

# 关闭数据库连接
cursor.close()
connection.close()
```

在每个示例中，我们首先建立了数据库连接，然后执行 SQL 查询，并通过 `cursor` 对象获取查询结果。最后，我们关闭了数据库连接。注意，在实际使用时，你需要根据你的数据库配置进行相应的修改。



## 23.4 事物

### 23.4.1 事物概念

​		数据库事务（Transaction）是一组数据库操作的集合，这些操作要么全部执行成功，要么全部不执行，以保证数据库的一致性和完整性。事务是数据库管理系统（DBMS）中的一个重要概念，用于处理数据库操作的原子性、一致性、隔离性和持久性，通常被缩写为 ACID。

​		ACID 是数据库事务的四个特性：

1. 原子性（Atomicity）：事务中的所有操作要么全部执行成功，要么全部不执行。如果其中任何一个操作失败，整个事务都会被回滚，以保持数据库的一致性。

2. 一致性（Consistency）：事务开始之前和结束之后，数据库的状态应该保持一致。事务的执行不会破坏数据库的完整性约束。

3. 隔离性（Isolation）：多个事务可以并发执行，但它们之间应该相互隔离，一个事务的操作对其他事务应该是透明的。事务的隔离性保证了数据的一致性。

4. 持久性（Durability）：一旦事务提交成功，其所做的更改应该在数据库中持久存在，即使系统崩溃也不会丢失。

​		在数据库中，你可以通过使用事务来组织一系列数据库操作，以确保数据的正确性和安全性。事务可以用于保证在复杂的数据库操作中，要么全部操作成功提交，要么全部操作回滚，以防止数据库中的数据损坏或不一致。

​		在 Python 中，你可以使用数据库的连接库（如 `pymysql`、`sqlite3`、`psycopg2` 等）来执行事务操作。事务的基本使用方式如上面的回答中所示。

		在 `pymysql` 中，你可以使用事务来确保一系列数据库操作的原子性，即要么所有操作都成功执行，要么都不执行。事务可以用于处理数据库中的复杂操作，保证数据的一致性和完整性。

以下是一个使用 `pymysql` 进行数据库事务的示例代码：

```python
import pymysql

# 连接数据库
connection = pymysql.connect(host='localhost', user='username', password='password', db='my_database')
cursor = connection.cursor()

try:
    # 开始事务
    connection.begin()

    # 执行多个数据库操作，如插入、更新等
    update_query = "UPDATE employees SET salary = salary + 1000 WHERE department = 'HR'"
    cursor.execute(update_query)

    insert_query = "INSERT INTO employees (name, department, salary) VALUES ('New Employee', 'IT', 5000)"
    cursor.execute(insert_query)

    # 提交事务
    connection.commit()
    print("Transaction committed successfully")

except Exception as e:
    # 回滚事务
    connection.rollback()
    print("Transaction rolled back due to:", str(e))

finally:
    # 关闭数据库连接
    cursor.close()
    connection.close()
```

在这个示例中，我们首先连接数据库并获取一个 cursor 对象。然后，我们使用 `connection.begin()` 开始一个事务，并执行了两个数据库操作（更新和插入）。如果所有操作都成功执行，我们使用 `connection.commit()` 提交事务。如果发生了任何异常，我们使用 `connection.rollback()` 回滚事务，以确保不会影响数据库的状态。最后，我们关闭了数据库连接。

注意：在实际使用时，你需要根据你的数据库配置进行相应的修改。同时，为了确保事务的有效性，你应该根据实际需求进行适当的异常处理和回滚操作。

### 23.4.2 事物函数

- 结合异常函数

- connectself.begin()  connectself.rollback()

  - ```python
    try:
    	
    	 connectself.begin()
    	 
    	 '''
    	 #操作
    	 '''
        
       connectself.commit()
      
    except Erro as e:
         
       connect.rollback()
      
    finally:
      
       connectself.close()
    
       
    ```

## 23.5 错误处理



## 23.6 数据库设计

### 23.6.1 设计过程

| 步骤       | 描述                                               |
| ---------- | -------------------------------------------------- |
| 需求分析   | 确定应用程序需求，定义数据实体、属性和关系。       |
| 概念设计   | 创建概念模型，使用EER图或ERD表示数据结构和关系。   |
| 逻辑设计   | 将概念模型转化为关系模型，定义数据库表格和关系。   |
| 物理设计   | 选择数据库管理系统、数据类型、索引、存储结构等。   |
| 规范化     | 将数据库设计规范化，消除冗余数据，确保数据一致性。 |
| 实施       | 根据设计创建数据库表格、字段、约束和索引。         |
| 测试和优化 | 测试数据库数据的正确性和一致性，优化性能。         |
| 数据迁移   | 将现有数据迁移到新设计的数据库中。                 |

​		这个表格概括了数据库设计的各个步骤以及每个步骤的主要内容。数据库设计是一个综合性的过程，需要在不同层次上考虑数据的结构、关系、性能和安全等方面。

        数据库设计是指在创建数据库时，定义数据库的结构、表格、关系、字段和约束等，以满足特定应用程序的需求并提供高效的数据存储和访问方式。良好的数据库设计能够确保数据的一致性、完整性和安全性，以及提高数据库的性能和可维护性。

​		数据库设计的过程通常包括以下几个步骤：

1. 需求分析：了解应用程序的需求，确定数据实体、属性、关系和业务规则。

2. 概念设计：绘制概念模型，使用实体-属性-关系（EER）图或实体关系图（ERD）来表示数据实体、属性和它们之间的关系。

3. 逻辑设计：将概念模型转化为数据库管理系统能够理解的模型，通常使用关系模型（表格）表示实体和属性，定义关系（外键）来表示实体之间的关联。

4. 物理设计：选择数据库管理系统、数据类型、索引、存储结构等，以优化数据库的性能和存储效率。

5. 规范化：将数据库设计进行规范化，消除冗余数据并确保数据的一致性和完整性。规范化通常分为多个范式，如第一范式（1NF）、第二范式（2NF）、第三范式（3NF）等。

6. 实施：根据逻辑设计和物理设计，创建数据库表格、定义字段、约束和索引等。

7. 测试和优化：对数据库进行测试，确保数据的正确性和一致性。根据性能测试结果进行优化，以提高数据库的响应速度和效率。

8. 数据迁移：将现有数据迁移到新设计的数据库中，确保数据的平稳过渡。

​		在数据库设计中，需要考虑数据的完整性、安全性、性能以及未来的扩展需求。良好的数据库设计可以减少数据冗余、提高数据质量，并为应用程序提供更好的数据支持。



### 23.6.2 范式设计

​		当进行数据库规范化的过程中，我们需要按照不同的范式逐步对数据库设计进行调整，以减少数据冗余、提高数据质量和维护性。以下是规范化过程的细化步骤：

- **第一范式（1NF）：** 确保每个列都包含原子值，不可再分。将重复的列和组合列拆分为单独的列。

   - 将表格中的重复数据拆分为多个行，并将原来的数据作为主键的一部分。
   - 确保每个单元格只包含一个值。

- **第二范式（2NF）：** 确保非主键列完全依赖于主键。消除部分依赖。

   - 将部分依赖的列拆分到其他表格，并与其相关的主键建立关联。
   - 确保每个非主键列都完全依赖于整个主键。
   - 举例 **（属性由多个ID或元素确定）**

     - 在数据库设计中，当一个非主键列（属性）完全依赖于主键列时，这种依赖关系称为函数依赖。函数依赖是指在一个关系（表格）中，一个或多个属性的值可以唯一地确定其他属性的值。具体而言，非主键列的值取决于主键列的值，而不受其他非主键列的影响。

       让我通过一个例子来说明非主键列完全依赖于主键：

       考虑一个学生课程成绩表格，其中包含学生的学号（主键）、课程号（主键）以及成绩信息。

       **学生课程成绩表格（StudentCourses）：**
       | 学号 | 课程号 | 成绩 |
       | ---- | ------ | ---- |
       | 101  | 001    | 85   |
       | 101  | 002    | 92   |
       | 102  | 001    | 78   |

       在这个例子中，学号和课程号构成了联合主键，而成绩是非主键列。可以观察到，成绩完全依赖于学号和课程号。换句话说，对于每一对学号和课程号的组合，成绩是唯一确定的，不受其他属性的影响。

       这种情况下的函数依赖可以表示为：
       ```
       学号, 课程号 -> 成绩
       ```

       在数据库设计中，通常会尽量避免非主键列对主键的完全函数依赖。因为如果存在这种依赖，可能会导致数据冗余和不一致性。如果非主键列的值只与主键有关，那么将其合并到主键中是一个更好的设计选择。

- **第三范式（3NF）：** 消除传递依赖，确保非主键列之间没有传递的关系。

   - 将非主键列之间的传递依赖拆分到其他表格中，与相关的主键建立关联。
   - 确保每个非主键列只依赖于主键或其他非主键列，没有传递依赖关系。
   - 举例 **（属性受不同表中的ID影响 ）**

     - 

       让我通过一个例子来说明传递依赖：

       假设有一个学生选课系统的数据库，其中有以下两个表格：学生表格（Students）和课程表格（Courses）。

       **学生表格（Students）：**
       | 学生ID | 姓名 | 班级 |
       | ------ | ---- | ---- |
       | 1      | 小明 | 10班 |
       | 2      | 小红 | 11班 |
       | 3      | 小李 | 10班 |

       **课程表格（Courses）：**
       | 课程ID | 课程名 | 班级 |
       | ------ | ------ | ---- |
       | 101    | 数学   | 10班 |
       | 102    | 英语   | 11班 |
       | 103    | 物理   | 10班 |

       在这个例子中，学生表格中的班级字段和课程表格中的班级字段都表示班级信息。如果我们设计时不注意，可能会造成传递依赖。例如，**课程表格中的班级字段依赖于学生表格中的班级字段，而学生表格中的班级字段又依赖于学生ID字段**。

       为了消除这种传递依赖，可以进行规范化，将班级信息提取到一个单独的表格中，例如“班级表格（Classes）”。

       **班级表格（Classes）：**
       | 班级ID | 班级 |
       | ------ | ---- |
       | 1      | 10班 |
       | 2      | 11班 |

       然后，学生表格和课程表格中的班级字段分别与班级表格中的班级ID字段关联。这样，就消除了传递依赖，每个字段都只依赖于主键字段，数据库结构更加规范。

       通过消除传递依赖，我们可以避免数据冗余和不一致性，提高数据库的稳定性和可维护性。

- **巴斯-科德范式（BCNF）：** 消除主键列之间的部分依赖。

   - 将主键列之间的部分依赖拆分到其他表格中，与相关的主键建立关联。
   - 确保每个主键列只依赖于整个主键。

     - 在数据库设计中，消除主键列之间的部分依赖是为了达到范式化的要求，尤其是第二范式（2NF）的要求。部分依赖是指非主键属性依赖于主键的一部分，而不是全部主键。

       以下是一个示例，说明如何消除主键列之间的部分依赖：

       考虑一个订单信息表格，其中包含订单号（主键）、产品号（主键）、产品名称和客户信息。

       **订单信息表格（Orders）：**
       | 订单号 | 产品号 | 产品名称 | 客户信息 |
       | ------ | ------ | -------- | -------- |
       | 1001   | 001    | 商品A    | 客户X    |
       | 1001   | 002    | 商品B    | 客户X    |
       | 1002   | 001    | 商品A    | 客户Y    |

       在这个例子中，订单号和产品号构成了联合主键，而产品名称和客户信息是非主键列。可以观察到，产品名称部分依赖于产品号，而不仅仅依赖于订单号。因此，存在部分依赖的情况。

       为了消除这种部分依赖，我们可以将产品信息独立出来，创建一个单独的产品表格，并将其与订单表格进行关联。这样可以确保产品信息只与产品号有关，而不再依赖于订单号。

       **订单表格（Orders）：**
       | 订单号 | 产品号 | 客户信息 |
       | ------ | ------ | -------- |
       | 1001   | 001    | 客户X    |
       | 1001   | 002    | 客户X    |
       | 1002   | 001    | 客户Y    |

       **产品表格（Products）：**
       | 产品号 | 产品名称 |
       | ------ | -------- |
       | 001    | 商品A    |
       | 002    | 商品B    |

       通过这种设计，我们消除了主键列之间的部分依赖，同时也将数据分散到不同的表格中，提高了数据的一致性和范式化程度。

- **第四范式（4NF）：** 消除多值依赖，确保每个非主键列只依赖于主键。

   - 将多值依赖的列拆分到其他表格中，与相关的主键建立关联。

     - 每个范式的细化步骤都涉及到将数据拆分为更小、更精确的部分，以消除不必要的冗余和依赖关系。在进行规范化过程时，我们需要深入了解数据库中数据的业务逻辑，以确保设计出合理、高效且易于维护的数据库结构。

       



​		需要注意的是，虽然规范化可以提高数据质量，但有时过度规范化可能会导致查询性能下降。在设计数据库时，需要根据实际情况权衡范式化和性能之间的平衡。		





## 23.7 数据库调优

| 调优方法         | 描述                                                         |
| ---------------- | ------------------------------------------------------------ |
| 索引优化         | 确保适当的字段有索引，提高查询速度，但需要平衡索引的数量。   |
| 查询优化         | 编写高效的查询语句，使用适当的条件和关联操作，避免全表扫描。 |
| 表设计优化       | 将数据拆分成合适的表格，避免冗余数据和不必要的关联。         |
| 硬件优化         | 使用高性能硬件和存储设备，确保服务器有足够资源。             |
| 内存管理         | 配置内存参数，缓存热门数据，减少磁盘IO。                     |
| 磁盘IO优化       | 使用RAID、分区、磁盘缓存等方式提高磁盘IO性能。               |
| 并发控制优化     | 使用乐观锁或悲观锁控制并发访问，避免数据冲突。               |
| 数据库缓存       | 使用缓存系统如Redis，加速读取操作。                          |
| 定期维护         | 定期备份、清理和优化，保持数据库健康。                       |
| 分区和分片       | 对大型表进行分区或分片，提高查询性能和扩展性。               |
| 批量处理         | 使用批量操作处理大量数据，减少单条记录操作。                 |
| 监控和分析       | 使用性能监控工具，定期分析性能指标，解决问题。               |
| 适当的数据类型   | 使用适当的数据类型，减少存储空间和计算开销。                 |
| 规范化和反规范化 | 根据业务需求，合理使用规范化和反规范化，平衡数据存储和查询性能。 |

- 乐观锁悲观锁

  - ​		当使用乐观锁（Optimistic Locking）时，假设并发冲突很少发生。在更新记录之前，你会检查记录的版本号是否与你读取的版本号相匹配。如果匹配，就进行更新操作；如果不匹配，说明在此期间另一个事务已经修改了该记录。

    ​		以下是一个使用乐观锁的 Python 示例代码：

    ```python
    import pymysql
    
    def update_record(connection, cursor, record_id, new_value, current_version):
        try:
            cursor.execute("UPDATE records SET value=%s WHERE id=%s AND version=%s",
                           (new_value, record_id, current_version))
            connection.commit()
            print("记录更新成功。")
        except pymysql.IntegrityError:
            connection.rollback()
            print("乐观锁冲突，记录已被其他事务更新。")
    
    # 使用示例
    connection = pymysql.connect(host='localhost', user='username', password='password', database='mydb')
    cursor = connection.cursor()
    
    record_id = 1
    new_value = "新值"
    current_version = 1  # 假设之前读取过这个版本号
    
    update_record(connection, cursor, record_id, new_value, current_version)
    
    cursor.close()
    connection.close()
    ```

    ​		悲观锁（Pessimistic Locking）假设并发冲突会更频繁发生，因此在执行任何操作之前会先锁定数据。其他事务必须等待锁释放后才能访问数据。

    ​		以下是一个使用悲观锁的 Python 示例代码：

    ```python
    import pymysql
    
    def update_record_with_lock(connection, cursor, record_id):
        try:
            cursor.execute("SELECT * FROM records WHERE id=%s FOR UPDATE", (record_id,))
            # 在这里进行必要的更新操作
            connection.commit()
            print("记录更新成功。")
        except:
            connection.rollback()
            print("更新记录时出现错误。")
    
    # 使用示例
    connection = pymysql.connect(host='localhost', user='username', password='password', database='mydb')
    cursor = connection.cursor()
    
    record_id = 1
    
    update_record_with_lock(connection, cursor, record_id)
    
    cursor.close()
    connection.close()
    ```

    ​		在乐观锁示例中，我们在更新记录之前先检查了版本号。而在悲观锁示例中，我们在 SQL 语句中使用了 `FOR UPDATE` 子句，以便在更新之前先锁定了记录。

    

-  数据库缓存

  - ​		当涉及数据库缓存时，代码的具体实现会依赖于所使用的缓存技术和数据库管理系统。以下是一个简单的示例，使用 Python 的 `redis` 库来实现查询缓存：

    ```python
    import redis
    import pymysql
    
    # 创建数据库连接
    db_conn = pymysql.connect(host='localhost', user='username', password='password', database='mydb')
    cursor = db_conn.cursor()
    
    # 创建 Redis 连接
    redis_conn = redis.StrictRedis(host='localhost', port=6379, db=0)
    
    def get_data_from_database(query):
        # 尝试从缓存获取数据
        cached_data = redis_conn.get(query)
        if cached_data:
            return cached_data.decode('utf-8')
        
        # 如果缓存中没有数据，则从数据库查询数据
        cursor.execute(query)
        result = cursor.fetchall()
        
        # 将查询结果存储到缓存中，设置过期时间
        redis_conn.setex(query, 60, str(result))
        
        return result
    
    # 示例查询语句
    query = "SELECT * FROM users WHERE age > 25"
    
    # 首次查询会从数据库获取数据并存储到缓存中
    data = get_data_from_database(query)
    print(data)
    
    # 第二次查询可以直接从缓存中获取数据
    cached_data = get_data_from_database(query)
    print(cached_data)
    
    # 关闭数据库连接
    cursor.close()
    db_conn.close()
    ```

    ​		请注意，这只是一个简单的示例，实际中还需要考虑缓存数据的更新和过期机制，以及保证数据一致性等问题。对于更复杂的应用场景，可能需要使用专门的缓存服务器或其他缓存管理工具。

    

- 定期维护

  - ​		当涉及到数据库定期维护时，大部分任务需要使用数据库管理系统的特定工具或SQL命令进行操作。以下是一些典型的数据库维护任务的代码示例（以MySQL为例）：

    1. **备份数据库：**

    ```python
    import subprocess
    
    backup_command = "mysqldump -u username -p password dbname > backup.sql"
    subprocess.run(backup_command, shell=True)
    ```

    2. **优化查询：**

    ```python
    from sqlalchemy import create_engine
    from sqlalchemy.orm import sessionmaker
    
    engine = create_engine("mysql://username:password@localhost/dbname")
    Session = sessionmaker(bind=engine)
    session = Session()
    
    # 执行优化查询
    # ...
    
    session.close()
    ```

    3. **定期清理数据：**

    ```python
    from sqlalchemy import create_engine
    from sqlalchemy.orm import sessionmaker
    from myapp.models import DataModel
    
    engine = create_engine("mysql://username:password@localhost/dbname")
    Session = sessionmaker(bind=engine)
    session = Session()
    
    # 删除过期数据
    session.query(DataModel).filter(DataModel.timestamp < threshold).delete()
    
    session.commit()
    session.close()
    ```

    4. **更新统计信息：**

    ```python
    from sqlalchemy import create_engine
    from sqlalchemy.orm import sessionmaker
    
    engine = create_engine("mysql://username:password@localhost/dbname")
    Session = sessionmaker(bind=engine)
    session = Session()
    
    # 更新统计信息
    session.execute("ANALYZE TABLE tablename")
    
    session.close()
    ```

    5. **碎片整理：**

    ```python
    import subprocess
    
    optimize_command = "mysqlcheck -u username -p password --optimize dbname"
    subprocess.run(optimize_command, shell=True)
    ```

    ​		以上示例中的代码片段演示了不同维护任务的大致操作。实际操作中，请根据数据库类型和需求进行相应的调整和优化。同时，一些任务可能需要在特定的时间段内运行，以避免对生产环境造成干扰。

- 分区和分片

  - 分区和分片是数据库和数据存储领域的术语，它们有些类似但又有一些不同之处。下面我将为你提供一些关于分区和分片的解释以及示例代码。

    ### 分区（Partitioning）：

    分区是将数据库表或索引逻辑地划分为更小、更可管理的部分，每个部分称为一个分区。分区可以基于特定的列值来划分数据，这有助于提高查询性能和数据管理。不同数据库管理系统（DBMS）有不同的分区方式，比如按范围、哈希、列表等。

    #### 示例代码（MySQL 分区）：

    ```python
    import pymysql
    
    # 连接数据库
    connection = pymysql.connect(host='localhost', user='username', password='password', db='mydb')
    
    # 创建分区表
    create_table_query = """
    CREATE TABLE employees (
        id INT NOT NULL,
        first_name VARCHAR(50),
        last_name VARCHAR(50),
        hire_date DATE
    ) PARTITION BY RANGE (YEAR(hire_date)) (
        PARTITION p0 VALUES LESS THAN (1990),
        PARTITION p1 VALUES LESS THAN (2000),
        PARTITION p2 VALUES LESS THAN (2010),
        PARTITION p3 VALUES LESS THAN MAXVALUE
    )
    """
    
    with connection.cursor() as cursor:
        cursor.execute(create_table_query)
        connection.commit()
    
    # 插入数据
    insert_query = """
    INSERT INTO employees (id, first_name, last_name, hire_date) VALUES
    (1, 'John', 'Doe', '1985-05-15'),
    (2, 'Jane', 'Smith', '2005-08-20'),
    (3, 'Michael', 'Johnson', '2015-03-10')
    """
    
    with connection.cursor() as cursor:
        cursor.execute(insert_query)
        connection.commit()
    
    # 查询特定分区的数据
    query = "SELECT * FROM employees PARTITION (p1)"
    
    with connection.cursor() as cursor:
        cursor.execute(query)
        result = cursor.fetchall()
        print(result)
    
    # 关闭连接
    connection.close()
    ```

    ### 分片（Sharding）：

    分片是将数据水平分割成多个部分，每个部分被称为一个分片，然后将这些分片分布在不同的数据库服务器上。分片有助于处理大规模数据，提高数据库的可伸缩性和性能。

    #### 示例代码（简化的分片示例）：

    假设我们有三个数据库服务器，每个服务器上存储不同的用户数据。

    ```python
    # Server 1
    server1_users = [
        {"id": 1, "name": "Alice", "email": "alice@example.com"},
        {"id": 2, "name": "Bob", "email": "bob@example.com"}
    ]
    
    # Server 2
    server2_users = [
        {"id": 3, "name": "Charlie", "email": "charlie@example.com"},
        {"id": 4, "name": "David", "email": "david@example.com"}
    ]
    
    # Server 3
    server3_users = [
        {"id": 5, "name": "Eve", "email": "eve@example.com"},
        {"id": 6, "name": "Frank", "email": "frank@example.com"}
    ]
    
    # 根据用户ID计算分片
    def get_shard(user_id):
        if user_id <= 2:
            return server1_users
        elif user_id <= 4:
            return server2_users
        else:
            return server3_users
    
    # 查询用户数据
    def get_user_by_id(user_id):
        shard = get_shard(user_id)
        for user in shard:
            if user["id"] == user_id:
                return user
        return None
    
    user_id = 3
    user = get_user_by_id(user_id)
    print(user)
    ```

    请注意，上述示例中的代码只是一个简化的模拟，实际上分片的实现可能更加复杂，并涉及到数据库连接、负载均衡等内容。

- 批量处理

  - ​		批量处理是一种常见的数据处理方式，可以有效地减少单个操作的开销，提高处理效率。在数据库操作中，批量处理通常是指一次性执行多个操作，如插入、更新、删除等，以减少与数据库服务器的交互次数，从而提高性能。

    下面是一个示例代码，展示如何使用 Python 中的 `pymysql` 库进行数据库批量插入操作：

    ```python
    import pymysql
    
    # 连接数据库
    connection = pymysql.connect(host='localhost', user='username', password='password', db='mydb')
    
    # 创建数据
    data_to_insert = [
        ("John", "Doe", "john@example.com"),
        ("Jane", "Smith", "jane@example.com"),
        ("Michael", "Johnson", "michael@example.com")
    ]
    
    # 批量插入
    insert_query = "INSERT INTO users (first_name, last_name, email) VALUES (%s, %s, %s)"
    
    with connection.cursor() as cursor:
        cursor.executemany(insert_query, data_to_insert)
        connection.commit()
    
    # 关闭连接
    connection.close()
    ```

    ​		在这个示例中，我们首先连接到数据库，然后创建了一组待插入的数据 `data_to_insert`。然后，我们使用 `executemany` 函数来一次性插入多个数据行，这样可以减少与数据库的交互次数。

    ​		请注意，具体的代码可能需要根据你的数据库表结构和数据进行调整。此外，类似的批量处理方法也适用于其他数据库操作，如批量更新、批量删除等。

- 监控和分析

  - 监控和分析是在软件开发和系统运维中非常重要的环节，用于监测应用程序、系统性能以及用户行为，以便及时发现问题、优化性能并做出决策。以下是监控和分析的一些常见方法和工具：

    **监控方法：**

    1. **日志记录：** 记录应用程序和系统的运行日志，有助于跟踪问题、排除故障和分析错误。

    2. **性能监控：** 使用性能监控工具来收集系统的性能指标，如 CPU 使用率、内存占用、网络流量等，以便发现资源瓶颈和性能问题。

    3. **实时监控：** 使用实时监控工具来实时地监控应用程序的运行状态，如实时监测请求响应时间、流量情况等。

    4. **用户行为监控：** 通过用户行为监控工具，了解用户在应用中的操作和行为，从而改进用户体验。

    **分析方法：**

    1. **数据分析：** 使用数据分析工具来处理和分析收集到的数据，挖掘有价值的信息，发现潜在问题和趋势。

    2. **性能分析：** 对系统性能进行分析，找出瓶颈和性能瓶颈，以便进行优化。

    3. **错误分析：** 分析应用程序的错误日志，找出可能的错误源并进行修复。

    4. **用户行为分析：** 分析用户的行为模式和使用情况，为改进产品和服务提供数据支持。

    **监控和分析工具：**

    1. **日志分析工具：** 如ELK Stack (Elasticsearch, Logstash, Kibana)、Splunk，用于集中管理和分析日志数据。

    2. **性能监控工具：** 如Prometheus、Grafana、New Relic，用于监控应用程序和系统的性能指标。

    3. **实时监控工具：** 如Nagios、Zabbix，可以实时地监控网络设备和应用程序。

    4. **用户行为分析工具：** 如Google Analytics、Mixpanel，用于跟踪用户在应用中的操作和行为。

    5. **数据分析工具：** 如Python的Pandas、R语言，用于数据的处理和分析。

    6. **性能分析工具：** 如Profiler、FlameGraph，用于分析应用程序性能。

    总之，监控和分析是保持系统和应用程序健康的关键步骤，它们可以帮助你在早期发现问题、优化性能并做出有根据的决策。

  - ​        当涉及到监控和分析时，代码的具体实现会因不同的应用场景和工具而异。以下是一个使用Python和Prometheus监控库来进行基本性能监控的简单示例：

    ```python
    from prometheus_client import start_http_server, Summary, Counter
    import random
    import time
    
    # 初始化性能指标
    REQUEST_TIME = Summary('request_processing_seconds', 'Time spent processing request')
    REQUEST_COUNTER = Counter('request_count', 'Total request count')
    
    # 模拟一个耗时操作
    @REQUEST_TIME.time()
    def process_request():
        time.sleep(random.uniform(0.1, 0.5))
        REQUEST_COUNTER.inc()
    
    if __name__ == '__main__':
        # 启动Prometheus HTTP服务
        start_http_server(8000)
        
        # 模拟请求处理
        while True:
            process_request()
    ```

    ​		在上面的示例中，我们使用了`prometheus_client`库来定义了一个性能指标`REQUEST_TIME`，用于记录请求处理时间，并定义了一个计数器`REQUEST_COUNTER`，用于记录请求总数。然后，我们模拟了一个耗时操作`process_request()`，并使用`@REQUEST_TIME.time()`装饰器来记录操作的执行时间。最后，我们在主循环中持续模拟请求的处理。

    ​		通过运行这段代码，你可以在浏览器中访问`http://localhost:8000`来查看Prometheus提供的监控数据，包括请求处理时间和请求总数等指标。

    ​		请注意，这只是一个简单的示例，实际上在监控和分析方面可能会涉及更复杂的应用场景和工具，具体的代码实现会根据需求和工具而有所不同。

- 适当的数据类型

  - ​		在数据库设计和数据处理中，选择适当的数据类型非常重要，它能够影响数据库性能、数据存储以及数据的完整性。以下是一些常见的数据库数据类型以及它们的用途：

    | 数据类型 | 描述和用途                                     |
    | -------- | ---------------------------------------------- |
    | INT      | 整数型数据，用于存储整数值                     |
    | BIGINT   | 用于存储大范围的整数值                         |
    | FLOAT    | 浮点数型数据，用于存储小数值                   |
    | DECIMAL  | 用于精确存储小数值，适用于货币、精确计算等场景 |
    | VARCHAR  | 可变长度字符串，适用于文本数据                 |
    | CHAR     | 定长字符串，适用于存储固定长度的字符串         |
    | TEXT     | 适用于存储大段文本数据                         |
    | DATE     | 日期数据类型，用于存储日期                     |
    | TIME     | 时间数据类型，用于存储时间                     |
    | DATETIME | 日期时间数据类型，用于存储日期和时间           |
    | BOOLEAN  | 布尔数据类型，用于存储真/假值                  |
    | ENUM     | 枚举数据类型，用于存储有限的选项值             |
    | JSON     | 用于存储非结构化或半结构化的数据               |
    | BLOB     | 二进制大对象，适用于存储图像、音频等二进制数据 |
    | UUID     | 用于存储唯一标识符                             |

    ​		在选择数据类型时，需要根据具体的业务需求和数据特点来决定。例如，如果需要存储小数值并且需要保持精确性，就应该选择DECIMAL类型；如果需要存储日期和时间，就应该选择DATE、TIME或DATETIME类型；如果需要存储大段文本，就应该选择TEXT类型等等。

    ​		同时，在数据库表的设计中，还需要考虑字段的索引、约束以及关联关系等因素，以确保数据的完整性和查询性能。

  - 以下是一个简单的示例代码，展示了如何在Python中使用SQLite数据库并选择适当的数据类型：

    ```python
    import sqlite3
    
    # 连接到数据库
    conn = sqlite3.connect('example.db')
    cursor = conn.cursor()
    
    # 创建表格
    cursor.execute('''
        CREATE TABLE IF NOT EXISTS students (
            id INTEGER PRIMARY KEY,
            name TEXT,
            age INTEGER,
            gpa REAL
        )
    ''')
    
    # 插入数据
    data = [
        (1, 'Alice', 20, 3.8),
        (2, 'Bob', 22, 3.5),
        (3, 'Carol', 21, 3.9)
    ]
    cursor.executemany('INSERT INTO students VALUES (?, ?, ?, ?)', data)
    
    # 查询数据
    cursor.execute('SELECT * FROM students')
    result = cursor.fetchall()
    for row in result:
        print(row)
    
    # 关闭连接
    conn.commit()
    conn.close()
    ```

    ​        在这个示例中，我们使用了SQLite数据库，并创建了一个名为"students"的表格。表格中包含id、name、age和gpa四个字段，分别代表学生的唯一标识、姓名、年龄和平均绩点。不同数据类型用于存储不同类型的数据，比如INTEGER、TEXT和REAL分别用于存储整数、文本和浮点数。

    ​        代码演示了如何插入数据、查询数据以及关闭数据库连接。在实际应用中，你可以根据具体需求来选择数据库和相应的库，并根据业务逻辑选择适当的数据类型。

- 规范化和反规范化

  - ​        规范化（Normalization）和反规范化（Denormalization）是数据库设计中的两个关键概念，用于优化数据库结构和查询性能。

    ​        规范化是指将数据库设计拆分为多个表格，以减少数据冗余和保持数据一致性。它通过将数据分解为更小的、不重复的部分，使得数据在不同的表格中被存储，并使用外键来建立表格之间的关系。规范化通常遵循一系列范式规则，例如第一范式（1NF）、第二范式（2NF）、第三范式（3NF）等，以确保数据的结构合理和数据的更新、插入、删除操作不引起数据异常。

    ​        反规范化是一种优化技术，用于提高查询性能。它可以通过将分散的数据重新合并，减少表格之间的关联，以便在某些情况下加速数据检索。反规范化的操作包括将多个表格合并为一个、将冗余数据存储在多个表格中以减少关联等。然而，反规范化可能会导致数据冗余和一致性问题，因此需要在设计时权衡。

    ​         以下是一个简单的示例来说明规范化和反规范化的概念：

    ​         假设有一个数据库中存储了学生和课程的信息，我们可以规范化地设计为两个表格：一个是学生表格，包含学生的信息（学号、姓名、年龄等），另一个是课程表格，包含课程的信息（课程号、课程名等）。这样做可以避免数据冗余，提高数据一致性。

    ​        但是，如果我们需要频繁查询某个学生的所有课程，每次都需要进行关联查询，这可能会影响查询性能。在这种情况下，我们可以采取反规范化的策略，将学生的课程信息直接存储在学生表格中，以减少关联查询，从而提高查询性能。这样做虽然引入了数据冗余，但可以在特定场景下提升性能。

    ​        在实际应用中，规范化和反规范化需要根据具体需求和查询模式进行权衡，以保证数据库的结构和性能达到最佳状态。

  - 1

    - 首先，让我们创建两个表格：学生表格和课程表格。

      ```python
      import sqlite3
      
      # 创建连接和游标
      conn = sqlite3.connect('school.db')
      cursor = conn.cursor()
      
      # 创建学生表格
      cursor.execute('''CREATE TABLE students (
                          student_id INTEGER PRIMARY KEY,
                          name TEXT,
                          age INTEGER
                      )''')
      
      # 创建课程表格
      cursor.execute('''CREATE TABLE courses (
                          course_id INTEGER PRIMARY KEY,
                          course_name TEXT
                      )''')
      
      # 提交更改并关闭连接
      conn.commit()
      conn.close()
      ```

    - 规范化（Normalization）示例：
              假设我们想要添加学生和课程的信息。我们将采取规范化的方法，将学生和课程信息分别存储在两个表格中，通过外键关联起来。

      ```python
      # 插入学生信息
      conn = sqlite3.connect('school.db')
      cursor = conn.cursor()
      
      cursor.execute("INSERT INTO students (name, age) VALUES (?, ?)", ('Alice', 20))
      cursor.execute("INSERT INTO students (name, age) VALUES (?, ?)", ('Bob', 22))
      
      # 插入课程信息
      cursor.execute("INSERT INTO courses (course_name) VALUES (?)", ('Math',))
      cursor.execute("INSERT INTO courses (course_name) VALUES (?)", ('Science',))
      
      # 关联学生和课程信息
      cursor.execute("INSERT INTO student_courses (student_id, course_id) VALUES (?, ?)", (1, 1))  # Alice takes Math
      cursor.execute("INSERT INTO student_courses (student_id, course_id) VALUES (?, ?)", (2, 2))  # Bob takes Science
      
      conn.commit()
      conn.close()
      ```

    - 反规范化（Denormalization）示例：
              现在，假设我们需要频繁查询每个学生所选的课程。为了提高查询性能，我们可以采取反规范化的方法，将学生的课程信息直接存储在学生表格中。

      ```python
      # 更新学生表格，添加课程信息
      conn = sqlite3.connect('school.db')
      cursor = conn.cursor()
      
      cursor.execute("UPDATE students SET courses = 'Math' WHERE student_id = 1")
      cursor.execute("UPDATE students SET courses = 'Science' WHERE student_id = 2")
      
      conn.commit()
      conn.close()
      ```

      ​        请注意，这只是一个简化的示例，实际情况中需要根据数据量、查询需求等进行更详细的设计和考虑。在实际应用中，我们需要权衡规范化和反规范化的利弊，以满足数据的一致性和查询性能。

## 23.8 数据库包

​			下面是常用的数据库模块及其特点的表格总结：

| 模块名称    | 用途和特点                                       | 安装方式                  |
| ----------- | ------------------------------------------------ | ------------------------- |
| sqlite3     | 连接和操作SQLite数据库，轻量级                   | 自带于Python标准库        |
| pymysql     | 连接和操作MySQL数据库                            | `pip install pymysql`     |
| psycopg2    | 连接和操作PostgreSQL数据库                       | `pip install psycopg2`    |
| pyodbc      | 连接多种数据库，如Microsoft SQL Server、Oracle等 | `pip install pyodbc`      |
| SQLAlchemy  | 提供高级SQL工具包，支持多种数据库，支持ORM映射   | `pip install sqlalchemy`  |
| cx_Oracle   | 连接和操作Oracle数据库                           | `pip install cx_Oracle`   |
| mongoengine | 连接和操作MongoDB数据库                          | `pip install mongoengine` |
| redis-py    | 连接和操作Redis数据库                            | `pip install redis`       |

​		根据不同的项目需求和数据库类型，选择适合的数据库模块来满足你的开发需求。



# 二十四、 同步、异步和并发

## 24.1 概念

下面是同步、异步和并发的区别的表格形式：

| 特点     | 同步                                       | 异步                                         | 并发                                       |
| -------- | ------------------------------------------ | -------------------------------------------- | ------------------------------------------ |
| 执行方式 | 顺序执行，一个任务完成后才开始下一个任务   | 任务可以在不同的时间段内执行，不按顺序       | 多个任务在同一时间段内交替执行             |
| 阻塞     | 阻塞的，一个任务的执行会阻塞后续任务的开始 | 非阻塞的，一个任务的执行不会影响其他任务     | 可能是阻塞的也可能是非阻塞的               |
| 目的     | 确保数据正确性和顺序性                     | 提高系统响应性，充分利用资源                 | 提高系统性能和资源利用率，任务协同         |
| 数据关系 | 任务间可能共享数据，需要确保数据安全性     | 任务通常是独立的，可以共享数据，需注意安全性 | 任务可能共享数据，可能需要同步机制保证安全 |
| 应用场景 | 顺序执行、依赖前一任务结果的场景           | 高响应性的应用、资源充分利用的场景           | 并行计算、多任务处理、资源共享的场景       |

#### 24.1.1 同步的概念



- 同步（Synchronous）：

  ​		同步执行是指任务按照顺序一个接一个地执行，每个任务必须等待前一个任务完成后才能开始执行。在同步模式下，任务的执行顺序是可预测的，但如果某个任务需要等待，整个程序可能会因为等待而变得不响应。同步模式通常在程序的控制流中引入阻塞，即某个任务的执行会阻止其他任务的执行。

  


#### 24.1.2 异步的概念

- 异步（Asynchronous）：

​		异步执行是指任务可以相互独立地执行，不需要等待前一个任务完成。在异步模式下，任务可以在后台执行，而不会阻塞主程序的执行。异步编程常用于处理 I/O 密集型任务，如网络请求和文件读写操作，以提高程序的响应性。



`async def main():` 是一个异步函数的定义，它通常用作异步编程的入口点，负责协调和调度其他异步任务。在 Python 中，异步编程使用 `async` 和 `await` 关键字来定义和管理异步任务。

​		在异步编程中，`async def` 声明的函数被称为异步函数。

​		这些函数可以包含 `await` 关键字，用于等待其他异步任务完成。异步函数可以由事件循环调度并并行执行，从而提高程序的并发性和响应性。

​		以下是一个示例，展示了如何定义和调用一个异步函数 `main()`：

```python
import asyncio

async def say_hello():
    print("Hello")
    await asyncio.sleep(1)
    print("World")

async def main():
    await say_hello()
    print("Main function is done")

asyncio.run(main())
```

​		在这个示例中，`say_hello()` 是一个异步函数，它使用了 `await asyncio.sleep(1)` 来模拟异步等待。`main()` 异步函数调用了 `say_hello()` 函数，并在等待它完成后继续执行，最后输出 "Main function is done"。

需要注意以下几点：

- 异步函数需要使用 `async` 关键字进行声明。
- 异步函数内部可以使用 `await` 关键字来等待其他异步任务完成。
- 异步函数需要在支持异步编程的环境中运行，如在 Python 3.7+ 中使用 `asyncio.run()`。

`async def main():` 通常用于协调和调度多个异步任务，它是异步编程的入口函数，负责启动整个异步程序的执行。



#### 24.1.3 并发的概念



在 Python 中，并发是指多个任务（线程、进程或协程）在同一时间段内执行的能力。并发可以提高程序的性能和响应性，允许程序在执行多个任务时共享系统资源。

Python 提供了多种并发编程的方式，其中一些常见的方法包括：

1. **多线程（Multithreading）：** 多线程是在单个进程内创建多个线程来并发执行任务的方式。Python 中的 `threading` 模块可以用于创建和管理多线程。然而，由于 GIL（全局解释器锁）的存在，Python 的多线程并不适用于 CPU 密集型任务，但对于 I/O 密集型任务仍然很有用。

2. **多进程（Multiprocessing）：** 多进程是通过创建多个独立的进程来并发执行任务的方式。每个进程都有自己独立的 Python 解释器，因此可以避免 GIL 限制。Python 中的 `multiprocessing` 模块用于创建和管理多进程。

3. **协程（Coroutines）：** 协程是一种轻量级的并发方式，允许在单线程内通过协作式调度来实现任务切换。Python 的 `asyncio` 模块提供了协程支持，可以用于处理大量的 I/O 密集型任务。

4. **并发原语（Concurrency Primitives）：** Python 提供了一些用于处理并发的原语，如 `threading.Lock` 和 `threading.Semaphore`，用于控制多线程之间的访问共享资源的顺序。

5. **并发框架（Concurrency Frameworks）：** 除了上述原生的并发方式，还有一些第三方并发框架，如 `concurrent.futures`、`Celery` 等，用于简化并发任务的管理和调度。

在选择并发方式时，需要根据任务的特性和需求来做出决策。如果任务主要是 I/O 密集型，协程和多线程可能是合适的选择。如果任务是 CPU 密集型，多进程可能更合适。同时，需要注意并发编程可能引发的线程安全问题和资源竞争。



#### 24.1.4 阻塞和非阻塞

阻塞（Blocking）和非阻塞（Non-blocking）是与程序执行中的操作或任务相关的概念，涉及到等待外部资源或操作完成时的不同行为。

- 阻塞（Blocking）：

​	在阻塞操作中，当一个任务在等待某个操作完成时，它会暂停自己的执行，阻止整个程序的继续执行，直到操作完成为止。这意味着在阻塞操作期间，程序无法执行其他任务。

- 阻塞的特点：
  - 阻塞操作会导致程序停止，等待外部操作完成。
  - 一旦阻塞操作开始，程序会一直等待，直到操作完成。
  - 阻塞操作的执行时间不确定，可能会导致程序响应变慢。

- 非阻塞（Non-blocking）：

​		在非阻塞操作中，一个任务在等待某个操作完成时，不会暂停自己的执行，而是继续执行其他任务。即使一个操作没有完成，程序仍然可以继续执行其他任务。

- 非阻塞的特点：
  - 非阻塞操作允许程序同时执行多个任务，提高了并发性和响应性。
  - 即使某个操作尚未完成，程序也可以继续执行其他任务。
  - 非阻塞操作通常需要轮询或回调等机制来检查操作是否完成。

​		在异步编程中，使用非阻塞操作是实现高并发性和响应性的关键。通过非阻塞操作，程序可以同时处理多个任务，而不会因为等待某个任务完成而阻塞整个程序。这在处理网络请求、I/O 操作等场景中特别有用。

- 总结：

​		阻塞会导致程序停止等待，而非阻塞允许程序继续执行其他任务。异步编程通过非阻塞操作来提高程序的效率和并发性。

##### 24.1.4.1 阻塞





​		以下是一些 Python 中常见的阻塞应用场景的示例：

- **文件 I/O 阻塞：** 在同步文件读写操作中，当程序读取或写入文件时会阻塞，直到操作完成。

  ```python
  with open('myfile.txt', 'r') as f:
      content = f.read()  # 阻塞等待文件读取完成
      print(content)
  ```

- **网络请求阻塞：** 在同步网络请求中，当程序向服务器发起请求时，会等待服务器响应返回。

  ```python
  import requests
  
  response = requests.get('https://example.com')  # 阻塞等待服务器响应
  print(response.text)
  ```

- **等待用户输入：** 当使用 `input()` 函数等待用户输入时，程序会阻塞，直到用户输入内容。

  ```python
  user_input = input("Enter something: ")  # 阻塞等待用户输入
  print("You entered:", user_input)
  ```

- **数据库查询阻塞：** 在同步数据库查询中，当程序执行数据库查询操作时，会等待查询结果返回。

  ```python
  import sqlite3
  
  connection = sqlite3.connect('mydb.sqlite')
  cursor = connection.cursor()
  cursor.execute('SELECT * FROM mytable')  # 阻塞等待数据库查询结果
  rows = cursor.fetchall()
  connection.close()
  ```

- **等待锁：** 在多线程编程中，当多个线程试图获取同一个锁时，只有一个线程能够获取锁，其他线程会被阻塞。

  ```python
  import threading
  
  lock = threading.Lock()
  
  def worker():
      with lock:
          print("Thread is working...")
  
  thread1 = threading.Thread(target=worker)
  thread2 = threading.Thread(target=worker)
  
  thread1.start()  # 阻塞等待锁释放
  thread2.start()  # 阻塞等待锁释放
  ```

​		这些示例展示了在不同情况下 Python 程序可能会遇到阻塞，从而导致程序的响应性降低。为了解决这些问题，可以使用异步编程技术、多线程、多进程等方式来避免或减轻阻塞的影响。

##### 24.1.4.2 非阻塞



​		在 Python 中，实现非阻塞操作通常涉及使用异步编程技术，其中最常见的是使用 `asyncio` 库。以下是一些示例，展示了如何在不同情况下使用 `asyncio` 实现非阻塞操作：

- **异步网络请求：** 使用 `asyncio` 和 `aiohttp` 库来实现异步非阻塞的网络请求。

  ```python
  import asyncio
  import aiohttp
  
  async def fetch_website(url):
      async with aiohttp.ClientSession() as session:
          async with session.get(url) as response:
              return await response.text()
  
  async def main():
      url = 'https://www.example.com'
      website_content = await fetch_website(url)
      print("Website content:", website_content[:100])  # 打印部分网页内容
  
  asyncio.run(main())
  ```

- **异步文件读写：** 使用 `asyncio` 和异步文件操作来实现非阻塞的文件读写。

  ```python
  import asyncio
  
  async def read_file(filename):
      async with asyncio.to_thread(open, filename, 'r') as f:
          return await f.read()
  
  async def main():
      filename = 'myfile.txt'
      file_content = await read_file(filename)
      print("File content:", file_content)
  
  asyncio.run(main())
  ```

- **并行运行任务：** 使用 `asyncio.gather()` 函数来并行运行多个异步任务。

  ```python
  import asyncio
  
  async def task1():
      await asyncio.sleep(2)
      print("Task 1 completed")
  
  async def task2():
      await asyncio.sleep(1)
      print("Task 2 completed")
  
  async def main():
      await asyncio.gather(task1(), task2())
  
  asyncio.run(main())
  ```

- **定时操作：** 使用 `asyncio.sleep()` 函数实现非阻塞的定时操作。

  ```python
  import asyncio
  
  async def main():
      print("Start")
      await asyncio.sleep(2)  # 非阻塞等待2秒
      print("After 2 seconds")
  
  asyncio.run(main())
  ```

​		

- **实时更新数据：** 使用异步循环来实时更新数据，例如实时获取股票价格。

  ```python
  import asyncio
  
  async def update_stock_price(symbol):
      while True:
          price = await fetch_stock_price(symbol)
          print(f"{symbol} stock price: {price}")
          await asyncio.sleep(5)
  
  async def main():
      symbols = ['AAPL', 'GOOG', 'AMZN']
      tasks = [update_stock_price(symbol) for symbol in symbols]
      await asyncio.gather(*tasks)
  
  asyncio.run(main())
  ```

## 





## 24.2 机制

### 24.2.1 同步机制

#### 24.2.1.1 线程同步

​		线程同步机制是用于确保多个线程在并发执行时数据的正确性和一致性的一组技术和工具。在多线程环境中，由于线程共享进程的内存空间，可能会导致多个线程同时访问和修改共享数据，从而引发数据竞争和不一致性的问题。线程同步机制的目标是协调线程之间的执行，防止并发访问造成的问题。

​		以下是常见的线程同步机制：

1. **锁（Lock）：** 锁是最常见的线程同步机制之一，它允许一个线程独占某个资源，其他线程必须等待锁的释放才能访问该资源。Python 中的 `threading.Lock` 就是一个常见的锁实现。

2. **信号量（Semaphore）：** 信号量是一个计数器，限制同时访问某个资源的线程数量。它可以用于控制允许的最大并发数。Python 中的 `threading.Semaphore` 可以实现信号量机制。

3. **条件变量（Condition）：** 条件变量用于在某个条件满足时唤醒等待的线程。它通常与锁结合使用，用于线程之间的通信和协调。Python 中的 `threading.Condition` 实现了条件变量。

4. **事件（Event）：** 事件是一种线程同步机制，允许线程等待其他线程的信号，以实现线程之间的协作和通信。Python 中的 `threading.Event` 实现了事件机制。

5. **互斥体（Mutex）：** 互斥体是一种用于线程同步的机制，类似于锁，但它可以被同一个线程多次获得，用于解决嵌套锁问题。

6. **条件锁（ConditionLock）：** 一种综合了锁和条件变量的同步机制，可以在特定条件下等待和唤醒线程。

​		这些线程同步机制可以根据不同的情景来选择使用，以确保多线程环境下数据的安全访问和协调执行。

下面是使用Python的`threading`模块来分别演示锁、信号量、条件变量、事件、互斥体和条件锁的示例代码：

1. **锁（Lock）：**
```python
import threading

counter = 0
counter_lock = threading.Lock()

def increment_counter():
    global counter
    with counter_lock:
        counter += 1

threads = []
for _ in range(10):
    thread = threading.Thread(target=increment_counter)
    threads.append(thread)
    thread.start()

for thread in threads:
    thread.join()

print("Counter:", counter)
```

2. **信号量（Semaphore）：**
```python
import threading

semaphore = threading.Semaphore(3)  # 允许3个线程同时执行

def worker():
    with semaphore:
        print(threading.current_thread().name, "is working")

threads = []
for i in range(5):
    thread = threading.Thread(target=worker, name=f"Thread-{i}")
    threads.append(thread)
    thread.start()

for thread in threads:
    thread.join()
```

3. **条件变量（Condition）：**
```python
import threading
import time

cond = threading.Condition()

def producer():
    with cond:
        print("Producing...")
        time.sleep(2)  # 模拟生产耗时
        cond.notify()

def consumer():
    with cond:
        cond.wait()
        print("Consuming...")

producer_thread = threading.Thread(target=producer)
consumer_thread = threading.Thread(target=consumer)

producer_thread.start()
consumer_thread.start()

producer_thread.join()
consumer_thread.join()
```

4. **事件（Event）：**
```python
import threading

event = threading.Event()

def worker():
    print("Waiting for event to be set")
    event.wait()
    print("Event is set!")

threads = []
for _ in range(3):
    thread = threading.Thread(target=worker)
    threads.append(thread)
    thread.start()

event.set()  # 设置事件，唤醒等待的线程

for thread in threads:
    thread.join()
```

5. **互斥体（Mutex）：**
互斥体与锁的使用方式相同，但不同之处在于它可以被同一个线程多次获得。

```python
import threading

counter = 0
mutex = threading.Lock()

def increment_counter():
    global counter
    with mutex:
        counter += 1

threads = []
for _ in range(10):
    thread = threading.Thread(target=increment_counter)
    threads.append(thread)
    thread.start()

for thread in threads:
    thread.join()

print("Counter:", counter)
```

6. **条件锁（ConditionLock）：**
条件锁结合了锁和条件变量，用于在满足特定条件时等待和唤醒线程。

```python
import threading

class ConditionLockExample:
    def __init__(self):
        self.condition = threading.Condition()
        self.value = 0

    def producer(self):
        with self.condition:
            self.value = 42
            self.condition.notify()

    def consumer(self):
        with self.condition:
            self.condition.wait()
            print("Consumer got value:", self.value)

example = ConditionLockExample()

producer_thread = threading.Thread(target=example.producer)
consumer_thread = threading.Thread(target=example.consumer)

producer_thread.start()
consumer_thread.start()

producer_thread.join()
consumer_thread.join()
```

这些示例演示了各种线程同步机制的用法，帮助你理解如何在多线程环境中实现数据的安全访问和协调执行。





#### 24.2.1.2 进程同步



当涉及多进程编程时，有多种不同的进程同步机制可用于协调和同步进程的执行。以下是这些机制的分别说明：

1. **锁（Lock）：**
   - 锁是最基本的进程同步机制，用于在多个进程之间提供互斥访问共享资源的能力。一个进程可以获取锁，以确保其他进程不能同时访问被锁定的资源。
   - 使用`multiprocessing.Lock`来创建锁对象，然后使用`with`语句在代码块中获取和释放锁，从而实现对共享资源的同步访问。

2. **信号量（Semaphore）：**
   - 信号量是一种更通用的同步机制，用于控制多个进程对资源的访问。信号量维护一个计数器，限制可以同时访问共享资源的进程数量。
   - 使用`multiprocessing.Semaphore`来创建信号量对象，然后使用`with`语句获取信号量，确保在信号量允许的情况下进程可以访问共享资源。

3. **条件变量（Condition）：**
   - 条件变量用于在多进程之间传递信息并实现进程的等待和唤醒。它允许一个进程等待某个条件满足，然后在另一个进程满足条件时唤醒等待的进程。
   - 使用`multiprocessing.Condition`来创建条件变量对象，然后使用`with`语句进行等待和通知操作，从而实现进程之间的通信和同步。

4. **事件（Event）：**
   - 事件是一种允许一个进程等待另一个进程发出信号的同步机制。一个进程可以等待事件的触发，而另一个进程可以设置事件来触发等待的进程。
   - 使用`multiprocessing.Event`来创建事件对象，然后使用`wait()`方法等待事件触发，使用`set()`方法设置事件，实现进程之间的通信和同步。

5. **队列（Queue）：**
   - 队列是一种实现进程间数据传递和同步的方式，用于在多个进程之间传递数据。进程可以将数据放入队列，然后其他进程可以从队列中获取数据。
   - 使用`multiprocessing.Queue`来创建队列对象，进程可以使用`put()`方法放入数据，使用`get()`方法获取数据，实现进程之间的数据传递和同步。

​		以上这些进程同步机制各自适用于不同的场景，可以根据需求选择适合的机制来确保多个进程之间的协调和有序执行。



- lock lock.acquire() lock.realse()

```python
import multiprocessing
import time
 
 
def task1(lock):
    with lock:  # with上下文语句使用锁，会自动释放锁
        n = 5
        while n > 1:
            print(f"{time.strftime('%H:%M:%S')} task1 输出信息")
            time.sleep(1)
            n -= 1
 
 
def task2(lock):
    lock.acquire() 
    n = 5
    while n > 1:
        print(f"{time.strftime('%H:%M:%S')} task2 输出信息")
        time.sleep(1)
        n -= 1
    lock.release()
 
 
def task3(lock):
    lock.acquire()
    n = 5
    while n > 1:
        print(f"{time.strftime('%H:%M:%S')} task3 输出信息")
        time.sleep(1)
        n -= 1
    lock.release()
 
 
if __name__ == "__main__":
    lock = multiprocessing.Lock()
    p1 = multiprocessing.Process(target=task1, args=(lock,))
    p2 = multiprocessing.Process(target=task2, args=(lock,))
    p3 = multiprocessing.Process(target=task3, args=(lock,))
    p1.start()
    p2.start()
    p3.start()
    
    
    
20:13:22 task1 输出信息
20:13:23 task1 输出信息
20:13:24 task1 输出信息
20:13:25 task1 输出信息
20:13:26 task2 输出信息
20:13:27 task2 输出信息
20:13:28 task2 输出信息
20:13:29 task2 输出信息
20:13:30 task3 输出信息
20:13:31 task3 输出信息
20:13:32 task3 输出信息
20:13:33 task3 输出信息


#lock.acquire(): 这个方法用于获取锁，即锁住共享资源，使得只有一个进程可以进入临界区（访问共享资源）。如果锁已经被其他进程占用，那么调用acquire()方法的进程会被阻塞，直到锁被释放为止。

#lock.release(): 这个方法用于释放锁，即解锁共享资源，允许其他进程进入临界区。在完成对共享资源的访问后，进程应该调用release()方法来释放锁，以便其他进程可以继续访问。
```

- 信号量

​		信号量（`Semaphore`）是一种进程同步机制，用于控制多个进程对共享资源的访问。与锁不同，信号量可以控制允许访问资源的进程数量，而不仅仅是一个进程。

​		以下是一个使用信号量进行进程同步的简单示例：

```python
import multiprocessing

def access_resource(semaphore, resource):
    semaphore.acquire()  # 获取信号量
    try:
        print(f"Process {multiprocessing.current_process().name} is accessing the resource.")
        resource.value += 1
    finally:
        semaphore.release()  # 释放信号量

if __name__ == "__main__":
    resource = multiprocessing.Value("i", 0)
    semaphore = multiprocessing.Semaphore(2)  # 允许两个进程同时访问
    
    processes = []
    
    for i in range(5):
        process = multiprocessing.Process(target=access_resource, args=(semaphore, resource))
        processes.append(process)
        process.start()
    
    for process in processes:
        process.join()
    
    print("Resource value:", resource.value)
```

​		在这个示例中，创建了一个信号量对象`semaphore`，它允许最多两个进程同时访问共享资源。通过在进程中调用`semaphore.acquire()`和`semaphore.release()`来获取和释放信号量，我们确保只有最多两个进程可以同时访问共享资源。其他进程必须等待信号量释放后才能访问。

​		使用信号量可以实现更细粒度的进程同步，允许一定数量的进程同时执行特定任务，从而在资源竞争的情况下保持控制和顺序。

- 条件变量

​		条件变量（`Condition`）是一种用于进程同步的高级机制，它允许一个或多个进程等待特定条件的发生，然后在条件满足时被唤醒。条件变量通常与锁（`Lock`）一起使用，以确保在多个进程之间协调共享资源的访问。

​		以下是一个使用条件变量进行进程同步的简单示例：

```python
import multiprocessing

def producer(condition, items):
    with condition:
        for item in items:
            print(f"Producing item: {item}")
            condition.notify()  # 通知等待的消费者
            condition.wait()    # 等待消费者的通知

def consumer(condition, items):
    with condition:
        for item in items:
            condition.wait()    # 等待生产者通知
            print(f"Consuming item: {item}")
            condition.notify()  # 通知生产者

if __name__ == "__main__":
    condition = multiprocessing.Condition()
    items = ["item1", "item2", "item3", "item4"]
    
    producer_process = multiprocessing.Process(target=producer, args=(condition, items))
    consumer_process = multiprocessing.Process(target=consumer, args=(condition, items))
    
    producer_process.start()
    consumer_process.start()
    
    producer_process.join()
    consumer_process.join()
```

​		在这个示例中，生产者进程通过循环逐个生成项目并使用`condition.notify()`通知等待的消费者。消费者进程等待生产者的通知，然后消费项目并使用`condition.notify()`通知生产者。通过交替的等待和通知，生产者和消费者之间实现了同步。

​		条件变量提供了更高级的同步机制，使得进程可以等待特定的条件满足后再进行操作，避免了不必要的轮询和资源浪费。





-  事件

  ​		事件（`Event`）是一种用于进程同步的机制，它允许一个进程等待另一个进程发出信号后才继续执行。事件通常用于在多个进程之间触发某些操作的同步。

  ​		以下是一个使用事件进行进程同步的示例：

  ```python
  import multiprocessing
  import time
  
  def worker(event):
      print("Worker is waiting for the event.")
      event.wait()  # 等待事件触发
      print("Worker has received the event and continues.")
  
  if __name__ == "__main__":
      event = multiprocessing.Event()
      
      worker_process = multiprocessing.Process(target=worker, args=(event,))
      worker_process.start()
      
      time.sleep(2)  # 模拟一些操作
      print("Main process is setting the event.")
      event.set()    # 设置事件，唤醒等待的工作进程
      
      worker_process.join()
  ```

  ​		在这个示例中，工作进程通过`event.wait()`等待事件的触发。主进程等待一段时间后，通过`event.set()`设置事件，这将唤醒等待的工作进程继续执行。

  ​		事件的主要用途是在不同的进程之间发出信号，使得一个或多个等待的进程可以继续执行。这种机制在需要根据外部条件来协调进程执行的情况下非常有用。

- 队列

  ​		队列（`Queue`）是一种进程同步的机制，用于在多个进程之间传递数据，并确保数据传递的安全性和顺序性。队列提供了一种有序的方式来进行进程间通信，避免了数据竞争和并发访问的问题。

  ​		以下是一个使用队列进行进程同步的示例：

  ```python
  import multiprocessing
  
  def producer(queue):
      for item in range(5):
          print(f"Producing item: {item}")
          queue.put(item)
  
  def consumer(queue):
      while True:
          item = queue.get()
          if item is None:
              break
          print(f"Consuming item: {item}")
  
  if __name__ == "__main__":
      queue = multiprocessing.Queue()
      
      producer_process = multiprocessing.Process(target=producer, args=(queue,))
      consumer_process = multiprocessing.Process(target=consumer, args=(queue,))
      
      producer_process.start()
      consumer_process.start()
      
      producer_process.join()
      queue.put(None)  # 发送终止信号给消费者
      consumer_process.join()
  ```

  ​		在这个示例中，生产者进程将一些项目放入队列中，而消费者进程从队列中获取这些项目并进行消费。通过队列的特性，我们可以确保数据传递的顺序性和安全性，避免了多个进程之间的竞争。

  ​		队列在多进程环境中广泛使用，用于进行数据传递、任务分发等，有效地解决了进程间通信和同步的问题。



### 24.2.2 异步机制

	Python 的异步机制主要是通过 `asyncio` 模块实现的，它提供了协程（coroutine）和事件循环（event loop）等机制，用于实现非阻塞的并发执行。以下是异步编程的基本概念和示例代码：

- **协程（Coroutine）：**
  - 协程是一种特殊的函数，可以在运行过程中被暂停并恢复。使用 `async def` 声明协程，内部使用 `await` 关键字来等待异步操作的完成。协程能够在等待 I/O 操作的同时执行其他任务，提高程序的并发性和响应性。

- **事件循环（Event Loop）：**
  - 事件循环是异步编程的核心，负责调度和管理协程的执行。事件循环会在协程遇到 `await` 时暂停该协程，然后切换到其他协程执行，直到异步操作完成后再恢复协程的执行。

- **异步操作（Async Operation）：**
  - 异步操作是指可能会阻塞程序执行的操作，如网络请求、文件读写等。通过使用协程和事件循环，可以将这些操作变为非阻塞的，从而避免了线程切换的开销。

以下是使用 `asyncio` 实现的异步机制示例代码：

```python
import asyncio

async def worker(name):
    print(f"Coroutine {name} is starting")
    await asyncio.sleep(2)
    print(f"Coroutine {name} is done")

async def main():
    tasks = [worker(i) for i in range(3)]
    await asyncio.gather(*tasks)

if __name__ == "__main__":
    asyncio.run(main())

print("All coroutines are done")
```

​		在上述代码中，我们定义了一个 `worker` 协程，模拟异步操作（等待2秒）。然后在 `main` 协程中使用 `asyncio.gather()` 来同时运行多个协程。最后，通过 `asyncio.run()` 来运行主协程，实现异步执行。

### 24.2.3 并发机制

​	在 Python 中，有几种常见的并发机制可以用于实现并发执行和提高程序的响应性。以下是一些常见的 Python 并发机制：

- **多线程（Multithreading）：** 使用 `threading` 模块可以创建多个线程，每个线程可以执行不同的任务。多线程适用于 I/O 密集型任务，但需要注意线程安全问题，如共享数据的同步和互斥。例如：

   ```python
   import threading
   
   def worker(name):
       print(f"Thread {name} is starting")
       # ... 执行任务 ...
       print(f"Thread {name} is done")
   
   threads = []
   for i in range(3):
       thread = threading.Thread(target=worker, args=(i,))
       threads.append(thread)
       thread.start()
   
   for thread in threads:
       thread.join()
   
   print("All threads are done")
   ```

- **多进程（Multiprocessing）：** 使用 `multiprocessing` 模块可以创建多个进程，每个进程有独立的内存空间。多进程适用于 CPU 密集型任务，可以充分利用多核处理器。进程之间可以通过进程间通信（IPC）来传递数据。例如：

   ```python
   import multiprocessing
   
   def worker(name):
       print(f"Process {name} is starting")
       # ... 执行任务 ...
       print(f"Process {name} is done")
   
   processes = []
   for i in range(3):
       process = multiprocessing.Process(target=worker, args=(i,))
       processes.append(process)
       process.start()
   
   for process in processes:
       process.join()
   
   print("All processes are done")
   ```

- **异步编程（Asynchronous Programming）：** 使用 `asyncio` 模块可以实现非阻塞的并发执行。通过协程和事件循环，可以在等待 I/O 操作的同时执行其他任务，提高程序的并发性和响应性。适用于 I/O 密集型任务。例如：

   ```python
   import asyncio
   
   async def worker(name):
       print(f"Coroutine {name} is starting")
       await asyncio.sleep(2)  # 模拟异步操作
       print(f"Coroutine {name} is done")
   
   async def main():
       tasks = [worker(i) for i in range(3)]
       await asyncio.gather(*tasks)
   
   asyncio.run(main())
   
   print("All coroutines are done")
   ```

- **线程池和进程池：** 使用 `concurrent.futures` 模块中的 `ThreadPoolExecutor` 和 `ProcessPoolExecutor` 可以管理线程池和进程池，以提高任务执行的效率。例如：

   ```python
   import concurrent.futures
   
   def worker(name):
       print(f"Thread {name} is starting")
       # ... 执行任务 ...
       print(f"Thread {name} is done")
   
   with concurrent.futures.ThreadPoolExecutor() as executor:
       for i in range(3):
           executor.submit(worker, i)
   
   print("All threads are done")
   ```

以上是 Python 中常用的并发机制，根据任务的性质和需求选择合适的并发模型，可以提高程序的并发性和响应性。





# 24.3 函数

## 24.3.1 同步函数

​		在 Python 中，函数默认是同步执行的，也就是说函数的调用会阻塞当前线程的执行，直到函数返回为止。以下是一个简单的同步函数示例：

```python
import time

def sync_function(name):
    print(f"Sync function {name} is starting")
    time.sleep(2)  # 模拟耗时操作
    print(f"Sync function {name} is done")

if __name__ == "__main__":
    print("Main thread is starting")
    
    sync_function("A")
    sync_function("B")
    
    print("Main thread is done")
```

​		在上述代码中，`sync_function` 是一个同步函数，它使用 `time.sleep()` 来模拟一个耗时操作。在主线程中，依次调用了两次 `sync_function`，每次调用都会阻塞主线程的执行，直到函数执行完成。

​		虽然同步函数是一种简单的编程模型，但在处理多个任务时可能会导致程序的响应性降低，因为每次函数调用都会阻塞当前线程的执行。为了提高程序的并发性和响应性，可以考虑使用异步编程或多线程/多进程等方式来处理任务。

## 24.3.2 异步函数

#### 24.3.2.1 函数定义

```python
>>> import asyncio
>>> dir(asyncio)
['ALL_COMPLETED', 'AbstractChildWatcher', 'AbstractEventLoop', 'AbstractEventLoopPolicy', 'AbstractServer', 'Barrier', 'BaseEventLoop', 'BaseProtocol', 'BaseTransport', 'BoundedSemaphore', 'BrokenBarrierError', 'BufferedProtocol', 'CancelledError', 'Condition', 'DatagramProtocol', 'DatagramTransport', 'DefaultEventLoopPolicy', 'Event', 'FIRST_COMPLETED', 'FIRST_EXCEPTION', 'FastChildWatcher', 'Future', 'Handle', 'IncompleteReadError', 'InvalidStateError', 'LifoQueue', 'LimitOverrunError', 'Lock', 'MultiLoopChildWatcher', 'PidfdChildWatcher', 'PriorityQueue', 'Protocol', 'Queue', 'QueueEmpty', 'QueueFull', 'ReadTransport', 'Runner', 'SafeChildWatcher', 'SelectorEventLoop', 'Semaphore', 'SendfileNotAvailableError', 'Server', 'StreamReader', 'StreamReaderProtocol', 'StreamWriter', 'SubprocessProtocol', 'SubprocessTransport', 'Task', 'TaskGroup', 'ThreadedChildWatcher', 'Timeout', 'TimeoutError', 'TimerHandle', 'Transport', 'WriteTransport', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__', '_enter_task', '_get_running_loop', '_leave_task', '_register_task', '_set_running_loop', '_unregister_task', 'all_tasks', 'as_completed', 'base_events', 'base_futures', 'base_subprocess', 'base_tasks', 'constants', 'coroutines', 'create_subprocess_exec', 'create_subprocess_shell', 'create_task', 'current_task', 'ensure_future', 'events', 'exceptions', 'format_helpers', 'futures', 'gather', 'get_child_watcher', 'get_event_loop', 'get_event_loop_policy', 'get_running_loop', 'iscoroutine', 'iscoroutinefunction', 'isfuture', 'locks', 'log', 'mixins', 'new_event_loop', 'open_connection', 'open_unix_connection', 'protocols', 'queues', 'run', 'run_coroutine_threadsafe', 'runners', 'selector_events', 'set_child_watcher', 'set_event_loop', 'set_event_loop_policy', 'shield', 'sleep', 'sslproto', 'staggered', 'start_server', 'start_unix_server', 'streams', 'subprocess', 'sys', 'taskgroups', 'tasks', 'threads', 'timeout', 'timeout_at', 'timeouts', 'to_thread', 'transports', 'trsock', 'unix_events', 'wait', 'wait_for', 'wrap_future']
```

	下面是你列出的 `asyncio` 模块中的一些属性和类的简要解释：

- `ALL_COMPLETED`：在 `asyncio.wait()` 中表示等待所有任务完成。
- `AbstractChildWatcher`：抽象基类，定义了异步子进程监视器的接口。
- `AbstractEventLoop`：抽象基类，定义了事件循环的接口。
- `AbstractEventLoopPolicy`：抽象基类，定义了事件循环策略的接口。
- `AbstractServer`：抽象基类，定义了异步服务器的接口。
- `Barrier`：用于多个任务之间的同步，类似于线程中的 `threading.Barrier`。
- `BaseEventLoop`：事件循环的基类。
- `BaseProtocol`：协议的基类。
- `BaseTransport`：传输的基类。
- `BoundedSemaphore`：有界信号量，类似于线程中的 `threading.BoundedSemaphore`。
- `BrokenBarrierError`：当 `Barrier` 中的等待被取消时引发的异常。
- `BufferedProtocol`：缓冲协议的基类。
- `CancelledError`：异步操作被取消时引发的异常。
- `Condition`：异步条件变量，类似于线程中的 `threading.Condition`。
- `DatagramProtocol` 和 `DatagramTransport`：用于处理 UDP 数据报的协议和传输。
- `DefaultEventLoopPolicy`：默认事件循环策略。
- `Event`：异步事件对象，类似于线程中的 `threading.Event`。
- `FIRST_COMPLETED` 和 `FIRST_EXCEPTION`：在 `asyncio.wait()` 中表示等待第一个任务完成或引发异常。
- `FastChildWatcher` 和 `MultiLoopChildWatcher`：用于监视子进程的不同实现。
- `Future`：表示异步操作的结果，可以被等待、取消或添加回调。
- `Handle` 和 `TimerHandle`：异步任务的句柄。
- `IncompleteReadError`：在读取不完整数据时引发的异常。
- `InvalidStateError`：操作在无效状态下引发的异常。
- `LifoQueue`：后进先出的异步队列，类似于线程中的 `queue.LifoQueue`。
- `LimitOverrunError`：超过限制时引发的异常。
- `Lock` 和 `Semaphore`：异步锁和信号量，用于控制异步任务的并发访问。
- `PidfdChildWatcher`：用于监视子进程的实现。
- `PriorityQueue`：带优先级的异步队列。
- `Protocol`：协议的基类。
- `Queue`、`QueueEmpty` 和 `QueueFull`：异步队列及其相关异常。
- `ReadTransport` 和 `WriteTransport`：用于读取和写入数据的传输。
- `SafeChildWatcher`：用于监视子进程的实现。
- `SelectorEventLoop`：基于选择器的事件循环。
- `Semaphore`：异步信号量，用于控制异步任务的并发访问。
- `SendfileNotAvailableError`：在 sendfile 不可用时引发的异常。
- `Server`：异步服务器对象。
- `StreamReader`、`StreamReaderProtocol` 和 `StreamWriter`：用于处理流的协议和传输。
- `SubprocessProtocol` 和 `SubprocessTransport`：用于处理子进程的协议和传输。
- `Task` 和 `TaskGroup`：表示异步任务的对象。
- `ThreadedChildWatcher`：用于监视子进程的实现。
- `Timeout` 和 `TimeoutError`：用于设置异步操作的超时。
- `Transport`：传输的基类。

- `WriteTransport`：用于写入数据的传输。

- `__all__`：包含模块中所有可导入的名称的列表。

- `__builtins__`：内置名称空间的引用，包括所有内置函数和异常。

- `__cached__`：模块被缓存的路径。

- `__doc__`：模块的文档字符串。

- `__file__`：模块文件的路径。

- `__loader__`：加载模块的加载器对象。

- `__name__`：模块的名称。

- `__package__`：模块所在的包的名称。

- `__path__`：包的子模块搜索路径。

- `__spec__`：模块的规范。

- `_enter_task`、`_leave_task`、`_register_task`、`_set_running_loop`、`_unregister_task`：用于内部管理异步任务的函数。

- `all_tasks`：返回事件循环中所有任务的集合。

- `as_completed`：在异步任务完成时产生结果。

- `base_events`、`base_futures`、`base_subprocess`、`base_tasks`：基础事件、未来、子进程和任务的模块。

- `constants`：异步编程中使用的常量。

- `coroutines`：用于管理协程的模块。

- `create_subprocess_exec`、`create_subprocess_shell`：创建子进程的函数。

- `current_task`：返回当前正在运行的任务。

- `ensure_future`：将对象转换为 `Future` 或协程。

- `events`：异步事件相关的模块。

- `exceptions`：定义了异步编程中的异常。

- `futures`：用于管理异步操作的未来对象。

- `gather`：在并行运行多个协程时收集结果。

- `get_child_watcher`、`set_child_watcher`：获取和设置子进程监视器。

- `get_event_loop`、`set_event_loop`：获取和设置事件循环。

- `get_event_loop_policy`、`set_event_loop_policy`：获取和设置事件循环策略。

- `get_running_loop`：返回正在运行的事件循环。

- `iscoroutine`、`iscoroutinefunction`、`isfuture`：用于检查对象是否为协程、协程函数或未来。

- `locks`：异步锁和信号量相关的模块。

- `log`：异步编程的日志模块。

- `mixins`：用于实现异步协议的混合类。

- `new_event_loop`：创建新的事件循环。

- `open_connection`、`open_unix_connection`：创建异步网络连接。

- `protocols`：用于管理协议的模块。

- `queues`：异步队列相关的模块。

- `run`：运行异步函数作为主程序入口。

- `run_coroutine_threadsafe`：在不同线程中运行协程。

- `runners`：用于运行异步函数的运行器。

- `selector_events`：基于选择器的事件循环。

- `shield`：在捕获异常时保护协程的函数。

- `sslproto`：SSL 协议支持。

- `start_server`、`start_unix_server`：开始监听连接的服务器。

- `streams`：用于处理流的模块。

- `subprocess`：用于处理子进程的模块。

- `taskgroups`、`tasks`、`threads`：任务和线程相关的模块。

- `timeout`、`timeout_at`、`timeouts`：设置异步操作的超时。

- `to_thread`：将同步函数放入不同的线程中运行。

- `transports`：传输相关的模块。

- `trsock`：套接字传输支持。

- `unix_events`：Unix 套接字和子进程事件支持。

- `wait`、`wait_for`：等待多个异步任务的完成。

- `wrap_future`：将 `Future` 对象包装成协程。

#### 24.3.2.2 异步总结



当涉及到 `asyncio` 模块的不同功能时，以下是一些主要的函数总结：

- **事件循环和任务调度**：

| 功能                   | 函数                         |
| ---------------------- | ---------------------------- |
| 启动事件循环           | `asyncio.run()`              |
| 获取当前事件循环       | `asyncio.get_event_loop()`   |
| 设置当前事件循环       | `asyncio.set_event_loop()`   |
| 创建新事件循环         | `asyncio.new_event_loop()`   |
| 获取正在运行的事件循环 | `asyncio.get_running_loop()` |

- **异步任务创建和管理**：

| 功能                             | 函数                      |
| -------------------------------- | ------------------------- |
| 创建异步任务                     | `asyncio.create_task()`   |
| 将对象转换为 `Future` 或协程     | `asyncio.ensure_future()` |
| 并行运行和等待多个任务           | `asyncio.gather()`        |
| 等待一组任务的任何一个或全部完成 | `asyncio.wait()`          |
| 在任务完成时产生结果             | `asyncio.as_completed()`  |
| 获取事件循环中所有任务的集合     | `asyncio.all_tasks()`     |

- **异步操作控制**：

| 功能                             | 函数                   |
| -------------------------------- | ---------------------- |
| 在异步函数中进行休眠             | `asyncio.sleep()`      |
| 保护协程在捕获异常时不被取消     | `asyncio.shield()`     |
| 异步操作超时时引发的异常         | `asyncio.TimeoutError` |
| 等待异步操作的完成，支持设置超时 | `asyncio.wait_for()`   |

- **异步队列和数据传递**：

| 功能               | 函数                |
| ------------------ | ------------------- |
| 异步队列           | `asyncio.Queue`     |
| 后进先出的异步队列 | `asyncio.LifoQueue` |

- **异步协议和传输**：

| 功能                     | 函数                             |
| ------------------------ | -------------------------------- |
| 创建异步网络连接         | `asyncio.open_connection()`      |
| 创建异步 Unix 套接字连接 | `asyncio.open_unix_connection()` |

- **异步网络编程**：

| 功能                             | 函数                          |
| -------------------------------- | ----------------------------- |
| 开始监听连接的服务器             | `asyncio.start_server()`      |
| 开始监听 Unix 套接字连接的服务器 | `asyncio.start_unix_server()` |

- **其他功能**：

| 功能                           | 函数                  |
| ------------------------------ | --------------------- |
| 将同步函数放入不同的线程中运行 | `asyncio.to_thread()` |



## 24.3.3 并发函数



- 线程

- 进程

  

## 24.5 多线程

### 24.5.1 线程创建、并发、同步



​		在 Python 中，多线程是一种并发编程技术，允许程序在同一进程中创建多个线程来执行任务，从而实现并发执行。Python 的多线程通过标准库中的 `threading` 模块来实现。每个线程是一个独立的执行流，它们共享同一个进程的资源，包括内存空间和文件描述符等。

​		以下是一些关于多线程的基本概念和示例：

- **创建线程：** 使用 `threading.Thread()` 类来创建线程，传入一个函数作为线程的执行内容。

   ```python
   import threading
   
   def print_numbers():
       for i in range(5):
           print(i)
   
   thread = threading.Thread(target=print_numbers)
   thread.start()  # 启动线程
   ```

- **并发执行：** 多个线程可以并发地执行，实现多任务处理。

   ```python
   import threading
   
   def print_numbers():
       for i in range(5):
           print(i)
   
   def print_letters():
       for letter in 'abcde':
           print(letter)
   
   thread1 = threading.Thread(target=print_numbers)
   thread2 = threading.Thread(target=print_letters)
   
   thread1.start()
   thread2.start()
   
   thread1.join()
   thread2.join()
   
   print("Both threads have finished")
   ```

- **线程同步：** 由于多个线程共享资源，可能会引发线程安全问题。可以使用锁（`threading.Lock`）来保护共享资源的访问，实现线程同步。

   ```python
   import threading
   
   counter = 0
   counter_lock = threading.Lock()
   
   def increment_counter():
       global counter
       with counter_lock:
           for _ in range(1000000):
               counter += 1
   
   thread1 = threading.Thread(target=increment_counter)
   thread2 = threading.Thread(target=increment_counter)
   
   thread1.start()
   thread2.start()
   
   thread1.join()
   thread2.join()
   
   print("Counter value:", counter)
   ```

​		需要注意的是，Python 的多线程因为 Global Interpreter Lock (GIL) 的存在，多个线程不能在同一时刻并行执行 CPU 密集型任务。多线程主要适用于 I/O 密集型任务，如网络请求、文件读写等，因为在 I/O 操作时线程会释放 GIL，允许其他线程执行。

​		如果需要利用多核 CPU 并行执行 CPU 密集型任务，可以考虑使用多进程编程，其中每个进程都有自己独立的 Python 解释器和资源。

### 24.5.2  GIL

			Global Interpreter Lock（GIL）是Python解释器中的一个重要概念。它是一个互斥锁，用于保护Python解释器中的内部数据结构，防止多个线程同时执行Python字节码。GIL的存在影响了Python多线程的并行性能。

以下是关于GIL的主要内容：

- **GIL的作用：** GIL是一个互斥锁，确保在CPython解释器中一次只有一个线程执行Python字节码。这是为了避免在多线程环境下产生竞态条件和数据不一致等问题。

- **影响多线程并行性：** 由于GIL的存在，Python多线程在执行CPU密集型任务时无法充分利用多核CPU，并不能实现真正的并行执行。但是对于I/O密集型任务，线程会在等待I/O操作时释放GIL，从而允许其他线程执行。

- **多线程适用场景：** Python多线程主要适用于处理I/O密集型任务，如网络请求、文件读写、数据库访问等，因为在等待I/O时，线程可以释放GIL，允许其他线程执行，从而提高并发性。

- **多进程替代：** 如果需要利用多核CPU进行并行计算，可以考虑使用多进程编程，每个进程都有独立的Python解释器和资源，不存在GIL的限制。

​		尽管GIL存在一些限制，但在实际应用中，Python仍然可以通过多线程在I/O密集型任务中提供高并发性和响应性。对于CPU密集型任务，可以使用多进程来实现真正的并行计算。其他的Python解释器（如Jython、IronPython等）不一定存在GIL，但CPython（官方的Python解释器）中存在GIL。

### 24.5.3 函数



```python
>>> import threading
>>> dir(threading)
['Barrier', 'BoundedSemaphore', 'BrokenBarrierError', 'Condition', 'Event', 'ExceptHookArgs', 'Lock', 'RLock', 'Semaphore', 'TIMEOUT_MAX', 'Thread', 'ThreadError', 'Timer', 'WeakSet', '_CRLock', '_DummyThread', '_HAVE_THREAD_NATIVE_ID', '_MainThread', '_PyRLock', '_RLock', '_SHUTTING_DOWN', '__all__', '__builtins__', '__cached__', '__doc__', '__excepthook__', '__file__', '__loader__', '__name__', '__package__', '__spec__', '_active', '_active_limbo_lock', '_after_fork', '_allocate_lock', '_count', '_counter', '_dangling', '_deque', '_enumerate', '_islice', '_limbo', '_main_thread', '_maintain_shutdown_locks', '_make_invoke_excepthook', '_newname', '_os', '_profile_hook', '_register_atexit', '_set_sentinel', '_shutdown', '_shutdown_locks', '_shutdown_locks_lock', '_start_new_thread', '_sys', '_threading_atexits', '_time', '_trace_hook', 'activeCount', 'active_count', 'currentThread', 'current_thread', 'enumerate', 'excepthook', 'functools', 'get_ident', 'get_native_id', 'getprofile', 'gettrace', 'local', 'main_thread', 'setprofile', 'settrace', 'stack_size']
```

​		这些函数、类和变量是Python的 `threading` 模块中与多线程编程相关的内部成员。以下是这些成员的解释：

- `Barrier`: 线程屏障对象，用于同步多个线程的执行。

- `BoundedSemaphore`: 有界信号量，用于控制资源的访问。

- `BrokenBarrierError`: 当Barrier对象破坏时引发的异常。

- `Condition`: 条件变量，用于实现线程之间的协调。

- `Event`: 事件对象，用于线程之间的通信和同步。

- `ExceptHookArgs`: 异常处理的参数对象。

- `Lock`: 锁对象，用于控制线程对共享资源的访问。

- `RLock`: 可重入锁，允许线程多次获得同一个锁。

- `Semaphore`: 信号量，用于控制同时访问某一资源的线程数量。

- `TIMEOUT_MAX`: 用于线程等待的最大超时时间。

- `Thread`: 线程类，用于创建和管理线程。

- `ThreadError`: 线程相关错误的异常类。

- `Timer`: 定时器类，用于在一段时间后执行指定操作。

- `WeakSet`: 弱引用集合，用于存储对象的弱引用。

- `_CRLock`: 一个基本的递归锁。

- `_DummyThread`: 内部类，用于充当假的线程对象。

- `_HAVE_THREAD_NATIVE_ID`: 表示是否支持原生线程标识符。

- `_MainThread`: 主线程对象。

- `_PyRLock`: 一个递归锁的C扩展实现。

- `_RLock`: 递归锁的C扩展实现。

- `_SHUTTING_DOWN`: 内部标志，表示是否正在关闭线程。

- `_active`: 活动线程的计数。

- `_active_limbo_lock`: 用于管理活动线程和"悬空"线程的锁。

- `_after_fork`: 在`fork()`之后需要重新初始化的内容。

- `_allocate_lock`: 内部函数，用于分配新锁。

- `_count`: 活动线程计数。

- `_counter`: 用于分配新线程名称的计数。

- `_dangling`: 存储被丢弃的线程的列表。

- `_deque`: 内部实现的双端队列。

- `_enumerate`: 用于枚举所有活动线程的函数。

- `_islice`: 内部切片实现。

- `_limbo`: 用于存储"悬空"线程的集合。

- `_main_thread`: 主线程对象。

- `_maintain_shutdown_locks`: 用于管理线程关闭锁的函数。

- `_make_invoke_excepthook`: 内部函数，用于调用异常处理。

- `_newname`: 内部函数，用于为新线程分配名称。

- `_os`: 内部操作系统相关功能。

- `_profile_hook`: 用于线程执行过程中的性能分析。

- `_register_atexit`: 内部函数，用于注册退出时的回调。

- `_set_sentinel`: 用于标记线程已退出。

- `_shutdown`: 内部函数，用于关闭线程。该函数被用于实际关闭线程。

- `_shutdown_locks`: 用于管理线程关闭锁的列表，用于确保线程被适当地关闭。

- `_shutdown_locks_lock`: 内部锁，用于保护关闭锁的管理。

- `_start_new_thread`: 用于启动新线程的底层函数。接受一个函数作为参数，用于线程的执行。

- `_sys`: 内部系统相关功能。

- `_threading_atexits`: 用于管理线程退出时的回调函数的列表。

- `_time`: 内部时间相关功能。

- `_trace_hook`: 用于线程执行过程中的跟踪功能。

- `activeCount` / `active_count`: 返回当前活动线程的数量。

- `currentThread` / `current_thread`: 返回当前线程对象。

- `enumerate`: 返回当前活动线程的一个列表。

- `excepthook`: 全局异常处理函数，处理线程异常。

- `functools`: functools模块，提供函数工具。

- `get_ident`: 返回当前线程的标识符。

- `get_native_id`: 返回当前线程的原生标识符。

- `getprofile`: 获取线程的全局profile函数。

- `gettrace`: 获取线程的全局trace函数。

- `local`: 用于创建线程本地数据对象。

- `main_thread`: 返回主线程对象。

- `setprofile`: 设置线程的全局profile函数。

- `settrace`: 设置线程的全局trace函数。

- `stack_size`: 用于设置线程堆栈大小。

​		这些函数、类和变量提供了在Python的 `threading` 模块中用于管理多线程编程的各种功能。它们使开发人员能够创建、控制和同步线程，以及处理多线程编程中的各种情况和需求。注意，使用这些功能需要了解多线程编程的基本概念和技术，以便合理地设计和管理多线程应用程序。



以下是`threading`模块中常用的函数按照功能进行分类总结：

- **线程创建与管理：**

| 函数名                             | 功能描述                 |
| ---------------------------------- | ------------------------ |
| `Thread`                           | 创建一个新线程对象       |
| `current_thread` / `currentThread` | 返回当前线程对象         |
| `enumerate`                        | 返回当前活动线程的列表   |
| `main_thread`                      | 返回主线程对象           |
| `get_ident`                        | 获取当前线程的标识符     |
| `get_native_id`                    | 获取当前线程的原生标识符 |
| `stack_size`                       | 设置线程的堆栈大小       |

- **线程同步与互斥：**

| 函数名                           | 功能描述             |
| -------------------------------- | -------------------- |
| `Lock`                           | 创建一个互斥锁对象   |
| `RLock`                          | 创建一个可重入锁对象 |
| `Semaphore` / `BoundedSemaphore` | 创建信号量对象       |
| `Barrier`                        | 创建线程屏障对象     |
| `Condition`                      | 创建条件变量对象     |
| `Event`                          | 创建事件对象         |
| `Timer`                          | 创建定时器对象       |

- **全局设置与操作：**

| 函数名                         | 功能描述                   |
| ------------------------------ | -------------------------- |
| `setprofile`                   | 设置线程的全局profile函数  |
| `getprofile`                   | 获取线程的全局profile函数  |
| `settrace`                     | 设置线程的全局trace函数    |
| `gettrace`                     | 获取线程的全局trace函数    |
| `excepthook`                   | 设置线程的全局异常处理函数 |
| `activeCount` / `active_count` | 返回当前活动线程的数量     |

​		这些函数提供了在多线程编程中创建、管理、同步和控制线程所需的基本功能。需要根据不同的应用场景选择适当的函数来实现多线程任务的编写与管理。同时，了解如何正确使用这些函数可以帮助避免线程安全和同步问题，确保多线程应用程序的正确执行。

### 24.5.3 线程的应用

​		当然，以下是多线程的优势和应用的中文描述表格：

| **多线程的优势**    | **应用场景**                                                 |
| ------------------- | ------------------------------------------------------------ |
| **1. 并发处理**     | - Web服务器同时处理多个客户端请求。<br>- 实时数据处理。      |
| **2. 提高响应性**   | - 用户界面可以在执行后台任务的同时保持响应。<br>- 处理I/O密集型操作，如读写文件。 |
| **3. 资源共享**     | - 在单个进程中多个线程之间共享数据。<br>- 在连接导向的应用程序中进行资源池化。 |
| **4. 任务分割**     | - 将大型任务分割为小的子任务，以便并行执行。<br>- 并行数据处理。 |
| **5. 多核CPU利用**  | - 在多核CPU上，充分利用多个线程并行执行的能力。<br>- 执行CPU密集型任务，如科学模拟。 |
| **6. 复杂计算**     | - 并行处理复杂的计算或模拟，提高性能。<br>- 密码学和数值计算。 |
| **7. 并发网络操作** | - 同时处理多个网络连接。<br>- Web抓取或并发下载文件。        |
| **8. 图形界面应用** | - 在执行后台任务的同时保持用户界面的响应性。<br>- 更新UI元素而不冻结界面。 |
| **9. 实时处理**     | - 实时传感器数据处理和控制系统。<br>- 多媒体处理和流媒体。   |
| **10. 异步操作**    | - 在主程序继续执行的同时异步运行任务。<br>- 同时处理多个异步事件。 |

​		需要注意的是，尽管多线程具有各种优势，但也会引入线程安全性、同步和潜在死锁等挑战。适当的设计和同步机制对于确保多线程应用程序的正确行为至关重要。

## 24.6 多进程

### 24.6.1 概念

​		通过使用Python的`multiprocessing`模块，你可以实现多进程编程，从而充分利用多核处理器，提高程序性能和并发处理能力。

| **概念**                | **描述**                                                     |
| ----------------------- | ------------------------------------------------------------ |
| **多进程**              | 在Python中，多进程是一种并发编程技术，允许同时运行多个独立的进程，每个进程都有自己独立的内存空间和系统资源。多进程编程可以通过利用多核处理器，实现任务的并行执行，提高程序性能和并发处理能力。 |
| **进程对象**            | 使用`multiprocessing.Process`类创建进程对象。每个进程对象代表一个要执行的独立进程。可以将一个函数或方法分配给进程对象的`target`参数，这个函数将在新的进程中执行。 |
| **进程的创建和启动**    | 通过进程对象的`start()`方法启动新的进程执行。一旦进程启动，它将在独立的进程空间中执行指定的函数。 |
| **进程间通信（IPC）**   | 由于每个进程有独立的内存空间，进程之间的通信需要使用特定的IPC机制，如`multiprocessing.Queue`、`multiprocessing.Pipe`等，在进程之间传递数据。 |
| **进程的等待和同步**    | 使用进程对象的`join()`方法可以等待进程执行完成，确保主程序等待子进程的结束。`multiprocessing`模块还提供了锁和信号量等同步机制。 |
| **进程池**              | `multiprocessing.Pool`类允许创建进程池，其中包含多个预先创建的进程。适用于需要执行多个相似任务的情况，可以有效地管理和重用进程。 |
| **全局解释器锁（GIL）** | 不同于线程，Python的多进程中，每个进程有自己独立的Python解释器和GIL，不受其他进程影响。这允许在多核处理器上充分利用并行性。 |

​		在Python中，可以使用`multiprocessing`模块来实现多进程编程，从而允许并发地执行多个独立的进程。以下是使用`multiprocessing`模块创建和管理多进程的一些常见操作和示例：

1. **导入模块：** 首先，需要导入`multiprocessing`模块。

```python
import multiprocessing
```

2. **创建进程对象：** 使用`multiprocessing.Process`类来创建进程对象。通过为进程对象指定`target`参数，将要在新进程中执行的函数传递给它。

```python
def worker_function(number):
    print(f"Process {number} started")
    # 执行一些任务
    print(f"Process {number} completed")

# 创建进程对象
process1 = multiprocessing.Process(target=worker_function, args=(1,))
process2 = multiprocessing.Process(target=worker_function, args=(2,))
```

3. **启动进程执行：** 使用进程对象的`start()`方法可以启动新进程的执行。

```python
# 启动进程执行
process1.start()
process2.start()
```

4. **等待进程完成：** 使用进程对象的`join()`方法可以等待进程执行完成，以确保主程序等待子进程的结束。

```python
# 等待进程完成
process1.join()
process2.join()
```

​		完整示例代码：

```python
import multiprocessing

def worker_function(number):
    print(f"Process {number} started")
    # 执行一些任务
    print(f"Process {number} completed")

if __name__ == "__main__":
    # 创建进程对象
    process1 = multiprocessing.Process(target=worker_function, args=(1,))
    process2 = multiprocessing.Process(target=worker_function, args=(2,))
    
    # 启动进程执行
    process1.start()
    process2.start()
    
    # 等待进程完成
    process1.join()
    process2.join()
    
    print("All processes have finished")
```

​		在这个示例中，我们创建了两个进程对象`process1`和`process2`，每个进程执行了`worker_function`函数中的任务。通过启动进程并使用`join()`方法等待进程完成，我们可以实现并发地执行多个进程。需要注意的是，为了避免在Windows平台上出现问题，最好将进程相关的代码放在`if __name__ == "__main__":`块中。

### 24.6.2 进程同步

​	

- **进程同步方式**

​		下面是锁、信号量、条件变量、事件和队列这些不同的进程同步方式的对比：

| 进程同步方式          | 用途和特点                                               | 使用时机                                 |
| --------------------- | -------------------------------------------------------- | ---------------------------------------- |
| 锁（Lock）            | 用于保护临界区，确保只有一个进程可以访问共享资源。       | 当需要控制对共享资源的互斥访问时。       |
| 信号量（Semaphore）   | 用于控制允许访问资源的进程数量，允许一定并发访问。       | 当需要限制一定数量的进程并发访问资源时。 |
| 条件变量（Condition） | 用于等待特定条件满足后再进行操作，可配合锁使用。         | 当需要在满足某些条件后才继续执行时。     |
| 事件（Event）         | 用于在一个进程发出信号后唤醒另一个进程。                 | 当需要等待其他进程发出信号后继续执行时。 |
| 队列（Queue）         | 用于在多个进程之间传递数据，确保数据传递的顺序和安全性。 | 当需要安全地传递数据并保持顺序时。       |

这些不同的进程同步方式具有不同的特点和适用场景。根据实际需求，可以选择合适的同步机制来保证多进程环境中的协调和资源共享。

### 24.6.3 进程并发

在 Python 中实现多进程并发操作通常涉及以下步骤：

1. **导入模块：** 首先，导入需要的模块，通常会使用`multiprocessing`模块来处理多进程相关操作。

2. **定义任务函数：** 创建一个或多个函数，这些函数将在多个进程中并发执行。这些函数应该是独立的，不共享数据，以确保并发执行时的安全性。

3. **创建进程：** 使用`multiprocessing.Process`类创建多个进程，每个进程对应一个任务函数。

4. **启动进程：** 使用进程对象的`start()`方法来启动各个进程，使它们开始并发执行。

5. **等待进程完成：** 使用进程对象的`join()`方法等待所有进程执行完毕。

以下是一个简单的示例，演示了如何使用多进程并发执行任务：

```python
import multiprocessing
import time

def worker(task):
    print(f"Task {task} started.")
    time.sleep(2)  # 模拟耗时操作
    print(f"Task {task} completed.")

if __name__ == "__main__":
    tasks = ["task1", "task2", "task3", "task4"]
    processes = []

    for task in tasks:
        p = multiprocessing.Process(target=worker, args=(task,))
        processes.append(p)
        p.start()

    for p in processes:
        p.join()

    print("All tasks completed.")
```

在这个示例中，我们创建了多个进程来并发执行`worker`函数，每个函数模拟执行一个耗时操作。通过`start()`方法启动进程，使用`join()`方法等待所有进程执行完毕。

注意，每个进程有独立的内存空间，不共享数据，因此在多进程并发操作时需要注意数据的同步和共享问题。在实际应用中，可能需要使用锁、队列等机制来确保数据的安全访问。

### 24.6.2 函数

```python
>>> import multiprocessing
>>> dir(multiprocessing)
['Array', 'AuthenticationError', 'Barrier', 'BoundedSemaphore', 'BufferTooShort', 'Condition', 'Event', 'JoinableQueue', 'Lock', 'Manager', 'Pipe', 'Pool', 'Process', 'ProcessError', 'Queue', 'RLock', 'RawArray', 'RawValue', 'SUBDEBUG', 'SUBWARNING', 'Semaphore', 'SimpleQueue', 'TimeoutError', 'Value', '__all__', '__builtins__', '__cached__', '__doc__', '__file__', '__loader__', '__name__', '__package__', '__path__', '__spec__', 'active_children', 'allow_connection_pickling', 'context', 'cpu_count', 'current_process', 'freeze_support', 'get_all_start_methods', 'get_context', 'get_logger', 'get_start_method', 'log_to_stderr', 'parent_process', 'process', 'reducer', 'reduction', 'set_executable', 'set_forkserver_preload', 'set_start_method', 'sys']
```



以下是对列出的一些 `multiprocessing` 模块中常见属性和函数的解释：

- **Array：** 用于创建一个共享数组，可以在多个进程之间共享数据。
- **AuthenticationError：** 身份验证错误，当进程间通信的身份验证失败时引发。
- **Barrier：** 栅栏，用于在多个进程之间同步，等待所有进程都达到一个点。
- **BoundedSemaphore：** 有界信号量，限制了信号量的最大计数。
- **BufferTooShort：** 缓冲区过短，用于 `multiprocessing` 模块内部。
- **Condition：** 条件变量，用于线程之间的协调和同步。
- **Event：** 事件对象，用于线程之间的通信，一个线程可以等待事件的设置。
- **JoinableQueue：** 可跟踪任务的完成状态的队列。
- **Lock：** 锁对象，用于线程之间的互斥访问共享资源。
- **Manager：** 管理器对象，用于在多进程之间共享 Python 对象，如列表、字典等。
- **Pipe：** 进程之间的管道通信方式。
- **Pool：** 进程池，用于创建一组进程来执行任务，可以提高任务执行的效率。
- **Process：** 进程类，用于创建新的进程。
- **ProcessError：** 进程错误，当进程出现问题时引发。
- **Queue：** 队列对象，用于在多进程之间传递数据。
- **RLock：** 递归锁，类似于 Lock，但允许同一线程多次获取锁。
- **RawArray 和 RawValue：** 与 Array 和 Value 类似，但创建的是不安全的原始数据。
- **Semaphore：** 信号量对象，用于控制多进程对共享资源的访问。
- **SimpleQueue：** 简单队列，类似于 Queue，但没有 task_done 和 join 方法。
- **TimeoutError：** 超时错误，当一个操作在指定时间内没有完成时引发。
- **Value：** 创建一个共享的 ctypes 值，在多进程之间共享数据。

- **__all__：** 这是一个包含了模块中所有公共接口的列表，当使用 `from module import *` 语句导入模块时，只会导入该列表中的接口。

- **__builtins__：** 这是一个指向内置命名空间的字典，其中包含 Python 解释器的内置函数、异常和其他对象。

- **__cached__：** 这是模块的缓存文件的路径，用于加速模块的加载。模块在首次加载时会被编译并保存在这个缓存文件中，以便下次加载时可以直接使用。

- **__doc__：** 这是模块的文档字符串，可以通过 `help(module)` 或 `module.__doc__` 获取模块的说明文档。

- **__file__：** 这是模块的文件路径，指示了模块源代码所在的位置。

- **__loader__：** 这是一个加载器对象，用于从文件系统或其他地方加载模块。

- **__name__：** 这是模块的名称，当模块作为主程序运行时，它的值为 `'__main__'`，当作为模块被导入时，它的值是模块的名字。

- **__package__：** 这是模块的包名，如果模块不是在包中，则值为 `None`。

- **__path__：** 这是一个包含模块所在包的文件夹路径的列表，如果模块不在一个包中，则该属性不存在。

- **__spec__：** 这是一个模块规范对象，提供了关于模块的更多信息，如模块的来源、加载器等。

- **active_children：** 返回一个包含所有活动子进程的列表，用于在程序中管理正在运行的子进程。

- **allow_connection_pickling：** 控制是否允许进程之间的连接的对象序列化（pickling）和反序列化（unpickling），默认为 `False`。

以下是 `multiprocessing` 模块中列出的一些特殊属性和函数的解释：

- **context：** 这是一个上下文对象，用于创建并管理进程和线程间的共享资源。

- **cpu_count：** 返回计算机的核心数，用于确定进程池的大小。

- **current_process：** 返回当前进程的 Process 对象。

- **freeze_support：** 在 Windows 上用于“冻结”可执行文件，使其可以使用 `multiprocessing` 模块。

- **get_all_start_methods：** 返回所有可用的进程启动方法，如 'fork'、'spawn'、'forkserver'。

- **get_context：** 返回一个进程上下文对象，用于创建和管理进程。

- **get_logger：** 返回一个进程特定的日志记录器。

- **get_start_method：** 返回当前进程的启动方法。

- **log_to_stderr：** 将进程的日志记录到标准错误流。

- **parent_process：** 返回当前进程的父进程。

- **process：** 一个 `Process` 类的别名，用于创建新的进程。

- **reducer 和 reduction：** 用于序列化和反序列化进程间共享的 Python 对象。

- **set_executable：** 设置进程可执行文件的名称。

- **set_forkserver_preload：** 设置在使用 forkserver 启动方法时，是否预加载模块。

- **set_start_method：** 设置进程的启动方法。

- **sys：** 包含了与 Python 解释器交互的函数和变量。

​	以下是根据功能将 `multiprocessing` 模块中的属性和函数划分的表格：

| 功能                     | 函数和属性                                                   |
| ------------------------ | ------------------------------------------------------------ |
| **进程管理和创建**       | Process, current_process, active_children                    |
| **上下文和配置**         | context, get_context                                         |
| **进程池和并发**         | Pool, cpu_count, freeze_support, get_all_start_methods       |
| **启动方法和配置**       | get_start_method, set_start_method                           |
| **日志和输出**           | log_to_stderr, get_logger                                    |
| **进程间通信和共享资源** | Array, Value, Lock, RLock, Semaphore, BoundedSemaphore, Event, Condition, Barrier, Queue, JoinableQueue, Pipe |
| **其它功能**             | parent_process, reducer, reduction, set_executable, set_forkserver_preload |

​		这个表格按照不同的功能将 `multiprocessing` 模块中的函数和属性进行了分类，有助于您更清晰地了解它们的用途和功能。

### 24.6.3 进程的应用

​		以下是关于Python多进程应用场景的表格：

| 应用场景       | 描述                                                   |
| -------------- | ------------------------------------------------------ |
| 并行计算       | 加速并行计算、大数据处理、模型训练等任务。             |
| 网络服务器     | 提高网络服务器的并发性能，处理多个客户端请求。         |
| 数据处理和分析 | 并行处理大量数据，加速数据清洗、转换、分析等操作。     |
| 图像处理       | 并行处理图像操作，如缩放、滤波、裁剪等。               |
| 并行算法       | 使用多进程执行并行算法，如排序、搜索等任务。           |
| 科学计算       | 并行求解复杂的数学模型，减少计算时间。                 |
| 并行测试       | 并行运行单元测试或集成测试，提高测试效率。             |
| 爬虫和数据采集 | 并行处理多个爬取任务，加速爬虫的速度和效率。           |
| 多媒体处理     | 并行处理音频、视频处理、转码等任务。                   |
| 并行任务调度   | 处理批量处理、定时任务等需求，实现任务并行调度和执行。 |

​		这个表格展示了Python多进程在不同应用场景中的应用，帮助提高程序的性能和效率，同时充分利用多核和多处理器系统的优势。

## 24.7 协程

### 24.7.1 概念

​		协程（Coroutine）是一种并发编程的技术，允许程序在执行过程中暂停并恢复，以实现非阻塞的异步编程。Python 使用 `async` 和 `await` 关键字来定义和管理协程，从而实现异步操作。协程通常用于处理 I/O 密集型任务，如网络请求、文件操作等，以提高程序的性能和效率。

​		以下是关于Python协程的一些重要概念和用法：

1. **定义协程：** 使用 `async def` 关键字定义一个协程函数。协程函数中可以使用 `await` 关键字等待异步操作的结果。

```python
async def async_function():
    # 异步操作
    result = await async_operation()
    return result
```

2. **事件循环（Event Loop）：** 使用 `asyncio` 模块中的事件循环来管理协程的执行。事件循环调度协程的执行顺序，使其在不阻塞整个程序的情况下进行切换。

```python
import asyncio

async def main():
    # 创建事件循环
    loop = asyncio.get_event_loop()
    # 运行协程
    result = await async_function()
    print(result)

# 启动事件循环
asyncio.run(main())
```

3. **异步操作：** 协程可以与异步操作（如 I/O 操作、定时器等）结合使用，从而实现并发处理。

```python
async def async_io_operation():
    # 异步 I/O 操作
    await asyncio.sleep(1)
    return "Async I/O operation completed"

async def main():
    result = await async_io_operation()
    print(result)

asyncio.run(main())
```

4. **协程的并发控制：** 使用 `asyncio` 提供的锁、信号量等可以控制协程的并发执行，避免竞争条件。

```python
async def concurrent_coroutines():
    async with asyncio.Lock():
        # 保证同一时刻只有一个协程执行
        await asyncio.sleep(1)
        print("Concurrent coroutine completed")

async def main():
    coroutines = [concurrent_coroutines() for _ in range(5)]
    await asyncio.gather(*coroutines)

asyncio.run(main())
```

​        Python的协程提供了一种有效的方式来处理异步编程，使得编写异步代码更加直观和可读。通过使用协程，可以在单线程中同时执行多个任务，从而提高程序的性能。

### 24.7.2 应用

​		下面是关于协程应用的表格：

| 应用场景     | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| 网络请求     | 处理多个网络请求，加速数据获取和处理，适用于爬虫、API 调用等。 |
| Web 框架     | 基于协程的异步 Web 框架如 FastAPI、Sanic，处理并发客户端请求。 |
| 数据库操作   | 使用异步数据库客户端处理多个数据库操作，提高数据查询和更新效率。 |
| 异步文件操作 | 并发进行文件的读取和写入操作，适用于处理大型文件。           |
| 事件驱动编程 | 处理事件驱动任务，如用户输入、传感器数据等，实现实时响应。   |
| 并发下载     | 同时下载多个文件，提高下载速度。                             |
| 消息队列处理 | 处理消息队列消费者任务，如 RabbitMQ、Kafka 等。              |
| 定时任务     | 处理定时任务，如定时发送邮件、数据备份等。                   |
| 并发测试     | 进行并发测试，模拟多个用户并发访问应用。                     |
| 协程池       | 创建协程池，对协程进行调度和管理，控制并发执行数量。         |
| 游戏开发     | 处理游戏中的复杂角色行为、AI 逻辑等。                        |
| 实时数据处理 | 处理实时数据流，如传感器数据、实时日志等。                   |

​		协程在许多不同领域都有广泛的应用，能够优化异步编程，提高程序的性能和效率。

## 24.8 区别总结

### 24.8.1 同步、异步、并发的区别

​		下面是同步、异步和并发这三个概念的区别：

| 特征       | 同步                                                         | 异步                                                         | 并发                                                     |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------------------------- |
| 定义       | 调用方需要等待被调用方完成操作后才继续执行，调用方会阻塞。   | 调用方不需要等待被调用方完成操作，可以继续执行其他任务，不会阻塞。 | 同一时间内处理多个任务，任务可能是同步的也可能是异步的。 |
| 阻塞       | 调用方会阻塞，等待被调用方完成后才能继续执行。               | 不会阻塞，可以继续执行其他任务。                             | 通常会伴随着异步执行，但不一定。                         |
| 任务顺序   | 严格按照任务的调用顺序依次执行。                             | 任务的执行顺序可能会乱序，由系统决定。                       | 任务的执行顺序可能会交错，由调度器决定。                 |
| 资源利用率 | 通常情况下，可能导致资源的低效利用，因为调用方在等待期间无法做其他事情。 | 资源的利用率高，调用方可以在等待期间做其他事情。             | 资源的利用率高，能够同时处理多个任务。                   |
| 编程风格   | 编程风格较为直观，任务的执行顺序清晰。                       | 编程风格相对复杂，需要处理异步回调或者使用协程等技术。       | 编程风格相对复杂，需要考虑任务的并发执行和同步问题。     |
| 示例       | 同步函数、阻塞 I/O 操作。                                    | 异步函数、非阻塞 I/O 操作。                                  | 多线程、多进程、协程等。                                 |

​			虽然同步、异步和并发是不同的概念，但它们在编程中经常会交织在一起。在处理复杂的任务和优化程序性能时，了解这些概念的区别以及如何正确应用它们是非常重要的。

### 24.8.2多线程、多进程和协程的区别



​			下面是多线程、多进程和协程这三个概念的区别：

| 特征           | 多线程                                                       | 多进程                                                       | 协程                                                         |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 定义           | 同一进程中的多个线程共享进程的资源，运行在同一地址空间中。   | 每个进程都有自己独立的内存空间，进程间通信较为复杂。         | 在同一线程中的协程共享线程的资源，通过协程切换实现任务切换，运行在同一地址空间中。 |
| 并发执行       | 同一进程中的多个线程可以并发执行，利用多核处理器实现并行。   | 多个进程可以并发执行，各进程之间是独立的，可以利用多核处理器实现并行。 | 在同一线程中的多个协程可以并发执行，通过协程切换实现并发，利用单个线程实现并行。 |
| 资源共享       | 线程共享同一进程的资源，访问和修改资源可能需要锁来保证线程安全。 | 进程之间资源独立，通信复杂，可通过进程间通信(IPC)来传递数据。 | 协程共享同一线程的资源，通过协程切换来保证资源共享的线程安全性。 |
| 内存占用       | 相对较小，因为线程共享进程的内存空间。                       | 相对较大，因为每个进程有独立的内存空间。                     | 相对较小，因为协程共享线程的内存空间，协程切换开销较小。     |
| 创建和销毁开销 | 创建和销毁开销较小。                                         | 创建和销毁开销较大。                                         | 创建和销毁开销较小。                                         |
| 编程难度       | 相对较复杂，需要考虑线程安全性和锁等问题。                   | 相对较复杂，需要考虑进程间通信和数据传递问题。               | 相对较简单，不需要考虑线程安全性和进程间通信问题，但需要处理协程切换和异步编程问题。 |
| 示例           | 并发访问共享资源，如多线程下载、Web 服务器等。               | 并发执行独立任务，如多进程爬虫、数据处理等。                 | 并发执行多个 I/O 密集型任务，如异步 Web 服务器、网络爬虫等。 |

​			虽然多线程、多进程和协程都是用于处理并发和并行编程的方式，但它们各自有自己的优势和适用场景。了解它们的区别和特点，可以根据不同的任务需求选择合适的并发编程方式。



## 24.9并发类库

​			下面是常用的并发类库及其特点的表格：

| 并发类库           | 特点                                                         |
| ------------------ | ------------------------------------------------------------ |
| threading          | Python标准库的线程模块，提供基本的线程管理和同步工具。       |
| multiprocessing    | Python标准库的多进程模块，用于创建和管理多进程，支持进程间通信。 |
| asyncio            | Python标准库的异步编程模块，提供协程和事件循环来实现异步任务。 |
| concurrent.futures | Python标准库的高层次接口，简化线程池和进程池的使用，适用于并行执行函数。 |
| threading2         | 第三方库，扩展了Python标准库的threading模块，提供更多功能和更好的性能。 |
| futures            | 第三方库，提供更多的线程和进程池的功能，包括ThreadPoolExecutor和ProcessPoolExecutor。 |
| gevent             | 第三方库，基于协程的并发库，提供异步I/O和协程切换，简化并发编程。 |
| greenlet           | 第三方库，提供协程支持，可用于构建自己的协程调度系统。       |
| curio              | 第三方库，用于异步I/O和并发编程，支持协程和异步上下文管理器。 |
| trio               | 第三方库，类似于curio的库，专注于异步编程和协程。            |
| joblib             | 第三方库，用于处理计算密集型任务，支持并行计算、内存映射、序列化等功能。 |
| pykka              | 第三方库，提供轻量级的并发编程支持，基于Actor模型处理并发任务。 |
| dask               | 第三方库，用于处理大数据集和分布式计算，提供并行计算和调度功能。 |

​		这些并发类库在不同场景下有不同的优势和适用性，可以根据项目需求选择合适的库来处理并发编程。

## 24.10 I/0交互

### 24.10.1 区别

#### 24.10.1.1 五种I/O



在并发编程中，常见的五种I/O交互方式是：阻塞I/O、非阻塞I/O、同步I/O、异步I/O和多路复用。下面是这五种I/O交互方式的区别：

| I/O交互方式 | 描述                                                         | 优点                                      | 缺点                                         | 示例应用                        |
| ----------- | ------------------------------------------------------------ | ----------------------------------------- | -------------------------------------------- | ------------------------------- |
| 阻塞I/O     | 在执行I/O操作时，线程或进程会被阻塞，直到I/O操作完成。       | 简单易用，适用于单线程或单进程环境。      | 阻塞会导致其他任务无法继续执行，效率低下。   | 文件读写、网络请求等            |
| 非阻塞I/O   | 在执行I/O操作时，线程或进程不会被阻塞，但需要不断地查询是否有数据就绪。 | 可以在不阻塞其他任务的情况下进行I/O操作。 | 需要不断地轮询I/O状态，造成CPU资源浪费。     | 轮询查询文件、网络套接字的状态  |
| 同步I/O     | 在执行I/O操作时，线程或进程会等待I/O操作完成，并在完成后继续执行后续代码。 | 结构清晰，易于理解。                      | 阻塞导致其他任务无法继续执行。               | 读写文件、网络请求等            |
| 异步I/O     | 在执行I/O操作时，线程或进程不会等待I/O操作完成，而是继续执行后续代码。通过回调或异步协程来处理I/O完成后的操作。 | 可以处理大量并发连接，避免阻塞。          | 编程模型较复杂，需要处理回调或使用异步协程。 | 异步Web服务器、高并发网络应用等 |
| 多路复用    | 使用一个线程或进程来同时监控多个I/O操作，当有任何一个I/O操作就绪时，即可进行处理，避免了不断的轮询查询。 | 资源占用较少，能够处理大量并发连接。      | 逻辑复杂，需要使用特定的多路复用机制。       | 高并发服务器、聊天应用等        |

​		这五种I/O交互方式各自适用于不同的场景和需求。选择合适的方式可以根据项目的性质、需求和并发程度。



#### 24.10.1.2 同步阻塞、同步非阻塞、异步阻塞和异步非阻塞



以下是对同步阻塞、同步非阻塞、异步阻塞和异步非阻塞这四种不同的I/O交互方式的简要描述：

| I/O交互方式                             | 描述                                                         | 示例                                 |
| --------------------------------------- | ------------------------------------------------------------ | ------------------------------------ |
| 同步阻塞（Blocking Synchronous）        | 在同步阻塞中，执行一个操作将阻塞当前线程/进程，直到操作完成。程序会等待操作结束后继续进行下一步操作。 | 发起网络请求，等待响应返回。         |
| 同步非阻塞（Non-blocking Synchronous）  | 同步非阻塞操作仍然是同步的，但在执行期间不会阻塞当前线程/进程。通常采用轮询或回调方式，可以继续执行其他任务。 | 轮询检查文件是否就绪，等待用户输入。 |
| 异步阻塞（Blocking Asynchronous）       | 异步阻塞操作是异步的，但在执行期间会阻塞当前线程/进程，其他任务无法继续。虽然异步，但执行时仍然会等待操作完成。 | 调用一个异步函数并等待其结果。       |
| 异步非阻塞（Non-blocking Asynchronous） | 在异步非阻塞操作中，执行异步操作时，可以继续进行其他任务，操作完成后通过回调或通知来处理结果。不会阻塞当前线程/进程。 | 使用回调函数处理异步操作的结果。     |

这些不同的交互方式在处理I/O操作时有不同的特点和用途，了解它们有助于更好地选择合适的方法来满足不同的需求。

#### 24.10.1.3 同步复用、异步复用

**同步复用（Synchronous Multiplexing）** 和 **异步复用（Asynchronous Multiplexing）** 都是在网络编程中常用的技术，用于实现在单个线程或进程中处理多个连接的方式，从而提高并发性能。

**同步复用**：
在同步复用中，通常使用系统提供的I/O多路复用机制（如`select()`、`poll()`、`epoll()`等），这些机制允许我们在一个线程/进程中同时监控多个I/O事件，当有事件就绪时，阻塞的方式通知程序进行相应的处理。虽然多个连接在一个线程中被监控，但在处理每个连接时，通常还是采用同步阻塞的方式进行。

**异步复用**：
异步复用则采用了异步的方式，通过使用异步I/O库（如`asyncio`、`twisted`等）来实现。在异步复用中，一个事件循环会监控多个I/O操作，但在处理连接时，不会像同步复用那样阻塞线程，而是通过异步的方式处理多个连接，从而允许程序在等待一个连接的I/O操作时，继续处理其他连接的I/O操作。



### 24.10.2 代码



#### 24.10.2.1 五种I/o



下面是针对不同I/O交互方式的示例说明：

1. **阻塞I/O**：
   - 示例：使用阻塞I/O进行文件读取
   - 描述：当使用阻塞I/O进行文件读取时，程序会一直等待文件读取完成，直到文件读取操作完成后，才会继续执行后续代码。
   - 代码示例：
   ```python
   with open('file.txt', 'r') as f:
       content = f.read()  # 阻塞，直到文件读取完成
   ```

2. **非阻塞I/O**：
   - 示例：使用非阻塞I/O查询网络套接字状态
   - 描述：程序会不断查询网络套接字的状态，如果有数据就绪，就会进行数据的读取或写入操作。
   - 代码示例：
   ```python
   import socket
   
   sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
   sock.setblocking(0)  # 设置为非阻塞模式
   try:
       sock.connect(('example.com', 80))
   except BlockingIOError:
       pass
   ```

3. **同步I/O**：
   - 示例：使用同步I/O进行文件写入
   - 描述：程序会等待文件写入操作完成，然后继续执行后续代码。
   - 代码示例：
   ```python
   with open('output.txt', 'w') as f:
       f.write('Hello, world!')  # 阻塞，直到文件写入完成
   ```

4. **异步I/O**：
   - 示例：使用异步I/O进行并发网络请求
   - 描述：多个网络请求可以并发进行，不需要等待某个请求完成后再进行下一个请求。
   - 代码示例（使用`asyncio`库）：
   ```python
   import asyncio
   
   async def fetch_url(url):
       async with aiohttp.ClientSession() as session:
           async with session.get(url) as response:
               return await response.text()
   
   urls = ['http://example.com', 'http://example.org', 'http://example.net']
   loop = asyncio.get_event_loop()
   results = loop.run_until_complete(asyncio.gather(*[fetch_url(url) for url in urls]))
   ```

5. **多路复用**：
   - 示例：使用`select`进行多路复用
   - 描述：程序通过`select`调用同时监控多个I/O事件，当有任何一个I/O事件就绪时，就会进行处理。
   - 代码示例：
   ```python
   import socket
   import select
   
   server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
   server.bind(('0.0.0.0', 8080))
   server.listen(5)
   
   inputs = [server]
   while True:
       readable, writable, exceptional = select.select(inputs, [], [])
       for sock in readable:
           if sock == server:
               client, addr = server.accept()
               inputs.append(client)
           else:
               data = sock.recv(1024)
               if data:
                   sock.send(data)
               else:
                   sock.close()
                   inputs.remove(sock)
   ```

​		这些示例展示了不同I/O交互方式的使用情况，每种方式在不同的场景下都有各自的优势和应用。



#### 24.10.2.2 同步阻塞、同步非阻塞、异步阻塞、异步非阻塞



​		下面我将通过Python代码来演示这四种不同的I/O交互方式。

​		首先，我们使用Python的`time.sleep()`函数来模拟耗时的操作，然后使用不同的方式进行交互：

```python
import time

# 同步阻塞
def synchronous_blocking():
    print("Synchronous Blocking: Start")
    time.sleep(3)  # 模拟耗时操作
    print("Synchronous Blocking: End")

# 同步非阻塞
def synchronous_non_blocking():
    print("Synchronous Non-blocking: Start")
    while True:
        time.sleep(1)
        print("Doing other tasks while waiting for operation to complete")
        if some_condition:  # 假设某个条件满足时退出循环
            break
    print("Synchronous Non-blocking: End")

# 异步阻塞
import asyncio

async def asynchronous_blocking():
    print("Asynchronous Blocking: Start")
    await asyncio.sleep(3)  # 模拟异步阻塞操作
    print("Asynchronous Blocking: End")

# 异步非阻塞
async def asynchronous_non_blocking():
    print("Asynchronous Non-blocking: Start")
    while True:
        await asyncio.sleep(1)
        print("Doing other tasks while waiting for async operation to complete")
        if some_condition:  # 假设某个条件满足时退出循环
            break
    print("Asynchronous Non-blocking: End")

# 使用同步阻塞方式
synchronous_blocking()

# 使用同步非阻塞方式
synchronous_non_blocking()

# 使用异步阻塞方式
asyncio.run(asynchronous_blocking())

# 使用异步非阻塞方式
asyncio.run(asynchronous_non_blocking())
```

​		请注意，代码中的`some_condition`是一个占位符，表示某个条件满足时退出循环，以模拟在非阻塞情况下可以继续执行其他任务。

​		通过运行上述代码，您可以看到不同I/O交互方式的区别，以及如何在不同方式下进行操作。

#### 24.10.2.3 同步复用和异步复用





在同步复用中，虽然可以监控多个连接，但每个连接的处理还是同步的，一个连接的I/O操作会阻塞整个线程/进程。而在异步复用中，连接的处理是异步的，允许多个连接的I/O操作并发执行，不会阻塞整个线程/进程。

下面是一个简单的示例，演示了同步复用和异步复用的概念：

**同步复用示例**：
```python
import select
import socket

server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server_socket.bind(('127.0.0.1', 8888))
server_socket.listen(5)

inputs = [server_socket]

while True:
    readable, _, _ = select.select(inputs, [], [])
    for sock in readable:
        if sock == server_socket:
            client_socket, client_addr = server_socket.accept()
            inputs.append(client_socket)
        else:
            data = sock.recv(1024)
            if data:
                sock.send(data)
            else:
                sock.close()
                inputs.remove(sock)
```

**异步复用示例**（使用`asyncio`库）：
```python
import asyncio

async def handle_client(reader, writer):
    data = await reader.read(100)
    message = data.decode()
    addr = writer.get_extra_info('peername')
    print(f"Received {message} from {addr}")
    print("Send: %r" % message)
    writer.write(data)
    await writer.drain()
    print("Closing the connection")
    writer.close()

async def main():
    server = await asyncio.start_server(handle_client, '127.0.0.1', 8888)
    addr = server.sockets[0].getsockname()
    print(f'Serving on {addr}')
    async with server:
        await server.serve_forever()

asyncio.run(main())
```

这两个示例展示了同步复用和异步复用的基本概念，以及它们在处理多个连接时的不同方式。



### 24.10.3 通俗解释



#### 24.10.3.1  五种I/O



假设有一个餐厅，里面有一位服务员和多名顾客，他们需要点餐、等待餐点准备以及享受美食。这个情景可以用来解释不同的I/O交互方式：

1. **阻塞I/O**：# 顺序执行
   在这个餐厅中，服务员会根据顾客的点餐顺序，依次将菜单上的餐点送至厨房，等待餐点准备完成后再将餐点端到顾客桌前。在这个过程中，服务员会被每个餐点的准备时间所阻塞，直到一个餐点准备好，才会继续处理下一个餐点。

2. **非阻塞I/O**： # 查询状态 选择执行
   在这个餐厅中，服务员会在厨房送餐的同时，不断地查询厨房的状态，看是否有餐点已经准备好。如果有餐点准备好了，服务员就会将其送至顾客桌前，如果没有准备好，服务员会继续查询。这样，服务员可以充分利用时间，不会被单个餐点的准备时间所阻塞。

3. **同步I/O**： # 全部执行后再 继续操作
   在这个餐厅中，服务员会依次接收每个顾客的点餐需求，然后将这些需求交给厨房，等待所有餐点都准备好后，再一次性将所有餐点端到顾客桌前。在这个过程中，服务员需要等待所有餐点都准备好后才能继续。

4. **异步I/O**： # 查询状态 
   在这个餐厅中，服务员会在接收顾客点餐的同时，将餐点准备的任务委托给厨房，并立即返回接待下一个顾客。当餐点准备好后，厨房会通知服务员，服务员再将餐点送至对应的顾客桌前。这样，服务员可以同时接待多个顾客，不需要等待餐点准备的过程。

5. **多路复用**：# 采用标签记录完成状态，通过标签 监控
   在这个餐厅中，服务员使用一个便签来记录每个顾客的点餐需求，然后在便签上不断查看是否有餐点准备好，一旦有餐点准备好，就将餐点送至对应的顾客桌前。这样，服务员可以同时监控多个餐点的准备状态，不需要依次等待每个餐点的准备。

通过这个小故事，可以更好地理解不同的I/O交互方式在并发环境中的应用和特点。







#### 24.10.3.2 同步阻塞、同步非阻塞、异步阻塞和异步非阻塞



让我们通过一个小故事来说明这四种不同的I/O交互方式：

故事背景：小明是一名忙碌的学生，他需要在晚上完成学习和休息。

1. **同步阻塞**：小明坐下来开始做作业，每完成一道题目后，他都会停下来等待老师的批改。在等待的过程中，他不能进行其他任何事情，必须等待批改完成后才能继续做下一道题目。

2. **同步非阻塞**：小明换了一种策略。他开始做作业后，每完成一道题目，就把它放在一旁，然后开始做其他事情，比如做一些练习题或者整理笔记。不过，他时不时地会回过头来看看老师是否已经批改完前面的题目。一旦老师批改完成，他就立即处理批改结果并继续做作业。

3. **异步阻塞**：这次，小明决定将作业上传到在线作业平台上，然后等待老师批改。在上传的过程中，他无法做其他事情，必须等待作业批改完成。虽然上传是异步的，但他在上传期间仍然被阻塞，不能做其他事情。

4. **异步非阻塞**：最后，小明尝试了一种全新的方法。他开始做作业，但并不等待老师批改。他继续做其他的学习任务，如背单词、阅读材料等，同时随时留意通知。一旦老师批改完成，系统会通知他，他可以立即查看批改结果并继续进行下一步。

这个小故事向我们展示了这四种I/O交互方式的不同特点。不同的方式在处理任务时有不同的策略，有的会阻塞当前进程/线程，有的允许进行其他任务。每种方式在不同的场景下都有自己的优势和适用性。



#### 24.10.3.3 同步复用和异步复用

​		当然，来听一个新的故事，来解释同步复用和异步复用：

**小故事：火车站上的旅客**

​		在一个繁忙的火车站上，有许多旅客需要购买车票和候车。火车站的工作人员采用了不同的方式来处理旅客的需求。

**同步复用的火车站**： 单个进程

​		在同步复用的火车站中，窗口只有一个，旅客必须排队等待他们的购票和咨询服务。每个旅客必须一一进行操作，直到他们的需求得到满足。这导致了队伍很长，需要花费较长时间等待。

**异步复用的火车站**    多个进程

​		在异步复用的火车站中，有多个服务窗口，每个窗口可以处理不同的任务。旅客可以自由选择窗口，进行购票、咨询和其他服务。每个窗口都可以独立处理旅客的需求，而不需要其他窗口的操作干扰。此外，火车站还设置了大屏幕显示器，上面显示着不同的服务窗口的空闲情况和操作流程，旅客可以根据自己的需求选择最合适的窗口。

​		这就好比在异步复用的火车站中，旅客可以自由选择窗口进行操作，不需要等待其他人的操作完成，而在同步复用的火车站中，旅客需要按顺序等待自己的操作被处理完毕。

​		通过这个小故事，我们可以更好地理解同步复用和异步复用的区别，以及它们在处理多个任务时的不同方式。





# 二十五、网络编程

## 25.1 网络模型

- 网络模型是一种用于理解和描述计算机网络体系结构的框架。有两种主要的网络模型：OSI（Open Systems Interconnection）七层网络模型和TCP/IP五层网络模型。它们都是用来分解网络通信的各个层次，以便更好地理解网络协议、功能和通信流程。

  这里是OSI七层网络模型和TCP/IP五层网络模型的简要比较：

  | 层级   | OSI七层网络模型               | TCP/IP五层网络模型                    |
  | ------ | ----------------------------- | ------------------------------------- |
  | 第七层 | 应用层（Application Layer）   | 应用层（Application Layer）           |
  | 第六层 | 表示层（Presentation Layer）  | 无                                    |
  | 第五层 | 会话层（Session Layer）       | 无                                    |
  | 第四层 | 传输层（Transport Layer）     | 传输层（Transport Layer）             |
  | 第三层 | 网络层（Network Layer）       | 网际层（Internet Layer）              |
  | 第二层 | 数据链路层（Data Link Layer） | 网络接口层（Network Interface Layer） |
  | 第一层 | 物理层（Physical Layer）      | 物理层（Physical Layer）              |

  - **应用层（Application Layer）**: 处理用户应用程序和网络之间的通信。包括各种网络服务，如HTTP、FTP、SMTP等。

  - **表示层（Presentation Layer）**: 处理数据的格式化、加密和压缩，确保数据在不同系统间的正确解释。

  - **会话层（Session Layer）**: 管理和维护应用程序之间的通信会话。

  - **传输层（Transport Layer）**: 负责端到端的通信，提供数据传输服务，主要的协议有TCP和UDP。

  - **网络层（Network Layer）**: 处理逻辑寻址和路由选择，使数据能够跨越不同的网络传输。

  - **数据链路层（Data Link Layer）**: 管理物理寻址和数据帧的传输，包括将数据帧划分为比特并管理物理连接。

  - **物理层（Physical Layer）**: 负责传输介质的物理连接，处理比特流的传输。

    ​	需要注意的是，OSI模型具有七层，而TCP/IP模型只有五层。TCP/IP模型中将表示层和会话层合并到了应用层，而将数据链路层和物理层合并到了网络接口层。这两种模型都是用来帮助解释和描述计算机网络通信的结构和协议，但在实际应用中，更常用的是TCP/IP模型。

- 

## 25.1 网络编程简介

​		Python是一种强大的编程语言，也被广泛用于网络编程。它提供了丰富的标准库和第三方库，使网络编程变得更加简单和高效。下面我会简要介绍一些Python中常用的网络编程模块和技术。

- **socket模块：** Python的`socket`模块是进行网络编程的基础工具。它提供了套接字（sockets）接口，可以用于创建客户端和服务器，实现不同计算机之间的通信。
- **urllib和urllib2模块：** 这些模块用于处理URL和HTTP请求，可以用于访问网页内容、下载文件等。
- **requests库：** `requests`是一个流行的第三方库，用于处理HTTP请求和响应。它使HTTP通信更加简单，并提供了丰富的功能。
- **socketserver模块：** 这个模块提供了一个基于套接字的服务器框架，可以更轻松地创建多线程或多进程服务器。
- **asyncio库：** `asyncio`是Python的异步I/O库，用于编写异步网络应用程序。它提供了协程和事件循环，支持高性能的异步编程。
- **Twisted框架：** `Twisted`是一个异步网络编程框架，适用于构建高性能和可扩展的网络应用程序。
- **Flask和Django框架：** 这些Web框架可以用于构建Web应用程序，处理HTTP请求和响应，并提供了许多方便的功能。
- **WebSocket库：** `websockets`库提供了实现WebSocket通信的功能，用于实时通信和交互。
- **网络协议处理：** Python也支持各种网络协议的处理，如SMTP（电子邮件协议）、POP3（邮件接收协议）、FTP（文件传输协议）等。

## 25.2 网络协议

下面是关于TCP/IP、HTTP、HTTPS、FTP、SMTP、POP3、IMAP、DNS、WebSocket、SSH、UDP这些协议的简要说明：

| 协议      | 描述                                                         | 应用场景                           |
| --------- | ------------------------------------------------------------ | ---------------------------------- |
| TCP/IP    | 一组协议，用于在互联网上进行数据通信，包括IP用于路由和寻址、TCP用于可靠数据传输等。 | 互联网通信、数据传输               |
| HTTP      | 超文本传输协议，用于在客户端和服务器之间传输超文本数据，通常用于请求和传输Web页面和资源。 | 网页浏览、Web应用通信              |
| HTTPS     | 安全超文本传输协议，是HTTP的加密版本，使用SSL/TLS加密传输数据，保证数据的安全性和隐私。 | 加密敏感信息的网页通信、在线支付等 |
| FTP       | 文件传输协议，用于在计算机之间传输文件，支持上传、下载和管理文件。 | 文件传输、备份                     |
| SMTP      | 简单邮件传输协议，用于发送电子邮件。                         | 邮件发送                           |
| POP3      | 邮局协议版本3，用于接收电子邮件，允许用户从邮件服务器下载自己的邮件。 | 接收电子邮件                       |
| IMAP      | 互联网消息访问协议，用于接收和管理电子邮件，允许在服务器上管理邮件，包括文件夹和标签。 | 接收和管理电子邮件                 |
| DNS       | 域名系统，用于将域名转换为IP地址，实现域名和IP地址之间的映射。 | 域名解析、浏览器访问网址           |
| WebSocket | 一种全双工通信协议，允许客户端和服务器保持长时间的连接，用于实时通信和交互。 | 实时通信、在线聊天                 |
| SSH       | 安全外壳协议，用于在网络中安全地远程连接到其他计算机，执行命令和管理远程系统。 | 远程管理、安全连接                 |
| UDP       | 用户数据报协议，无连接、不可靠的传输协议，适用于实时性要求较高、数据量小的场景。 | 实时音视频传输、游戏通信等         |























