# vue.js
- 必需在head里面引入
- 在script创建new vue({
     el:"#root",
     data:{数据
       content：“输出内容”
      }，
     methods：{
        handleClick：function（）{
     alert(123) 
      }

# vue.js缩写

- v-bind=：
- v-on=@
- data 用于定义属性，实例中有三个属性分别为：site、url、alexa。
- methods 用于定义的函数，可以通过 return 来返回函数值。
- {{ }} 用于输出对象属性和函数返回值 


#侦听器
- 监听count
- data：{count：0}，
- watch：{firstName：function（）{
- this.count ++},

# 计算属性
- computed=methods

# 指令
- v-if  v-show 点击隐藏
- v-for循环li标签

# todolist
 	 Vue.component('todo-item',{
	template:'<li>item</it>'
 	 })

# 样式绑定
    <style>
	.active {
	width: 100px;
	height: 100px;
	background: green;
	}
	</style>
	</head>
	<body>
	<div id="app">
	  <div v-bind:class="{ active: isActive }"></div>
	</div>

	<script>
	new Vue({
	  el: '#app',
 	 	data: {
    isActive: true
 	 	}
	})
	</script>

# 命令行工具（cli）
- npm install --global vue-cli
> 全局安装vue-cli

- vue init webpack my-project
> 创建一个基于webpack模板的新项目 安装依赖

- cd my-project
- npm run serve 
- vue-cli3运行命令
- npm run dev
- 创建新项目
- vue create 项目名
- 全局扩展
- npm install -g @vue/cli-service-global
- 在现有项目里安装插件
- vue add @vue/插件名
- @vue/cli：全局安装的，暴露 vue create <app> 命令；
- @vue/cli-service：局部安装，暴露 vue-cli-service 命令。






