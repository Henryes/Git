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

# 条件渲染
- v-if 是一个指令用于条件性地渲染一块内容，这块内容只会在指令的表达式返回 truthy 值的时候被渲染
- 切换多个元素有<template>
- v-else必须在v-if后面 不然不能识别
- v-else-if 可以连续使用
- loginType不会清除输入内容
- v-show切换元素的css属性display
- v-show不支持template 和v-else
- v-if是真条件渲染，只有条件第一次为真才渲染
- 频繁切换使用v-show好 反之v-if好


# 列表渲染
- v-for是一个数组渲染一个列表，需使用item in item语法，item是被迭代的数组别名，也可以用of间隔
- v-for可以访问所有父作用域属性
- 为了跟踪每个节点 要为每项给一个key，才能排序现有元素
- 变异方法打开控制台，然后对前面例子的 items 数组尝试调用变异方法
  		
	    example1.items.push({ message: 'Baz' })
- 注意事项  由于 JavaScript 的限制，Vue 不能检测以下数组的变动：
当你利用索引直接设置一个数组项时

		vm.items[indexOfItem] = newValue
当你修改数组的长度时，

		vm.items.length = newLength
- vm.$set  vm.items.splice方法也可以响应
- 显示过滤或排序的结果
			
		<li v-for="n in even(numbers)">{{ n }}</li>

- v-for比v-if优先级更高
- 在template使用v-for可以循环一段包含多个元素的内容
- 


# 事件处理
- v-on监听dom事件
- 内联处理器方法除了绑定亦可以在JavaScript中调用方法
- 访问原始dom事件可以使用特殊变量 $event
- 事件修饰符
     	.stop  
    	.prevent
   		.capture
		.self
		.once
        .passive
- 使用修饰符时，顺序很重要；相应的代码会以同样的顺序产生，用 v-on:click.prevent.self 会阻止所有的点击，
- 而 v-on:click.self.prevent 只会阻止对元素自身的点击
-  点击事件将只会触发一次 
<a v-on:click.once="doThis"></a>
- 按键修饰符
- 只有在 `key` 是 `Enter` 时调用 `vm.submit()` 
  <input v-on:keyup.enter="submit">
- keyCode 特性也是允许
- .exact 修饰符
- 鼠标按钮修饰符
   			.left
			.right
			.middle

# 组件基础
- 组件可以重复使用，每使用都会有新的实例被创建
- 一个组件的data必须是一个函数，不然会影响其他实例
- prop可以给博文组件传递一个标题，一个组件默认可以拥有任意数量的 prop，任何值都可以传递给任何 prop
- 构建一个 <blog-post> 组件不可能只有一个标题，每个组件必须只有一个根元素
		<div class="blog-post">
  			<h3>{{ title }}</h3>
  			<div v-html="content"></div>
		</div>
- 监听子组件 postFontSize可以控制博文的字号
- v-model自定义输入组件，这个组件input将其 value 特性绑定到一个名叫 value 的 prop 上在其 input 事件被触发时，将新的值通过自定义的 input 事件抛出
- 动态组件可以在<component> 元素加一个特殊的 is 特性来实现

# 组件注册
- 全局注册Vue.component('my-component'.
- 局部注册

        var Child = {
 		 template: '<div>A custom component!</div>'
		}
		new Vue({
 		  // ...
 		  components: {
  		   // <my-component> 将只在父模板可用
 	      'my-component': Child
 		  }
		})

# props
- prop 是父组件用来传递数据的一个自定义属性。子组件需要显式地用 props 选项 声明 “prop”
- v-bind动态绑定到父组件，父组件的变化可以传到子组件
- props传递的是字符串，不能数字，需要v-bind才可以
- 改变prop 1义一个概念局部 data 属性，将 prop 的初始值作为局部数据的初始值

			props: ['initialCounter'],
		data: function () {
  		return { counter: this.initialCounter }
		}
- 2定义一个 computed 属性，此属性从 prop 的值计算得出

 		props: ['size'],
		computed: {
  		normalizedSize: function () {
 	    return this.size.trim().toLowerCase()
 	    }
	    }
- 如果子组件传回父组件，使用v-on自定义事件
- 给组件绑定原生事件使用 .native 修饰 v-on
- 自定义事件也可以用来创建自定义的表单输入组件，使用 v-model 来进行数据双向绑定
- 要让组件的 v-model 生效，它必须：
	1·接受一个 value 属性
	2·在有新的 value 时触发 input 事件

# slots
- 父组件模板的内容在父组件作用域内编译；子组件模板的内容在子组件作用域内编译
-  多个组件可以使使用同样一个挂载点，动态的切换他们


		var vm = new Vue({
  		el: '#example',
  		data: {
  		  currentView: 'home'
  		},
  		components: {
   		 home: { /* ... */ },
   		 posts: { /* ... */ },
    	archive: { /* ... */ }
  		}
		})
		<component v-bind:is="currentView">
 		 <!-- 组件在 vm.currentview 变化时改变！ -->
		</component>
-  keep-alive可以把切换出去的组件保留在内存中，可以保留它的状态或避免重新渲染


# 杂项
- Props 允许外部环境传递数据给组件
Events 允许组件触发外部环境的副作用
Slots 允许外部环境将额外的内容组合在组件中
- 异步组件 Vue.js 允许将组件定义为一个工厂函数，动态地解析组件的定义 Vue.js 只在组件需要渲染时触发工厂函数，并且把结果缓存起来，用于后面的再次渲染  工厂函数接收一个 resolve 回调，在收到从服务器下载的组件定义时调用。也可以调用 reject(reason) 指示加载失败
- 子组件有 inline-template 特性，组件将把它的内容当作它的模板，而不是把它当作分发内容
- 定义模版的方式是在 JavaScript 标签里使用 text/x-template 类型
- 当组件中包含大量静态内容时，可以考虑使用 v-once 将渲染结果缓存起来

	    Vue.component('terms-of-service', {
  		template: '\
  		  <div v-once>\
  	    <h1>Terms of Service</h1>\
  	    ... a lot of static content ...\
 		   </div>\
 			 '
		})

# 响应式原理
- 用户看不到 getter/setters，但是在内部它们让 Vue 追踪依赖，在属性被访问和修改时通知变化
- Vue 不允许在已经创建的实例上动态添加新的根级响应式属性（root-level reactive properties）。然而它可以使用 Vue.set(object, key, value) 方法将响应属性添加到嵌套的对象上

		Vue.set(vm.someObject, 'b', 2)
- 还可以使用 vm.$set 实例方法，这也是全局 Vue.set

		this.$set(this.someObject,'b',2)

- Vue 不允许动态添加根级响应式属性，所以你必须在初始化实例前声明根级响应式属性，哪怕只是一个空值
- 如果你不在 data 对象中声明 message，Vue 将发出警告表明你的渲染方法正试图访问一个不存在的属性

# 过度效果
- 元素封装成过渡组件之后，在遇到插入或删除时，Vue 将
自动嗅探目标元素是否有 CSS 过渡或动画，并在合适时添加/删除 CSS 类名
如果过渡组件设置了过渡的 JavaScript 钩子函数，会在相应的阶段调用钩子函数。
如果没有找到 JavaScript 钩子并且也没有检测到 CSS 过渡/动画，DOM 操作（插入/删除）在下一帧中立即执行。(注意：此指浏览器逐帧动画机制，与 Vue，和Vue的 nextTick 概念不同

-  过渡的-css-类名
-  1  v-enter: 定义进入过渡的开始状态。在元素被插入时生效，在下一个帧移除。
-  2 v-enter-active: 定义进入过渡的结束状态。在元素被插入时生效，在 transition/animation 完成之后移除。
-  3 v-leave: 定义离开过渡的开始状态。在离开过渡被触发时生效，在下一个帧移除。
-   4 v-leave-active: 定义离开过渡的结束状态。在离开过渡被触发时生效，在 transition/animation 完成之后移除。
-  CSS 动画用法同 CSS 过渡，区别是在动画中 v-enter 类名在节点插入 DOM 后不会立即删除，而是在 animationend 事件触发时删除
-  当需要设置两种过渡效果比如 animation 很快的被触发并完成了，而 transition 效果还没结束。在这种情况中，你就需要使用 type 特性并设置 animation 或 transition 来明确声明你需要 Vue 监听的类型
-  注意：当只用 JavaScript 过渡的时候， 在 enter 和 leave 中，回调函数 done 是必须的 。 否则，它们会被同步调用，过渡会立即完成
-  推荐对于仅使用 JavaScript 过渡的元素添加 v-bind:css="false"，Vue 会跳过 CSS 的检测
-  注意：当有相同标签名的元素切换时，需要通过 key 特性设置唯一的值来标记以让 Vue 区分它们，否则 Vue 为了效率只会替换相同标签内部的内容。即使在技术上没有必要，给在 <transition> 组件中的多个元素设置 key 是一个更好的实践
-  列表的位移过渡<transition-group> 组件不仅可以进入和离开动画，还可以改变定位
-  可复用过渡组件<transition> 或者 <transition-group> 作为根组件，然后将任何子组件放置在其中
-  所有的过渡特性都是动态绑定。，通过事件的钩子函数方法，可以在获取到相应上下文数据。可以根据组件的状态通过 JavaScript 过渡设置不同的过渡效果。