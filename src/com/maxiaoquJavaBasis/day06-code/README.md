## 类与对象、封装、构造方法

> ## 第一部分：面向过程\面向对象概述

### demo01.Demo01PrintArray.java(面向对象思想的概述)
```shell
一、面向过程：
    当需要实现一个功能的时候，每一个具体的步骤都要亲力亲为，详细处理每一个细节。

二、面向对象：
    当需要实现一个功能的时候，不关心具体的步骤，而是找一个已经具有该功能的人，来帮我做事儿。
```

### demo01.Student.java(类的定义)
```shell
一、定义一个类，用来模拟“学生”事物。其中就有两个组成部分：
    属性（是什么）：
        姓名
        年龄
    行为（能做什么）：
        吃饭
        睡觉
        学习

二、对应到Java的类当中：
    成员变量（属性）：
        String name; // 姓名
        int age; // 年龄
    成员方法（行为）：
        public void eat() {} // 吃饭饭
        public void sleep() {} // 睡觉觉
        public void study() {} // 打豆豆

三、注意事项：
    1. 成员变量是直接定义在类当中的，在方法外边。
    2. 成员方法不要写static关键字。
```

### demo01.Demo02Student.java && demo01.Student.java(对象的创建和使用)
```shell
一、通常情况下，一个类并不能直接使用，需要根据类创建一个对象，才能使用。

    1. 导包：也就是指出需要使用的类，在什么位置。
    import 包名称.类名称;
    import cn.itcast.day06-code.demo01.Student;
    对于和当前类属于同一个包的情况，可以省略导包语句不写。

    2. 创建，格式：
    类名称 对象名 = new 类名称();
    demo01.Student stu = new demo01.Student();

    3. 使用，分为两种情况：
    使用成员变量：对象名.成员变量名
    使用成员方法：对象名.成员方法名(参数)
    （也就是，想用谁，就用对象名点儿谁。）

二、注意事项：
如果成员变量没有进行赋值，那么将会有一个默认值，规则和数组一样。
```


> ## 第二部分：练习（定义一个手机类）

### demo02.Phone.java(练习：定义一个手机类)
```shell
一、定义一个类，用来模拟“手机”事物。
    属性：品牌、价格、颜色
    行为：打电话、发短信

二、对应到类当中：
    成员变量（属性）：
        String brand; // 品牌
        double price; // 价格
        String color; // 颜色
    成员方法（行为）：
        public void call(String who) {} // 打电话
        public void sendMessage() {} // 群发短信
```

### demo02.Demo01PhoneOne.java(练习：简单的使用这个手机类)
<p align="center">
    <span>只有一个对象的内存图</span>
    <img width="100%" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/01-只有一个对象的内存图.png"/>
</p>

```shell
简单的使用这个手机类
```

### demo02.Demo02PhoneTwo.java(练习：两个对象使用同一个方法的内存图)
<p align="center">
    <span>两个对象使用同一个方法的内存图</span>
    <img width="100%" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/02-两个对象使用同一个方法的内存图.png"/>
</p>

```shell
两个对象使用同一个方法的内存图
```

### demo02.Demo03PhoneSame.java(练习：03-两个引用指向同一个对象的内存图)
<p align="center">
    <span>两个引用指向同一个对象的内存图</span>
    <img width="100%" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/03-两个引用指向同一个对象的内存图.png"/>
</p>

```shell
两个引用指向同一个对象的内存图
```

### demo02.Demo04PhoneParam.java(练习：使用对象类型作为方法的参数)
<p align="center">
    <span>使用对象类型作为方法的参数</span>
    <img width="100%" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/04-使用对象类型作为方法的参数.png"/>
</p>

```shell
使用对象类型作为方法的参数
```

### demo02.Demo05PhoneReturn.java(练习：使用对象类型作为方法的返回值)
<p align="center">
    <span>使用对象类型作为方法的返回值</span>
    <img width="100%" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/05-使用对象类型作为方法的返回值.png"/>
</p>

```shell
使用对象类型作为方法的返回值
```


> ## 第三部分：成员变量和局部变量的区别、封装方法

### demo03.Demo01VariableDifference.java(成员变量和局部变量的区别)
```shell
一、局部变量和成员变量
    1. 定义的位置不一样【重点】
        局部变量：在方法的内部
        成员变量：在方法的外部，直接写在类当中
    
    2. 作用范围不一样【重点】
        局部变量：只有方法当中才可以使用，出了方法就不能再用
    成员变量：整个类全都可以通用。
    
    3. 默认值不一样【重点】
        局部变量：没有默认值，如果要想使用，必须手动进行赋值
        成员变量：如果没有赋值，会有默认值，规则和数组一样
    
    4. 内存的位置不一样（了解）
        局部变量：位于栈内存
        成员变量：位于堆内存
    
    5. 生命周期不一样（了解）
        局部变量：随着方法进栈而诞生，随着方法出栈而消失
        成员变量：随着对象创建而诞生，随着对象被垃圾回收而消失
```

### demo03.Demo02Method.java(面向对象三大特征：封装==>方法)
```shell
一、面向对象三大特征：封装、继承、多态。

二、封装性在Java当中的体现：
    1. 方法就是一种封装
    2. 关键字private也是一种封装

三、封装就是将一些细节信息隐藏起来，对于外界不可见。
```

### demo03.Person.java(定义一个Person类)
```shell
一、问题描述：
    定义Person的年龄时，无法阻止不合理的数值被设置进来。

二、解决方案：
    用private关键字将需要保护的成员变量进行修饰。

三、一旦使用了private进行修饰，那么本类当中仍然可以随意访问。
    但是！超出了本类范围之外就不能再直接访问了。

四、间接访问private成员变量，就是定义一对儿Getter/Setter方法

五、必须叫setXxx或者是getXxx命名规则。
    对于Getter来说，不能有参数，返回值类型和成员变量对应；
    对于Setter来说，不能有返回值，参数类型和成员变量对应。
```

### demo03.Demo03Person.java && demo03.Person.java(封装练习==>private)
```shell
关键字private也是一种封装
```

### demo03.Student.java(定义一个Student类)
```shell
对于基本类型当中的boolean值，Getter方法一定要写成isXxx的形式，而setXxx规则不变。
```

### demo03.Demo04Student.java && demo03.Student.java(封装练习==>private)
```shell
封装练习==>private
```


> ## 第四部分：成员变量和局部变量的区别、封装方法

### demo04.Person.java(this关键字)
```shell
当方法的局部变量和类的成员变量重名的时候，根据“就近原则”，优先使用局部变量。
如果需要访问本类当中的成员变量，需要使用格式：
this.成员变量名

“通过谁调用的方法，谁就是this。”
```

### demo04.Demo01Person.java && demo04.Person.java(封装练习==>this关键字)
```shell
this解决重名分不开的问题
```

### demo04.Student.java(定义一个Student类)
```shell
构造方法是专门用来创建对象的方法，当我们通过关键字new来创建对象时，其实就是在调用构造方法。
    格式：
        public 类名称(参数类型 参数名称) {
            方法体
        }

注意事项：
    1. 构造方法的名称必须和所在的类名称完全一样，就连大小写也要一样
    2. 构造方法不要写返回值类型，连void都不写
    3. 构造方法不能return一个具体的返回值
    4. 如果没有编写任何构造方法，那么编译器将会默认赠送一个构造方法，没有参数、方法体什么事情都不做。
    public Student() {}
    5. 一旦编写了至少一个构造方法，那么编译器将不再赠送。
    6. 构造方法也是可以进行重载的。

重载：方法名称相同，参数列表不同。
```

### demo04.Demo02Student.java && demo04.Student.java(封装练习==>构造方法)
```shell
封装练习==>构造方法
```


> ## 第五部分：定义一个标准的类

### demo05.Student.java(定义一个Student类)
```shell
一个标准的类通常要拥有下面四个组成部分：

    1. 所有的成员变量都要使用private关键字修饰
    2. 为每一个成员变量编写一对儿Getter/Setter方法
    3. 编写一个无参数的构造方法
    4. 编写一个全参数的构造方法

这样标准的类也叫做Java Bean

Getter/Setter可以通过快捷键生成：code->Genearte..->。。。。
```

### demo05.Demo01Student.java && demo05.Student.java(定义一个标准的类)
```shell
定义一个标准的类
```