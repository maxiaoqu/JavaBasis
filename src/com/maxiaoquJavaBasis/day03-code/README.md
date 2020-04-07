## 流程控制语句：if判断语句、switch语句、for循环、while循环、do-while循环、break关键字、continue关键字、for嵌套循环

### Demo01Sequence.java(顺序结构)
```shell
一、执行的顺序：
    开始--->步骤A===>步骤C===>步骤...===>介绍
```

### Demo02If.java(if判断语句：单if语句)
```shell
一、执行流程 
    首先判断关系表达式看其结果是true还是false 
    如果是true就执行语句体 
    如果是false就不执行语句体

二、表达式
    if(关系表达式){
        语句体;
    }
```

### Demo03IfElse.java(if判断语句：标准的if-else语句)
```shell
一、执行流程 
    首先判断关系表达式看其结果是true还是false 
    如果是true就执行语句体1 
    如果是false就执行语句体2    

二、表达式
    if(关系表达式){
        语句体1;
    }else{
        语句体2;
    }
```

### Demo03IfElse.java(if判断语句：if..else if..else)
```shell
一、执行流程 
    首先判断关系表达式1看其结果是true还是false 
    如果是true就执行语句体1 
    如果是false就继续判断关系表达式2看其结果是true还是false 
    如果是true就执行语句体2 
    如果是false就继续判断关系表达式…看其结果是true还是false 
    如果没有任何关系表达式为true，就执行语句体3。

二、表达式
    if(关系表达式){
        语句体1;
    } else if(关系表达式2){
        语句体2;
    }else{
        语句体3;
    }
```

### Demo05IfElsePractise.java(if判断语句：if..else if..（多个else if）...else)
```shell
一、执行流程 
    首先判断关系表达式1看其结果是true还是false 
    如果是true就执行语句体1 
    如果是false就继续判断关系表达式2看其结果是true还是false 
    如果是true就执行语句体2 
    如果是false就继续判断关系表达式…看其结果是true还是false 
    … 
    如果没有任何关系表达式为true，就执行语句体n+1。

二、表达式
    if(关系表达式){
        语句体1;
    } else if(关系表达式2){
        语句体2;
    }
    ....
    else if(关系表达式2){
        语句体n;
    }else{
        语句体n+1;
    }
```

### Demo06Max.java(三元运算符+if判断语句)
```shell
    1、使用三元运算符和标准的if-else语句来实现相应的流程判断结构；
    2、在某些简单的应用中，if语句是可以和三元运算符互换使用的。
```

### Demo07Switch.java(switch语句)
```shell
一、执行流程 
    首先计算出表达式的值 
    其次，和case依次比较，一旦有对应的值，就会执行相应的语句，在执行的过程中，遇到break就会结束。
    最后，如果所有的case都和表达式的值不匹配，就会执行default语句体部分，然后程序结束掉。

二、表达式
    switch(表达式) {
        case 常量值1:
            语句体1;     
            break;   
        case 常量值2:     
            语句体2;     
            break;   
        ...   
        default:     
            语句体n+1;     
            break; 
    }
```

### Demo08SwitchNotice.java(switch语句使用的注意事项)
```shell
一、switch语句使用的注意事项：
    1. 多个case后面的数值不可以重复。
    2. switch后面小括号当中只能是下列数据类型：
        基本数据类型：byte/short/char/int
        引用数据类型：String字符串、enum枚举
    3. switch语句格式可以很灵活：前后顺序可以颠倒，而且break语句还可以省略。
    “匹配哪一个case就从哪一个位置向下执行，直到遇到了break或者整体结束为止。”

二、表达式
    switch(表达式) {
        case 常量值1:
            语句体1;     
            break;   
        case 常量值2:     
            语句体2;     
            break;   
        ...   
        default:     
            语句体n+1;     
            break; 
    }
```

### Demo09For.java(for循环)
```shell
一、循环结构的基本组成部分，一般可以分成四部分：
    1. 初始化语句：在循环开始最初执行，而且只做唯一一次。
    2. 条件判断：如果成立，则循环继续；如果不成立，则循环退出。
    3. 循环体：重复要做的事情内容，若干行语句。
    4. 步进语句：每次循环之后都要进行的扫尾工作，每次循环结束之后都要执行一次。

二、表达式
    for (初始化语句; 条件判断; 步进语句) {
        循环体
    }
```

### Demo10While.java(while循环)
```shell
一、while循环有一个标准格式，还有一个扩展格式。
  
二、表达式
    while (条件判断) {
        循环体
    }
  
三、扩展格式：
    初始化语句;
    while (条件判断) {
        循环体;
        步进语句;
    }
```

### Demo11DoWhile.java(do-while循环)
```shell
一、表达式
    do {
    	循环体
    } while (条件判断);
    
二、扩展格式：
    初始化语句
    do {
    	循环体
    	步进语句
    } while (条件判断);
```

### Demo12HundredSum.java(题目练习)
```shell
一、题目：求出1-100之间的偶数和。
  
二、思路：
    1. 既然范围已经确定了是1到100之间，那么我就从1、2、3⋯⋯一直到100这么多数字一个一个进行检查。
    2. 总共有100个数字，并非所有数字都能用。必须要是偶数才能用，判断（if语句）偶数：num % 2 == 0
    3. 需要一个变量，用来进行累加操作。也就好比是一个存钱罐。
```

### Demo13LoopDifference.java(三种循环的区别)
```shell
一、三种循环的区别。
    1. 如果条件判断从来没有满足过，那么for循环和while循环将会执行0次，但是do-while循环会执行至少一次。
    2. for循环的变量在小括号当中定义，只有循环内部才可以使用。while循环和do-while循环初始化语句本来就在外面，所以出来循环之后还可以继续使用
```

### Demo14Break.java(break关键字)
```shell
一、break关键字的用法有常见的两种：
    1. 可以用在switch语句当中，一旦执行，整个switch语句立刻结束。
    2. 还可以用在循环语句当中，一旦执行，整个循环语句立刻结束。打断循环。
  
二、关于循环的选择，有一个小建议：
    凡是次数确定的场景多用for循环；否则多用while循环。
```

### Demo15Continue.java(continue关键字)
```shell
一、continue关键字：
    一旦执行，立刻跳过当前次循环剩余内容，马上开始下一次循环。
```

### Demo16DeadLoop.java(死循环)
```shell
一、死循环：
    永远停不下来的循环，叫做死循环。
    
二、死循环格式（错误用法）
    死循环的标准格式：
    while (true) {
    	循环体
    }
```

### Demo17LoopHourAndMinute.java(for嵌套循环)
```shell
一、for嵌套循环：
    第二个for循环在第一个循环里面，都有第二个循环执行循环体；
    
二、表达式
    for (初始化语句; 条件判断; 步进语句) {
        for (初始化语句2; 条件判断2; 步进语句2) {
            循环体
        }
    }
```