## HTML笔记

### 属性
    HTML 元素可以设置属性
    属性可以在元素中添加附加信息
    属性一般描述于开始标签

### 段落空格
    HTML中所有连续的空格或空行都会被算作一个空格
    
### id属性
    id属性可用于创建一个HTML文档书签标记
    id属性起到标示作用
    a属性可以结合id属性来使用
    
### link元素
    <link> 标签定义了文档与外部资源之间的关系
    <link rel="stylesheet" type="text/css" href="mystyle.css">

### img元素
    <img>是空标签，只包含属性，没有闭合标签
    语法: <img src="url" alt="some_text">
    alt属性是一段预备替换的文本：即当浏览器无法载入图像时，会输出alt中的内容
    
### table元素
    表格从table标签开始
    表格行从tr标签开始
    表格列从td标签开始
    表头标签从th标签开始（表头代表加粗）
    
### 列表元素
    无序列表<ul>
    有序列表<ol>
    列表项<li>
    
### 区块元素
    <div>是块级元素，定义文档区域
    <span>是内联元素，用来组合文档中的行内元素

### 布局
    通常用<div>标签进行布局，用利于css对元素进行定位
    用<div>标签的时候，建议定义id属性来识别不同的div
    
### form表单
    <input type="text" > 文本
    <input type="password" > 密码
    <input type="radio" > 单选按钮
    <input type="checkbox"> 复选按钮
    <input type="submit"> 提交按钮
    
### HTML快捷键
    div*5 快速生成五个div
    有父子级关系的标签可以用>来实现: ul>li
    带有类名的标签：.demo
    带有id关系的标签: #demo
    div类名有顺序的，可以用自增符号$ : .demo$*5
    标签内部想要有内容，可以用{}符号：div{hello}
    
  
  

    
    
    