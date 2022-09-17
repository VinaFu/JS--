# JS--

Part One: The JavaScript language (1/14)
Part Two: Browser: Document, Events, Interfaces (6)
Part Three: Additional articles (7)
每天看一小时 + 笔记一小时。看九月底能看多少。

Part One: The JavaScript language (14)

1. An introduction

    1.1 introduction：
        1）不会对CPU进行read，write，copy，execute，主要对browser； node.js允许它访问
        2）与html，css集成
        
    1.2 manuals： MDN
    
    1.3 code editor： IDE：Integrated Development Environment
        常见的有：Visual Studio Code， WebStorm 轻便的有：
Sublime Text， Notepad++ (Windows).

    1.4 developer console：can be opened with F12 for most browsers on Windows. Chrome for Mac needs Cmd+Opt+J, Safari: Cmd+Opt+C (need to enable first).

2. JavaScript Fundamentals

    2.1 Hello, world!  <script> tag
       1）自动插入html任何位置
       2）可接入外部资源 <script src="/js/script1.js"></script>
       3）如果设置了 src 特性，script 标签内容将会被忽略。
            <script src="file.js">
              alert(1); // 此内容会被忽略，因为设定了 src
            </script>

    2.2 Code structure
        1）semicolon：语句分开，有时候自动隐去
        2）comments： 单行：// ；多行：/*  */-没法连用
            在大多数的编辑器中，一行代码可以使用 Ctrl+/ 快捷键进行单行注释，诸如 Ctrl+Shift+/ 的快捷键可以进行多行注释（选择代码，然后按下快捷键）。对于 Mac 电脑，应使用 Cmd 而不是 Ctrl，使用 Option 而不是 Shift。
    
    2.3 The modern mode, "use strict" 出现在顶端
    
        为了避免一些情况，使用use strict可以更加规范，例如分号不要省略。
    
    2.4 Variables 变量 和 常数
    
        variables
        1）一般用let（var太老了）
             let message;
             message = 'Hello'; // 将字符串 'Hello' 保存在名为 message 的变量中
        2）多行变量用逗号，分号隔开，一行一个 好看
        3）一个变量只能declared 一次
        let message = "This";// 重复 'let' 会导致 error
        let message = "That"; // SyntaxError: 'message' has already been declared
        4）命名：变量名称必须仅包含字母、数字、符号 $ 和 _。且首字符必须非数字。不建议使用非英文字母。❕❕保留字列：let、class、return、function都用于编程本身，不能命名。
        
        constant - 定义常数，顾名思义不变的
        1）定义之后不可改，要改的话就会报错
        2）大写命名基本定住了，属于常数；变量不可大写
    
    2.5 Data types
    
        1）number：有加减乘除等操作；有infinity以及NaN-计算错误，后者一出现都是错
        2）bigint：超大整数（2**53 -1 ）
        3）string：一般用“”或者‘’：直接引用。但是反引号`嵌入字符中`一般与大括号连用alert( `the result is ${1 + 2}` ); // the result is 3 
        4）boolean：是否
        5) undefined：未被赋值；null：空集
        6) typeof：得知类型
        7)
    
    2.6 Interaction: alert, prompt, confirm
    
        alert
        prompt：一般两部分：result = prompt(title, [default])，default为输入内容
            * let age = prompt('How old are you?', 100);
            * alert(`You are ${age} years old!`); // You are 100 years old!
        confirm：一般输入问题，弹出true或false的选项
    
    2.7 Type Conversions
    
        String（）
        
        number：Number（）；“6”/“2” = 3
            undefined = NaN
            null = 0
            true = 1； false = 0
            Number（“”） = 去掉空格、换行符 \n、制表符 \t 等纯数字，则为数字；若有其他符号，返回NaN。alert( Number("   123   ") ); // 123； alert( Number("123z") );      // NaN
            
        boolean： 为“空”的值（如 0、空字符串、null、undefined 和 NaN）将变为 false。否则为1。
            
    2.8 Basic operators, maths ❕❕
        
        取余 %：alert( 5 % 2 ); // 1，5 除以 2 的余数
        求幂 **：alert( 4 ** (1/2) ); // 2（1/2 次方与平方根相同)
        
        “”与+：  alert( '1' + 2 ); // "12"
                alert( '1' + ‘2’ ); // "12"
                alert(2 + 2 + '1' ); // "41"，不是 "221"
                alert('1' + 2 + 2); // "122"，不是 "14" - 往后影响了
                
        + 一元运算符：对于非数字类型变为数字：alert( +true ); // 1
                                        alert( +"" );   // 0 - 类似Number（）
        ++：counter = counter +1 //只适合variable，不实用于常数，常数也不会变呀！
        --：counter = counter - 1 
        
        comma：let a = (1 + 2, 3 + 4); alert( a ); // 7（3 + 4 的结果）只返回最后的值
        
    2.9 Comparisons
    
    2.10 
    
3. 

4. 

5. 
