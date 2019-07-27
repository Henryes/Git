# Javascript 确认
- 语法：confirm（str）
- str：消息对话框显示的文本
- 点确定按钮时返回true 取消false

		var mymessage = confirm("你喜欢JavaScript吗?");
		if (mymessage==true) {
			document.write("很好,加油!");
		} else {
			document.write("JS功能强大，要学习噢!");
		}

#js'提问
- prompt（str1）（str2）
- 1可修改 2不可修改 
> var myname=prompt("请输入你的姓名:");
if(myname!=null)
  {   alert("你好"+myname); }
else
  {  alert("你好 my friend.");  }

# js'打开新的窗口
- window.open([URL],[窗口名称],[参数字符串]);
 
> script type="text/javascript"> window.open('http://www.imooc.com','_blank','width=300,height=200,menubar=no,toolbar=no, status=no,scrollbars=yes')
</script>

# js'关闭窗口
- window。close（）;
- <窗口对象>.close();
>(script type="text/javascript">
   var mywin=window.open('http://www.imooc.com'); //将新打的窗口对象，存储在变量mywin中
   mywin.close();
</script>

# 通过ID获取元素
- document.getElementById(“id”) 

> 获取的元素是一个对象，如想对元素进行操作，我们要通过它的属性或方法。

# innerHTML 属性
- Object.innerHTML 
> 1.Object是获取的元素对象，如通过document.getElementById("ID")获取的元素。

> 2.注意书写，innerHTML区分大小写。

# 改变html样式
- Object.style.property=new style;
> Object是获取的元素对象，如通过document.getElementById("id")获取的元素。


- p id="pcon">Hello World!</p>
script>
   var mychar = document.getElementById("pcon");
   mychar.style.color="red";
   mychar.style.fontSize="20";
   mychar.style.backgroundColor ="blue";
</script>

# 显示与隐藏
- Object.style.display = value
> :Object是获取的元素对象，如通过document.getElementById("id")获取的元素。


1.隐藏：mychar.style.display="none";

2.显示: mychar.style.display="block";

# 控制类名
- object.className = classname
- 1.获取元素的class 属性
- 2. 为网页内的某个元素指定一个css样式来更改该元素的外观

# 语句 
- break	用于跳出循环。
- catch	语句块，在 try 语句块执行出错时执行 catch 语句块。
- continue	跳过循环中的一个迭代。
- do ... while	执行一个语句块，在条件语句为 true 时继续执行该语句块。
- for	在条件语句为 true 时，可以将代码块执行指定的次数。
- for ... in	用于遍历数组或者对象的属性（对数组或者对象的属性进行循环操作）。
- function	定义一个函数
- if ... else	用于基于不同的条件来执行不同的动作。
- return	退出函数
- switch	用于基于不同的条件来执行不同的动作。
- throw	抛出（生成）错误 。
- try	实现错误处理，与 catch 一同使用。
- var	声明一个变量。
- while	当条件语句为 true 时，执行语句块。

#变量转换
- var iNum1=10;
- alert(iNum1.toString());可以吧10变成字符串“10”
- alert（Number（sNum1））；内容变成数字
- alert（parsiInt（sNum1））内容变整数
- alert （parseFloat（sNUM1)内容变小数

# 条件判断
    if（INum1>iNum2){
    iNum3 = iNum1;
    }else{
    iNum3 = iNum2;
    }
    一样的意思iNum = iNum1>iNum2?iNum1:iNum2;
    } 

# 等于逻辑运算符
- &&与运算
- ||或运算
- ！||非运算

# 循环
    iSum+=i；===》就是当前的iSum=上一次的iSum+当前的i

