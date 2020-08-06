### JS作用
    表单动态校验
    网页特效
    服务端开发
    桌面程序
    App
    游戏开发
    
### JS组成
    ECMAScript 基本语法
    DOM 页面文档对象模型-对页面上的各种元素进行操作
    BOM 浏览器对象模型-操作浏览器窗口
    
### JS引入
    行内式 - JS中推荐用单引号
    内嵌式 - 类似于CSS<style>标签
    外部式 - <script src="01-my.js"></script> 外部引用时，script标签中不能写代码
    
### JS输入输出
    prompt - 浏览器弹出输入框，用户可以输入
    connsole.log() - 浏览器控制台打印输出信息
    alert() - 浏览器弹出警示框
    
### JS变量
    语法： var 变量名 
    
### JS数据类型
    JS的变量数据类型是只有程序在运行过程中，根据等号右边的值来判断的
    JS是动态类型，变量的数据类型是可以变化的：
        var x = 10; 
        x = 'lesenelir';
    JS数据类型分为两大类：
        简单数据类型：Number String Boolean Undefined Null
        复杂数据类型：object

### JS-String类型
    字符串引号嵌套：外双内单引号，或者，外单内双引号
    字符串转义符：
        \\    斜杠\
        \'    单引号'
        \"    双引号"
        \t    tab缩进
        \n    换行
    字符串长度：
        str.length
    字符串的拼接：
        多个字符串用+来拼接：字符串 + 任何类型 = 拼接之后的字符串

### JS获取数据类型
    typeof 变量名字 
    var a = undefined; console.log(typeof a); // undefined
    var b = null; console.log(typeof b); // object
    
### JS数据类型转换
    1. 转换成字符串：
        变量.toString()
        String(变量)
        加号拼接字符串：常用
    2. 转换成数字型：
        parseInt(string)函数
        parseFloat(string)函数
       