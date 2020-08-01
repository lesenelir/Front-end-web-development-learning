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
    background-repeat:no-repeat; 不平铺
    background-position 改变图像在背景中的位置
    
### 盒子模型
    盒子模型包括四部分：
        margin 边距
        border 边框
        padding 填充
        content 实际内容
    总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距
    总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距
    
    