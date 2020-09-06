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
            鼠标点击onclick，键盘按下
            失去焦点onblur，获取焦点onfocus
            鼠标经过onmouseover，鼠标离开onmouseout
        事件处理程序：
            通过一个函数赋值的方式完成

### 操作元素
    1.修改元素内容
        element.innerText 从起始位置到终止位置内容，不识别html标签，同时空格和换行也会去掉    
        element.innerHTML 从起始位置到终止位置全部内容，识别html标签，同时保留空格和换行
    2.修改元素属性
        元素.属性 
        src href title alt元素属性
    3.修改表单属性
        type 表单类型
        value 修改表单内容
        element.disable = true 禁用按钮
    4.修改元素样式属性
        element.style  行内样式操作
        element.className  类名样式操作 (直接更改元素的类名，会覆盖原先的类名)  
    5.自定义属性操作
        获取属性值:
            element.属性
            element.getAttribute('属性') //通常用于获得自定义属性值
        设置属性值：
            element.属性 = '值'
            element.setAttribute('属性', '值') //通常用于自定义属性
        案例：tab切换      
        H5自定义属性新规范：
            data- 开头的属性是自定义属性       
    
### 节点操作
    页面所有内容都是节点（标签、属性、文本、注释），DOM中节点使用node来表示
    1.节点属性：
        nodeType 节点类型
            元素节点 nodeType 为 1 【主要】
            属性节点 nodeType 为 2
            文本节点 nodeType 为 3
        nodeName 节点名称
        nodeValue 节点值
    2.节点层级：通过节点层级关系获取元素【常用】
        父级节点 parentNode
        子元素节点 parentNode.children【伪数组】
        第一个子元素结点 parentNode.firstElementChild | parentNode.children[0]
        最后一个子元素结点 parentNode.lastElementChild | parentNode.children[parent.children.length-1]
        下一个兄弟元素节点 node.nextElementSibling
        上一个兄弟元素节点 node.previousElementSibling     
    3.CRUD节点：
        动态创建节点：
            document.createElement('tagName')
        添加节点：
            node.appendChild(child) 将一个节点添加到指定父节点的子节点列列表末尾 node是父级 child是子级
            node.insertBefore(child, 指定元素) 将一个节点添加到父节点的指定子节点前面        
        删除节点：
            node.removeChild(child) 删除一个子节点并返回子节点
        复制节点：
            node.cloneNode() 浅拷贝：只复制标签不复制标签里的内容
            node.cloneNode(true) 深拷贝：复制标签并复制里面的内容
 
### 注册事件
    注册事件两种方法：
        1.利用on开头的事件 (特点：注册事件唯一性)
        2.方法监听注册方式 addEventListener() 它是一个方法 (同一元素同一事件可以注册多个监听器)
            eventTarget.addEventListener('type', listener[, useCapture])
            将指定的监听器注册到eventTarget(目标对象)上 
            type 事件类型，click mouseover 不用带on
            listener 事件处理函数，事件发生时，会调用该监听函数
            useCapture 可选参数，是一个布尔值，默认值是false（冒泡阶段）， true（捕获阶段）
            
### 删除事件
    1.传统方法
        在方法调用末尾添加 onclick = null
    2.方法监听方式
        eventTarget.removeEventListener('type', listener[, useCapture])
        eventTarget.datachEvent(eventNameWithOn, callback)
        
### DOM事件流
    概述：事件发生会在元素节点之间按照特定的顺序传播，这个传播过程即DOM事件流
    DOM事件流分为三个阶段：
        捕获阶段（从上到下）
        当前目标阶段
        冒泡阶段（从下到上）
           
### 事件对象
    事件对象属性方法
    e.target 返回触发事件的对象 【常用】
    e.srcElement 返回触发事件的对象
    e.type 返回事件的类型
    e.cancelBubble 阻止冒泡
    e.stopPropagation() 阻止冒泡【常用】
    e.returnValue 阻止默认事件
    e.preventDefault() 阻止默认事件【常用】
    