### 盒子模型
    盒子模型包括四部分：
            margin 边距
            border 边框
            padding 填充
            content 实际内容
        总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距
        总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距
        
### 盒子模型-边框
    边框的粗细 border-width: 20px;
    边框样式实线 border-style: solid;
    边框样式虚线 border-style: dashed;
    边框样式点线 border-style: dotted;
    
    边框复合写法 border: 1px solid red;
    
    合并相邻边框 border-collapse:coolapse;
    
### 盒子模型-填充
    padding-top padding-bottom padding-left padding-right
    填充复合属性：
        padding:1px;  上下左右1px
        padding:5px 10px;  上下5px 左右10px
        padding:5px 10px 20px;  上5px 左右10px 下20px
        padding:5px 10px 15px 20px; 上右下左（顺时针）