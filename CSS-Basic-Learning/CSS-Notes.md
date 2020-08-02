### CSS简介
    内容表现分离，外部样式表可以提高效率
    把外部样式表存储在CSS文件中
    
### CSS语法
    选择器{属性:值;属性:值;}
    eg h1{color:blue;font-size:12px;}
    
### id与class选择器
    HTML中以id属性来设置选择器，CSS中id选择器以"#"定义
    HTML中以classs属性来设置选择器，CSS中class选择器以"."定义
    
### 样式表三种方式
    外部样式表：.css文件，不能有任何html标签
        <link rel="stylesheet" type="text/css" href="mystyle.css">
    内部样式表：head标签嵌套style标签
    内联样式
    
    多重样式优先级：内联样式 > 内部样式 > 外部样式
    
### 背景
    背景图片: background-img: url("static/pic/i.jpg");
    背景不平铺: background-repeat:no-repeat; 不平铺
    背景中图像的位置: background-position: x y; （x为水平值，y为垂直值）
        background-position也可以跟方位名词 center top left right
    背景图像固定或滚动：background-attachment: scroll | fixed
        fixed: 背景图像固定; scroll: 背景图像随内容滚动
    【注意】：背景复合写法：
        background: 背景颜色 背景图片地址 背景平铺 背景图像滚动 背景图片位置
    
### 后代选择器
    后代选择器称为包含选择器，可以选择父元素里的子元素
    语法： 元素1 元素2 {样式声明}
    eg: 选择ol中的li标签 ol li {}
    
### 并集选择器
    可以选择多组标签，通常用于集体声明
    语法：元素1， 元素2 {样式声明}
    
### 子元素选择器
    只能选择作为某元素的最近一级子元素，亲儿子选择器
    语法： 元素1> 元素2 {样式声明}
    
### 伪类选择器
    伪类选择器用于向某些选择器添加特殊效果，如，给链接添加特殊效果
    语法：伪类选择器用冒号来实现，如，:hover :first-child
    a:link 选择所有未被访问过的链接
    a:visited 选择一被访问过的链接
    a:hover 选择鼠标表指针位于其上的链接
    a:active 选择鼠标按下未弹起的链接 
    
### 块元素
    <h1>~<h6> <p> <div> <ul> <ol> <li>
    特点：
        独占一行
        高度 宽度 外边距 内边距都可以控制
        宽度默认是容器的100%
        是一个容器及盒子，里面可以放行内或者块级元素
        
### 行内元素
    <a> <span> <del> <b> ... 等
    特点：
        行内元素可以一行显示多个元素
        宽 高 直接设置是无效的
        默认宽度就是本身内容的宽度
        行内元素只能容纳文本或其他行内元素
        
 ### 元素转换
    块元素转换成行内元素 display:inline;
    行内元素转换成块元素 display:block;
    
### CSS三大特性
    层叠性：相同选择器设置相同样式，主要解决样式冲突的问题
        层叠性原则：样式冲突遵循"就近原则"，离哪个样式近，就执行哪个样式
    继承性：子标签会继承父标签的某些样式
    优先级
          
### 盒子模型
    盒子模型包括四部分：
        margin 边距
        border 边框
        padding 填充
        content 实际内容
    总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距
    总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距