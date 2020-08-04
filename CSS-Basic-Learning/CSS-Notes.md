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
    
### 行高继承
    行高和盒子高度一样，文字垂直居中
    
        
### 盒子模型-边框
    边框的粗细 border-width: 20px;
    边框样式实线 border-style: solid;
    边框样式虚线 border-style: dashed;
    边框样式点线 border-style: dotted;
    
    边框复合写法 border: 1px solid red;
    
    合并相邻边框 border-collapse:coolapse;
    
    圆角边框 border-radius: height / 2(圆角矩形可以设置高度一般，圆形直接设置50%);
    
### 盒子模型-填充
    padding-top padding-bottom padding-left padding-right
    填充复合属性：
        padding:1px;  上下左右1px
        padding:5px 10px;  上下5px 左右10px
        padding:5px 10px 20px;  上5px 左右10px 下20px
        padding:5px 10px 15px 20px; 上右下左（顺时针）
        
### 盒子模型-边距
    控制盒子与盒子之间的距离
    块级盒子水平居中对齐： margin: 0 auto; // 上下外边距0 左右auto
    
### 浮动应用
    浮动最典型应用：可以让多个块级元素一行内排列显示
    网页排列布局：
        多个块元素纵向排列用标准流，多个块元素横向排列用浮动来完成
    
### 浮动
    float属性用于创建浮动，将其移动到一边，直到左边缘和右边缘触及包含块或另一个浮动的边缘
    语法： 选择器 {float: 属性值;}
    
### 浮动特性【重要】
    1.浮动元素会脱离标准流【脱标】，浮动的盒子不再保留原先的位置【重要特性：浮动后不保留占据位置】
    2.多个浮动元素会一行内显示并且顶端对齐排列
    3.浮动元素会具有行内块元素的特性

### 网页布局一般策略
    先用标准流的父元素排列上下位置，之后内部自元素采取浮动排列左右位置
    
### 浮动注意点
    1.浮动元素基本上都是要用父元素来进行约束，即先用标准流的父元素排列上下位置秒之后内部子元素用浮动
    2.一个元素浮动了，其余所有的兄弟元素也都是要浮动
    3.浮动盒子只会影响浮动盒子后面的标准流，不会影响前面的标准流
    
### 清除浮动
    原因：有时父盒子不方便给高度，但子盒子浮动又不占有位置，最后父盒子高度为0，影响下面的标准流
    策略：清除浮动的策略是：闭合浮动，清除浮动影响
    语法：
        选择器{clear:属性值;}
        clear:both 同时清除两侧浮动影响【用的比较多】
        
### 清除浮动方法
    1.overflow属性：给父亲元素添加代码属性
        overflow: hdiien;
    2.after伪元素法：给父亲元素代码添加clearfix类属性
        .clearfix:after {
            content:"";
            display:block;
            height:0;
            clear:both;
            visibility:hidden;
        }
        .clearfix {
            *zoom: 1;
        }
    3.双伪元素清除浮动
    