如果需要在程序中自行引发异常，则应使用 raise 语句。raise 语句有如下三种常用的用法：

1. raise：单独一个 raise。该语句引发当前上下文中捕获的异常（比如在 except 块中），或默认引发 RuntimeError 异常。
2. raise 异常类：raise 后带一个异常类。该语句引发指定异常类的默认实例。
3. raise 异常对象：引发指定的异常对象。

`raise 异常 `后面还可以加入异常描述，下面的实例就有运用到。

当然，我们手动让程序引发异常，很多时候并不是为了让其崩溃。事实上，raise 语句引发的异常通常用 `try except（else finally）`异常处理结构来捕获并进行处理。例如：

```
try:
a = input("输入一个数：")
     #判断用户输入的是否为数字
     if(not a.isdigit()):
              raise ValueError("a 必须是数字")
except ValueError as e:
     print("引发异常：",repr(e))
```

可以看到，当用户输入的不是数字时，程序会执行 raise 引发 ValueError 异常。但由于其位于 try 块中，因为 raise 而抛出的异常会被 try 捕获，并跳转到 except 块进行处理。  
  
因此，虽然程序中使用了 raise 语句引发异常，但程序的执行是正常的，手动抛出的异常并不会导致程序崩溃。


这里涉及到了[[try except]]结构
