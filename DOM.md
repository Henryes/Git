
# DOM
- HTML控制展示内容，CSS控制样式显示，JavaScript赋予HTML行为。利用BOM对象来操作浏览器对象。DOM提供接口让我们操作HTML元素。
- window.onload function() 加载完网页执行
- var imgWidth = imgs[0].offsetWidth;通过offsetWidth可以获得图片的宽度；offsetWidth 属于dom样式设置的内容
- parseInt(imgs[j].style.left,10) imgs[j].style.left的值含有单位px不能直接数值运算，需要先转化为数字，通过parseInt()来进行转化
# 文档类型
- 超文本标记语言，HTML(Help Text Markup Language)W3C万维网联盟维护
  用来显示数据，重点是如何显示数据
  使用定义的标准标签，html标签作为根元素
- 可扩展标记语言，XML(Extensable Markup Language)
  用来描述数据，重点是什么是数据，如何存放数据
# 节点的属性
- nodeName
- nodeValue
- nodeType

# nodeName 属性规定节点的名称

- nodeName 是只读的
- 元素节点的 nodeName 与标签名相同
- 属性节点的 nodeName 是属性的名称
- 文本节点的 nodeName 永远是 #text
- 文档节点的 nodeName 永远是 #document

 # nodetype：文档节点类型

判断节点类型的方法

 定义一个节点：


    <div id="content">内容</div>

- 使用JavaScript判断——定义变量divNode，通过id获取节点并赋值给变量：
		
    var divNode = document.getElementById("content");

- if或switch语句判断节点类型

- （获取节点divNode的节点类型）
			
    divNode.nodeType ==Node.ELEMENT_NODE(或者1）

- 【相比较的节点类型的字符常量（或者数字常量）】
alert（）语句回应。




