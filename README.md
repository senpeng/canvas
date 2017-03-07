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
