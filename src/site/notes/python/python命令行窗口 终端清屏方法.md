---
{"dg-publish":true,"dg-home":false,"permalink":"/python/python命令行窗口 终端清屏方法/","dgPassFrontmatter":true,"created":"2024-10-26T21:14:01.124+08:00","updated":"2024-10-26T23:06:43.426+08:00"}
---


当窗口命令行太多了，进行清屏
```python
import os
def clear()
	os.system('cls')
clear()	
```
当然也可以不用定义
```python
import os
os.system('cls')
```