# Bootstrap排版表格

           <table class=""></table>
- .table 基础表格效果
- .table-striped  斑马线效果
- .table-bordered  边框效果
- .table-hover  高亮效果（鼠标经过的变色效果）
- 为了让bootstrap对移动设备友好在head添加

	      <meta name="viewport" content="width=device-width, initial-scale=1.0">
- maximum-scale=1.0 与 user-scalable=no 一起使用。这样禁用缩放功能后，用户只能滚动屏幕，

# html强调标签
    <small>（设置文本为父文本大小的 85%）  <strong>（设置文本为更粗的文本）<em>（设置文本为斜体）
- text-muted：提示，使用浅灰色
- text-primary：主要，使用蓝色
- text-success：成功，使用浅绿色
- text-info：通知信息，使用浅蓝色
- text-warning：警告，使用黄色
- text-danger：危险，使用褐色
- bootstrap中text-left：左对齐，text-center：居中对齐，text-right：右对齐,text-justify：两端对齐。

# 表格
- table：基础表格
- table-striped：斑马线表格
- table-bordered：带边框的表格
- .table-hover：鼠标悬停高亮的表格
- .table-condensed：紧凑型表格
- .table-responsive：响应式表格
- 在<table class="table">的基础上增加类名“.table-striped”变成有条纹表格
- 添加一个“.table-bordered“边框表格
- 添加类名“table-hover”鼠标悬浮表格
- 类名“table-condensed紧凑表格
- 设置类名“table-responsive”响应式表格

# 表单
- 复选框（Checkbox）和单选框（Radio）
- 在一个水平表单内的表单标签后放置纯文本时，在 <p> 上使用 class .form-control-static
- 使用 class .input-lg 和 .col-lg-* 来设置表单的高度和宽度
- 以 label input 标签为一组外部box类名 .from-group 内部表单标签类名 .from-control
- 表单嵌入输入控件 .input-group
- 整个表单水平排列(内联排列)： 给from 添加类名 .from-inline
- 表单水平排列： from标签添加类名 .from-horizontal并且 label和input 标签分别使用栅格 比如.col-sm-2 .col-sm-10然后给label标签添加类名.control-label 使其靠近输入框
- .form-control-static 使label标签旁边的文本对齐
- 加入图标： .has-feedback一组表单外部Box input后面添加 span 标签 添
- 类名 form-control-feedback 添加图标类名glyphicon glyphicon-ok
- 表单描述 .help-block 比如p标签


# js插件
- 点击按钮属性： data-toggle='modal'
- 点击按钮选择显示那个弹框属性： data-target='弹框id'
- 弹框类名： modal fade

# 按钮
- 类名 .btn
- 样式： .btn-default .btn-success 等
- 大小： .btn-lg .btn-sm .btn-xs
- .btn-block 变为块级元素
- 属性： 禁止点击 disabled
- 那些标签都可以做按钮： （鼠标可以点击的） a input button
- 按钮组： .btn-group (外部box) (内部按钮必须有.btn) .btn-group-vertical 垂直按钮组
- 按钮工具框： .btn-toolbar （内部包含按钮组.btn-group）
按钮组嵌入下拉菜单：

# 图片
- 形状： 类名 .img-rounded 圆角 .img-circle 圆 .img-thumbnail 边框（背景透明的显示不出来）
- 响应式图片 .img-responsive
- 清除浮动.clearfix

# 下拉菜单
- 外部box类名 .dropdown 向上.dropup
- 按钮属性 data-toggle='dropdown'
- 下拉列表类名 .dropdown-menu
- 下拉列表位置类名 .dropdown-menu-right
- 列表标题 .dropdown-header
- 列表分割线 .divider
- 禁用菜单项 .disabled

# 导航
- 面包屑导航 ol li ol 标签类名 .breadcrumb
- 分页导航 ul li ul 标签类名 .pagination 激活状态 li .active 禁用 .disabled 