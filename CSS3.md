# css
- transition 使网页的一个属性值平滑过度到另一个值
- animation 可在不使用js的情况下实现复杂酷炫的动画效果 
- transition:<过渡属性名称><过渡时间><过渡模式>
- safari、chrome浏览器用webkit-transition
- firefox用moz-transition
- opera用o-transition
- 过渡模式分为五种：ease（缓慢开始，缓慢结束），linear（匀速），ease-in（缓慢开始），ease-out（缓慢结束），ease-in-out（缓慢开始，缓慢结束，和ease稍有区别）
# 3D场景
- 浏览器作为窗口，三维物体距离窗口的距离：
webkit-perspective:800px代表物体离屏幕距离800
- 视点，对应x轴，y轴:
webkit-perspective-origin:50% 50%代表从物体中心观看物体
- 用webkit-transform-style：-webkit-preserve-3d告诉浏览器设置的是3D场景

- 用transform属性调整元素：

translate：

    translateX（x px）translateY（）translateZ（）

rotate：

    rotateX（）rotateY（）rotateZ（）

# translate属性
- webkit-transform: translateZ 轴方向整体平移 
- webkit-transform: rotateY(45deg) 以轴为圆心旋转
- 滑竿控件：<input type="range" min="-360"max="360" id="transtatex" value="0" class="reange-control" onchange="translateall()" />
- html5中，input type="range"即是滑杆。
# transform-origin调整旋转中心：

- x轴：left，center，right
- y轴：top，center，bottom
- z轴：length px

# 图片延伸
- 方式有三种，round/repeat/stretch
- round（平铺）:可理解为圆满的平铺，为了实现圆满所以会压缩/拉伸

- repeat（重复）：一直重复，超出部分剪裁掉，而且是居中开始重复

- stretch（拉伸）：有多长拉多长，若不填写则默认为stretch

# css颜色

	    角度               用英文                     作用

		0deg               to top                   从下向上

		90deg              to right                 从左向右

		180deg             to bottom                从上向下

		270deg             to left                  从右向左

                           to top left              右下角到左上角

                           to top right             左下角到右上角


# 字体
- 设置文字溢出时显示为省略号

		 text-overflow:ellipsis; 
		 overflow:hidden; 
		 white-space:nowrap; 
- 嵌入新的字体

    	  @font-face {
   		     font-family : 字体名称;
   		     src : 字体文件在服务器上的相对或绝对路径;
   	      }
- 文本阴影
- X-Offset：表示阴影的水平偏移距离，其值为正值时阴影向右偏移，反之向左偏移；      
- Y-Offset：是指阴影的垂直偏移距离，如果其值是正值时，阴影向下偏移，反之向上偏移；
- Blur：是指阴影的模糊程度，其值不能是负值，如果值越大，阴影越模糊，反之阴影越清晰，如果不需要阴影模糊可以将Blur值设置为0；
- Color：是指阴影的颜色，其可以使用rgba色。

#



