### WebAPI
    Web API 主要用于浏览器交互效果，很多时候都是方法（函数）
    Web API 是浏览器提供的一套操作浏览器功能和页面元素的API（BOM DOM）

### DOM简介
    文档对象模型
    通过DOM接口可以改变网页的内容、结构、样式
    DOM树：
        文档：一个页面就是一个文档，document来表示
        元素：页面中所有的标签都是元素，element来表示
        节点：页面中所有的内容都是节点（标签属性文本注释），node来表示
    
### 获取元素
    1.根据ID获取
        getElementById('id') // id是字符串类型，返回一个元素对象
    2.根据标签名获取
        // 其中element是【某个】父元素可省略，返回的是带有指定标签名的对象集合,以伪数组的形式存储
        // Note：父元素必须是单个对象（必须指明是哪一个元素对象）
        (element).getElementsByTagName('标签') 
    3.通过HTML5新增方法获取
        getElementByClassName('类名') // 根据类名返回元素对象集合
        querySelector('选择器') // 根据指定选择器返回第一个元素对象 【选择器一定要带符号 .box #nav】
        querySelectorAll('选择器') // 返回指定选择器的所有元素对象集合
    4.特殊元素获取
        获取body元素
            document.body // 返回body元素对象
        获取html元素
            document.documentElement // 返回html元素对象
            
### 事件基础
    事件是JS检测到的行为，即：触发---响应机制
    1.事件三要素：
        事件源：
            事件被触发的对象，谁触发了事件
        事件类型：
            如何触发事件，比如：
            鼠标点击onclick，鼠标经过onmouseover，键盘按下
        事件处理程序：
            通过一个函数赋值的方式完成