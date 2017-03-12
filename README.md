# canvas
canvas demo


####HTML5 Canvas中绘制直线的属性和方法：
    * strokeStyle       # 用于设置画笔绘制路径的颜色、渐变和模式
    * lineWidth         # 定义绘制线条的宽度
    * beginPath()       # 开始一个新的绘制路径
    * moveTo(x, y)      # 移动画笔到指定的坐标点(x, y)，该点就是新的子路径的起始点
    * lineTo(x, y)      # 使用直线连接当前端点和指定的坐标点(x, y)
    * stroke()          # 沿着绘制路径的坐标点顺序绘制直线
    * closePath()       # 如果当前的绘制路径是打开的，则关闭掉该绘制路径


#####线段与像素边界
	* 在某2个像素的边界处绘制一条1像素宽的线段,该线段实际上会占据2个像素的宽度
		* 如果在像素边界处绘制一条1像素宽的垂直线段，那么Canvas的绘图环境对象会试着将半个像素  
		画在边界中线的右边，将另外半个像素画在边界中线的左边。然而，在一个整像素的范围内绘制
		半个像素宽的线段是不可能的，所以左右两个方向上的半像素都被扩展为1个像素。
	* 在某2个像素中的一个像素中绘制一条1像素宽的线段，该像素刚好占据1个像素的宽度
		* 中线左右两端的那半个像素就不会再延伸
	* 如果绘制一条真正1像素宽的线段，必须将该线段绘制在某两个像素之间的那个像素中，而不能将它  绘制在两个像素的交界处。

#####绘制虚线
	* setLineDash(segments) 	# 设置虚线样式
		* segments：一个Array数组。一组描述交替绘制线段和间距（坐标空间单位）长度的数字。 如果数组元素的数量是奇数，   
		数组的元素会被复制并重复。例如， [5, 15, 25] 会变成 [5, 15, 25, 5, 15, 25]。
