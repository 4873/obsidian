[[ReadItLater]] [[Article]]

# [Python Try Except](https://www.w3school.com.cn/python/python_try_except.asp)

## Python Try Except

-   [Python PIP](https://www.w3school.com.cn/python/python_pip.asp "Python PIP")
-   [Python 命令输入](https://www.w3school.com.cn/python/python_cmd_input.asp "Python 命令行输入")

**`try` 块允许您测试代码块以查找错误。**

**`except` 块允许您处理错误。**

**`finally` 块允许您执行代码，无论 try 和 except 块的结果如何。**

## 异常处理

当我们调用 Python 并发生错误或异常时，通常会停止并生成错误消息。

可以使用 `try` 语句处理这些异常：

### 实例

try 块将生成异常，因为 x 未定义：

try:
  print(x)
except:
  print("An exception occurred")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_1)

由于 try 块引发错误，因此会执行 except 块。

如果没有 try 块，程序将崩溃并引发错误：

### 实例

该语句将引发错误，因为未定义 x：

print(x)

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_error)

## 多个异常

您可以根据需要定义任意数量的 exception 块，例如，假如您要为特殊类型的错误执行特殊代码块：

### 实例

如果 try 块引发 `NameError`，则打印一条消息，如果是其他错误则打印另一条消息：

try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_2)

## Else

如果没有引发错误，那么您可以使用 `else` 关键字来定义要执行的代码块：

### 实例

在本例中，`try` 块不会生成任何错误：

try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_3)

## Finally

如果指定了 `finally` 块，则无论 try 块是否引发错误，都会执行 finally 块。

### 实例

try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_4)

这对于关闭对象并清理资源非常有用：

### 实例

试图打开并写入不可写的文件：

try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=python_try_except_5)

程序可以继续，而且不会打开文件对象。

## 引发异常

作为 Python 开发者，您可以选择在条件发生时抛出异常。

如需抛出（引发）异常，请使用 `raise` 关键词。

### 实例

假如 x 小于 0，则引发异常并终止程序：

x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=demo_python_ref_keyword_raise_1)

`raise` 关键字用于引发异常。

您能够定义所引发异常的类型、以及打印给用户的文本。

### 实例

如果 x 不是整数，则引发 TypeError：

x = "hello"

if not type(x) is int:
  raise TypeError("Only integers are allowed")

[运行实例](https://www.w3school.com.cn/tiy/t.asp?f=demo_python_ref_keyword_raise_2)

-   [Python PIP](https://www.w3school.com.cn/python/python_pip.asp "Python PIP")
-   [Python 命令输入](https://www.w3school.com.cn/python/python_cmd_input.asp "Python 命令行输入")