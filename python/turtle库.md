---
dg-publish: true
dg-home: false
---
# 绘图坐标体系、
使用turtle.setup()设置窗口的大小和位置
```python
turtle.setup(width,height,startx,starty)
```

如果输入整数，表示像素值；如果小数，表示宽度与屏幕的比例（适用w和h）
- width:窗口宽度
- height:窗口高度
- startx:窗口左侧到屏幕左侧的像素距离，如果是None，窗口位于屏幕水平中央（位于中间竖直线的位置）
- starty:窗口顶部到屏幕顶部的像素距离，如果是None，窗口位于屏幕垂直中央（窗口顶部直接触顶）

刚开始绘制时，默认在图中央，方向**水平向右**

# 画笔控制函数
- penup和pendown
	- turtle.penup()
	 抬起画笔，简写为：turtle.up()/turtle.pu()
	 - turtle.pendown()
	 落下画笔，简写为：turtle.down()/turtle.pd()
- pensize
turtle.pensize()
简写：turtle.width()
设置画笔宽度，不输入参数时会返回当前画笔宽度
- pencolor
设置画笔颜色，不输入参数会返回当前画笔颜色
可以输入颜色字符串，例如("black")
还可以输入RGB，例如(255 255 255)白色

# 形状绘制函数
- turtle.fd()
行走距离
可以输入负数来反方向走
- turtle.seth()
改变方向的度数
- turtle.circle()
画弧形
turtle.circle(半径,角度)
半径>0逆时针转，<0顺时针转
不输入角度时默认画整个圆形
