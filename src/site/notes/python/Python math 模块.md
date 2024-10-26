---
{"dg-publish":true,"dg-home":false,"permalink":"/python/Python math 模块/","dgPassFrontmatter":true,"created":"2024-10-26T21:14:00.376+08:00","updated":"2024-10-26T23:06:34.658+08:00"}
---


# [Python math 模块 | 菜鸟教程](https://www.runoob.com/python3/python-math.html)

Python **math** 模块提供了许多对浮点数的数学运算函数。

**math** 模块下的函数，返回值均为浮点数，除非另有明确说明。

如果你需要计算复数，请使用 cmath 模块中的同名函数。

要使用 math 函数必须先导入：

import math

查看 math 模块中的内容:

\>>> import math  
\>>> dir(math)  
\['\_\_doc\_\_', '\_\_file\_\_', '\_\_loader\_\_', '\_\_name\_\_', '\_\_package\_\_', '\_\_spec\_\_', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'lcm', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'nextafter', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc', 'ulp'\]  

### math 模块常量

| 常量 | 描述 |
| --- | --- |
| [math.e](https://www.runoob.com/python3/ref-math-e.html) | 返回欧拉数 (2.7182...) |
| [math.inf](https://www.runoob.com/python3/ref-math-inf.html) | 返回正无穷大浮点数 |
| [math.nan](https://www.runoob.com/python3/ref-math-nan.html) | 返回一个浮点值 NaN (not a number) |
| [math.pi](https://www.runoob.com/python3/ref-math-pi.html) | π 一般指圆周率。 圆周率 PI (3.1415...) |
| [math.tau](https://www.runoob.com/python3/ref-math-tau.html) | 数学常数 τ = 6.283185...，精确到可用精度。Tau 是一个圆周常数，等于 2π，圆的周长与半径之比。 |

### math 模块方法

| 方法 | 描述 |
| --- | --- |
| [math.acos(x)](https://www.runoob.com/python3/ref-math-acos.html) | 返回 x 的反余弦，结果范围在 0 到 pi 之间。 |
| [math.acosh(x)](https://www.runoob.com/python3/ref-math-acosh.html) | 返回 x 的反双曲余弦值。 |
| [math.asin(x)](https://www.runoob.com/python3/ref-math-asin.html) | 返回 x 的反正弦值，结果范围在 -pi/2 到 pi/2 之间。 |
| [math.asinh(x)](https://www.runoob.com/python3/ref-math-asinh.html) | 返回 x 的反双曲正弦值。 |
| [math.atan(x)](https://www.runoob.com/python3/ref-math-atan.html) | 返回 x 的反正切值，结果范围在 -pi/2 到 pi/2 之间。 |
| [math.atan2(y, x)](https://www.runoob.com/python3/ref-math-atan2.html) | 返回给定的 X 及 Y 坐标值的反正切值，结果是在 -pi 和 pi 之间。 |
| [math.atanh(x)](https://www.runoob.com/python3/ref-math-atanh.html) | 返回 x 的反双曲正切值。 |
| [math.ceil(x)](https://www.runoob.com/python3/ref-math-ceil.html) | 将 x 向上舍入到最接近的整数 |
| [math.comb(n, k)](https://www.runoob.com/python3/ref-math-comb.html) | 返回不重复且无顺序地从 n 项中选择 k 项的方式总数。 |
| [math.copysign(x, y)](https://www.runoob.com/python3/ref-math-copysign.html) | 返回一个基于 x 的绝对值和 y 的符号的浮点数。 |
| [math.cos()](https://www.runoob.com/python3/ref-math-cos.html) | 返回 x 弧度的余弦值。 |
| [math.cosh(x)](https://www.runoob.com/python3/ref-math-cosh.html) | 返回 x 的双曲余弦值。 |
| [math.degrees(x)](https://www.runoob.com/python3/ref-math-degrees.html) | 将角度 x 从弧度转换为度数。 |
| [math.dist(p, q)](https://www.runoob.com/python3/ref-math-dist.html) | 返回 p 与 q 两点之间的欧几里得距离，以一个坐标序列（或可迭代对象）的形式给出。 两个点必须具有相同的维度。 |
| [math.erf(x)](https://www.runoob.com/python3/ref-math-erf.html) | 返回一个数的误差函数 |
| [math.erfc(x)](https://www.runoob.com/python3/ref-math-erfc.html) | 返回 x 处的互补误差函数 |
| [math.exp(x)](https://www.runoob.com/python3/ref-math-exp.html) | 返回 e 的 x 次幂，Ex， 其中 e = 2.718281... 是自然对数的基数。 |
| [math.expm1()](https://www.runoob.com/python3/ref-math-expm1.html) | 返回 Ex - 1， e 的 x 次幂，Ex，其中 e = 2.718281... 是自然对数的基数。这通常比 math.e \*\* x 或 pow(math.e, x) 更精确。 |
| [math.fabs(x)](https://www.runoob.com/python3/ref-math-fabs.html) | 返回 x 的绝对值。 |
| [math.factorial(x)](https://www.runoob.com/python3/ref-math-factorial.html) | 返回 x 的阶乘。 如果 x 不是整数或为负数时则将引发 ValueError。 |
| [math.floor()](https://www.runoob.com/python3/ref-math-floor.html) | 将数字向下舍入到最接近的整数 |
| [math.fmod(x, y)](https://www.runoob.com/python3/ref-math-fmod.html) | 返回 x/y 的余数 |
| [math.frexp(x)](https://www.runoob.com/python3/ref-math-frexp.html) | 以 (m, e) 对的形式返回 x 的尾数和指数。 m 是一个浮点数， e 是一个整数，正好是 x == m \* 2\*\*e 。 如果 x 为零，则返回 (0.0, 0) ，否则返回 0.5 <= abs(m) < 1 。 |
| [math.fsum(iterable)](https://www.runoob.com/python3/ref-math-fsum.html) | 返回可迭代对象 (元组, 数组, 列表, 等)中的元素总和，是浮点值。 |
| [math.gamma(x)](https://www.runoob.com/python3/ref-math-gamma.html) | 返回 x 处的伽马函数值。 |
| [math.gcd()](https://www.runoob.com/python3/ref-math-gcd.html) | 返回给定的整数参数的最大公约数。 |
| [math.hypot()](https://www.runoob.com/python3/ref-math-hypot.html) | 返回欧几里得范数，sqrt(sum(x\*\*2 for x in coordinates))。 这是从原点到坐标给定点的向量长度。 |
| [math.isclose(a,b)](https://www.runoob.com/python3/ref-math-isclose.html) | 检查两个值是否彼此接近，若 a 和 b 的值比较接近则返回 True，否则返回 False。。 |
| [math.isfinite(x)](https://www.runoob.com/python3/ref-math-isfinite.html) | 判断 x 是否有限，如果 x 既不是无穷大也不是 NaN，则返回 True ，否则返回 False 。 |
| [math.isinf(x)](https://www.runoob.com/python3/ref-math-isinf.html) | 判断 x 是否是无穷大，如果 x 是正或负无穷大，则返回 True ，否则返回 False 。 |
| [math.isnan()](https://www.runoob.com/python3/ref-math-isnan.html) | 判断数字是否为 NaN，如果 x 是 NaN（不是数字），则返回 True ，否则返回 False 。 |
| [math.isqrt()](https://www.runoob.com/python3/ref-math-isqrt.html) | 将平方根数向下舍入到最接近的整数 |
| [math.ldexp(x, i)](https://www.runoob.com/python3/ref-math-ldexp.html) | 返回 x \* (2\*\*i) 。 这基本上是函数 [math.frexp() 的反函数。](https://www.runoob.com/python3/ref-math-frexp.html) |
| [math.lgamma()](https://www.runoob.com/python3/ref-math-lgamma.html) | 返回伽玛函数在 x 绝对值的自然对数。 |
| [math.log(x\[, base\])](https://www.runoob.com/python3/ref-math-log.html) | 使用一个参数，返回 x 的自然对数（底为 e ）。 |
| [math.log10(x)](https://www.runoob.com/python3/ref-math-log10.html) | 返回 x 底为 10 的对数。 |
| [math.log1p(x)](https://www.runoob.com/python3/ref-math-log1p.html) | 返回 1+x 的自然对数（以 e 为底）。 |
| [math.log2(x)](https://www.runoob.com/python3/ref-math-log2.html) | 返回 x 以 2 为底的对数 |
| [math.perm(n, k=None)](https://www.runoob.com/python3/ref-math-perm.html) | 返回不重复且有顺序地从 n 项中选择 k 项的方式总数。 |
| [math.pow(x, y)](https://www.runoob.com/python3/ref-math-pow.html) | 将返回 x 的 y 次幂。 |
| [math.prod(iterable)](https://www.runoob.com/python3/ref-math-prod.html) | 计算可迭代对象中所有元素的积。 |
| [math.radians(x)](https://www.runoob.com/python3/ref-math-radians.html) | 将角度 x 从度数转换为弧度。 |
| [math.remainder(x, y)](https://www.runoob.com/python3/ref-math-remainder.html) | 返回 IEEE 754 风格的 x 除于 y 的余数。 |
| [math.sin(x)](https://www.runoob.com/python3/ref-math-sin.html) | 返回 x 弧度的正弦值。 |
| [math.sinh(x)](https://www.runoob.com/python3/ref-math-sinh.html) | 返回 x 的双曲正弦值。 |
| [math.sqrt(x)](https://www.runoob.com/python3/ref-math-sqrt.html) | 返回 x 的平方根。 |
| [math.tan(x)](https://www.runoob.com/python3/ref-math-tan.html) | 返回 x 弧度的正切值。 |
| [math.tanh(x)](https://www.runoob.com/python3/ref-math-tanh.html) | 返回 x 的双曲正切值。 |
| [math.trunc(x)](https://www.runoob.com/python3/ref-math-trunc.html) | 返回 x 截断整数的部分，即返回整数部分，删除小数部分 |