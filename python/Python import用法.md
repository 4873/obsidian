

# [Python导入模块，Python import用法（超级详细）](http://c.biancheng.net/view/2397.html)

使用 Python 进行编程时，有些功能没必须自己实现，可以借助 Python 现有的标准库或者其他人提供的第三方库。比如说，在前面章节中，我们使用了一些数学函数，例如余弦函数 cos()、绝对值函数 fabs() 等，它们位于 Python 标准库中的 math（或 cmath）模块中，只需要将此模块导入到当前程序，就可以直接拿来用。

前面章节中，已经看到使用 import 导入模块的语法，但实际上 import 还有更多详细的用法，主要有以下两种：

1.  `import 模块名1 [as 别名1], 模块名2 [as 别名2]，…`：使用这种语法格式的 import 语句，会导入指定模块中的所有成员（包括变量、函数、类等）。不仅如此，当需要使用模块中的成员时，需用该模块名（或别名）作为前缀，否则 Python 解释器会报错。
2.  `from 模块名 import 成员名1 [as 别名1]，成员名2 [as 别名2]，…`： 使用这种语法格式的 import 语句，只会导入模块中指定的成员，而不是全部成员。同时，当程序中使用该成员时，无需附加任何前缀，直接使用成员名（或别名）即可。

注意，用 \[\] 括起来的部分，可以使用，也可以省略。

其中，第二种 import 语句也可以导入指定模块中的所有成员，即使用 form 模块名 import ＊，但此方式不推荐使用，具体原因本节后续会做详细说明。

## import 模块名 as 别名

下面程序使用导入整个模块的最简单语法来导入指定模块：

\# 导入sys整个模块
import sys
# 使用sys模块名作为前缀来访问模块中的成员
print(sys.argv\[0\])

上面第 2 行代码使用最简单的方式导入了 sys 模块，因此在程序中使用 sys 模块内的成员时，必须添加模块名作为前缀。

运行上面程序，可以看到如下输出结果（sys 模块下的 argv 变量用于获取运行 Python 程序的命令行参数，其中 argv\[0\] 用于获取当前 Python 程序的存储路径）：

C:\\Users\\mengma\\Desktop\\hello.py

导入整个模块时，也可以为模块指定别名。例如如下程序：

\# 导入sys整个模块，并指定别名为s
import sys as s
# 使用s模块别名作为前缀来访问模块中的成员
print(s.argv\[0\])

第 2 行代码在导入 sys 模块时才指定了别名 s，因此在程序中使用 sys 模块内的成员时，必须添加模块别名 s 作为前缀。运行该程序，可以看到如下输出结果：

C:\\Users\\mengma\\Desktop\\hello.py

也可以一次导入多个模块，多个模块之间用逗号隔开。例如如下程序：

\# 导入sys、os两个模块
import sys,os
# 使用模块名作为前缀来访问模块中的成员
print(sys.argv\[0\])
# os模块的sep变量代表平台上的路径分隔符
print(os.sep)

上面第 2 行代码一次导入了 sys 和 os 两个模块，因此程序要使用 sys、os 两个模块内的成员，只要分别使用 sys、os 模块名作为前缀即可。在 Windows 平台上运行该程序，可以看到如下输出结果（os 模块的 sep 变量代表平台上的路径分隔符）：

C:\\Users\\mengma\\Desktop\\hello.py  
\\

在导入多个模块的同时，也可以为模块指定别名，例如如下程序：

\# 导入sys、os两个模块，并为sys指定别名s，为os指定别名o
import sys as s,os as o
# 使用模块别名作为前缀来访问模块中的成员
print(s.argv\[0\])
print(o.sep)

上面第 2 行代码一次导入了sys 和 os 两个模块，并分别为它们指定别名为 s、o，因此程序可以通过 s、o 两个前缀来使用 sys、os 两个模块内的成员。在 Windows 平台上运行该程序，可以看到如下输出结果：

C:\\Users\\mengma\\Desktop\\hello.py  
\\

## from  模块名 import 成员名 as 别名

下面程序使用了 from...import 最简单的语法来导入指定成员：

\# 导入sys模块的argv成员
from sys import argv
# 使用导入成员的语法，直接使用成员名访问
print(argv\[0\])

第 2 行代码导入了 sys 模块中的 argv 成员，这样即可在程序中直接使用 argv 成员，无须使用任何前缀。运行该程序，可以看到如下输出结果：

C:\\Users\\mengma\\Desktop\\hello.py

导入模块成员时，也可以为成员指定别名，例如如下程序：

\# 导入sys模块的argv成员，并为其指定别名v
from sys import argv as v
# 使用导入成员（并指定别名）的语法，直接使用成员的别名访问
print(v\[0\])

第 2 行代码导入了 sys 模块中的 argv 成员，并为该成员指定别名 v，这样即可在程序中通过别名 v 使用 argv 成员，无须使用任何前缀。运行该程序，可以看到如下输出结果：

C:\\Users\\mengma\\Desktop\\hello.py

form...import 导入模块成员时，支持一次导入多个成员，例如如下程序：

\# 导入sys模块的argv,winver成员
from sys import argv, winver
# 使用导入成员的语法，直接使用成员名访问
print(argv\[0\])
print(winver)

上面第 2 行代码导入了 sys 模块中的 argv、 winver 成员，这样即可在程序中直接使用 argv、winver 两个成员，无须使用任何前缀。运行该程序，可以看到如下输出结果（sys 的 winver 成员记录了该 Python 的版本号）：

C:\\Users\\mengma\\Desktop\\hello.py  
3.6

一次导入多个模块成员时，也可指定别名，同样使用 as 关键字为成员指定别名，例如如下程序：

\# 导入sys模块的argv,winver成员，并为其指定别名v、wv
from sys import argv as v, winver as wv
# 使用导入成员（并指定别名）的语法，直接使用成员的别名访问
print(v\[0\])
print(wv)

上面第 2 行代码导入了 sys 模块中的 argv、winver 成员，并分别为它们指定了别名 v、wv，这样即可在程序中通过 v 和 wv 两个别名使用 argv、winver 成员，无须使用任何前缀。运行该程序，可以看到如下输出结果：

C:\\Users\\mengma\\Desktop\\hello.py  
3.6

#### 不推荐使用 from import 导入模块所有成员

在使用 from...import 语法时，可以一次导入指定模块内的所有成员（此方式不推荐），例如如下程序：

\#导入sys 棋块内的所有成员
from sys import \*
\#使用导入成员的语法，直接使用成员的别名访问
print(argv\[0\])
print(winver)

上面代码一次导入了 sys 模块中的所有成员，这样程序即可通过成员名来使用该模块内的所有成员。该程序的输出结果和前面程序的输出结果完全相同。

需要说明的是，一般不推荐使用“from 模块 import”这种语法导入指定模块内的所有成员，因为它存在潜在的风险。比如同时导入 module1 和 module2 内的所有成员，假如这两个模块内都有一个 foo() 函数，那么当在程序中执行如下代码时：

foo()

上面调用的这个 foo() 函数到底是 module1 模块中的还是 module2 模块中的？因此，这种导入指定模块内所有成员的用法是有风险的。

但如果换成如下两种导入方式：

import module1  
import module2 as m2

接下来要分别调用这两个模块中的 foo() 函数就非常清晰。程序可使用如下代码：

\#使用模块module1 的模块名作为前缀调用foo()函数
module1.foo()
\#使用module2 的模块别名作为前缀调用foo()函数
m2.foo()

或者使用 from...import 语句也是可以的：

\#导入module1 中的foo 成员，并指定其别名为foo1
from module1 import foo as fool
\#导入module2 中的foo 成员，并指定其别名为foo2
from module2 import foo as foo2

此时通过别名将 module1 和 module2 两个模块中的 foo 函数很好地进行了区分，接下来分别调用两个模块中 foo() 函数就很清晰：

foo1() \#调用module1 中的foo()函数  
foo2() \#调用module2 中的foo()函数