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
    prompt - 浏览器弹出输入框，用户可以输入；【prompt传过来的都是字符型，有时要用数字型要进行parseInt转换】
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
        str.length（数组长度: arr.length）
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
        parseInt(string)函数 【prompt传过来是字符型用parseInt进行转换】
        parseFloat(string)函数【prompt传过来是字符型用parseFloat进行转换】
        
### JS运算符
    比较运算符：
        18 == '18' //true (==运算符会默认转换数据类型)
        18 === '18' //false (===运算符是全等运算符，会比较数据类型) 
        Note：
            = 赋值；
            == 判断，判断数值是否相等；
            === 全等，判断数值和数据类型是否相等；
    逻辑运算符：
        1. 逻辑中断逻辑与：
            表达式1 && 表达式2；逻辑与短路运算，如果表达式1为真则返回表达式2，如果表达式1为假则返回表达式1
            123 && 456  // 456
            0 && 456  // 0
        2. 逻辑中断逻辑或
            表达式1 && 表达式2；逻辑或短路运算，如果表达式1为真则返回表达式1，如果表达式1为假则返回表达式2
            123 || 456 || 789  // 123
            0 || 456 // 456
    三元运算符：
        语法结构: 条件表达式 ? 表达式1 : 表达式2;
        
### JS数组
    创建数组两种方式:
        1. new关键字创建数组
            var 数组名 = new Array();
        2. 数组字面量创建数组【常用】
            var 数组名 = [];
            eg: var arr = [1, 2.5, 'lesenelir', true];
            JS中的数组可以存放任意数据类型的数据
    数组长度：
        arr.length  
        
### JS函数
    声明函数两种方式：
        1. 命名函数：
            function 函数名() {函数体}
        2. 函数表达式（匿名函数）：
            var 变量名 = function() {函数体}
            eg: var fn = function() {函数体} // fn是变量名，不是函数名。
    形参实参：
        形参是在声明函数的小括号内，实参是在函数调用的小括号内。
        实参个数小于形参个数，多的形参会定义为undefined，结果为NaN
    return：
        return终止函数
        return只会返回一个结果
        函数如果没有return则返回undefined
    arguments:
        如果不知道要传入多少个参数，可以用arguments来获取。
        arguments是当前函数的一个内置对象，arguments对象中存储了要传递的所有参数
                   
### JS作用域
     全局变量：
        定义在<script>标签内的变量
        【注意】：在函数内部没有声明直接赋值的变量也称为全局变量
        eg: function fn() {
            var num = 10 // 局部变量
            num2 = 20 // 全局变量
        }
     局部变量：定义在函数内的变量 
     块级作用域：if\for{}内部定义的变量称为块级作用域，可以在{}外部使用
     
### JS预解析
     JS解释器运行JS分为两部：
        1.预解析：JS解释器会把js里所有var还有function提升到当前作用域最前面
        2.代码执行：按照代码书写顺序从上到下执行
        
### JS对象 
    创建对象的三种方式：
        1.利用字面量创建对象{}
            里面的属性采用键值对的方式；
            多个属性用逗号分割，最后一个属性不用逗号；
            方法冒号后面跟的是一个匿名函数
            eg:var obj = {
                uname: 'lesenelir',
                age: 18,
                sayHi: function () {
                    console.log('hi~')
                }
            }
        2.利用new Object创建对象
            利用等号=赋值的方法 添加对象的属性和方法
            var obj = new Object()
                obj.uname = 'lesenelir'
                obj.age = 18
                obj.sayHello = function () {
                    console.log('hello~')
            }
        3.利用构造函数创建对象  
            构造函数创建对象，一次可以创建多个对象
            构造函数里面封装的不是普通代码，而是对象。即，把对象的一些相同的属性和方法抽象出来封装到函数里面
            语法：
                function 构造函数名() {
                    this.属性 = 值
                    this.方法 = function () {}
                }
            使用:
                new 构造函数名()
            注意：
                构造函数名首字母大写
                构造函数不需要return就可以返回结果
                只要调用了构造函数          
    使用对象：
        调用对象的属性：对象名.属性名 | 对象名['属性名']
        调用对象的方法：对象名.方法名()      
    遍历对象：
        for (变量 in 对象) {}   

        