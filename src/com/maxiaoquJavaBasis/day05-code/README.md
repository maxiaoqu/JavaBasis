## 数组的初始化、使用

### Demo01Array.java(数组的相关概念：动态初始化)
```shell
一、数组的概念：
    是一种容器，可以同时存放多个数据值。

二、数组的特点：
    1. 数组是一种引用数据类型
    2. 数组当中的多个数据，类型必须统一
    3. 数组的长度在程序运行期间不可改变

三、数组的初始化：
    在内存当中创建一个数组，并且向其中赋予一些默认值。

四、两种常见的初始化方式：
    1. 动态初始化（指定长度）
    2. 静态初始化（指定内容）

五、动态初始化数组的格式：
    数据类型[] 数组名称 = new 数据类型[数组长度];

六、解析含义：
    左侧数据类型：也就是数组当中保存的数据，全都是统一的什么类型
    左侧的中括号：代表我是一个数组
    左侧数组名称：给数组取一个名字
    右侧的new：代表创建数组的动作
    右侧数据类型：必须和左边的数据类型保持一致
    右侧中括号的长度：也就是数组当中，到底可以保存多少个数据，是一个int数字
```

### Demo02Array.java(数组的初始化：静态初始化)
```shell
一、动态初始化（指定长度）：
    在创建数组的时候，直接指定数组当中的数据元素个数。

二、静态初始化（指定内容）：
    在创建数组的时候，不直接指定数据个数多少，而是直接将具体的数据内容进行指定。

三、静态初始化基本格式：
    数据类型[] 数组名称 = new 数据类型[] { 元素1, 元素2, ... };

四、注意事项：
    虽然静态初始化没有直接告诉长度，但是根据大括号里面的元素具体内容，也可以自动推算出来长度。
```

### Demo03Array.java(静态初始化的省略格式)
```shell
一、使用静态初始化数组的时候，格式还可以省略一下。
  
二、标准格式：
    数据类型[] 数组名称 = new 数据类型[] { 元素1, 元素2, ... };
  
三、省略格式：
    数据类型[] 数组名称 = { 元素1, 元素2, ... };
  
四、注意事项：
    1. 静态初始化没有直接指定长度，但是仍然会自动推算得到长度。
    2. 静态初始化标准格式可以拆分成为两个步骤。
    3. 动态初始化也可以拆分成为两个步骤。
    4. 静态初始化一旦使用省略格式，就不能拆分成为两个步骤了。
  
五、使用建议：
    如果不确定数组当中的具体内容，用动态初始化；
    否则，已经确定了具体的内容，用静态初始化。
```

### Demo04ArrayUse.java(动态初始化:访问数组元素)
```shell
一、直接打印数组名称，得到的是数组对应的：内存地址哈希值。
    二进制：01
    十进制：0123456789
    16进制：0123456789abcdef

二、访问数组元素的格式：数组名称[索引值]
    索引值：就是一个int数字，代表数组当中元素的编号。
    【注意】索引值从0开始，一直到“数组的长度-1”为止。
```

### Demo05ArrayUse.java(动态初始化:数组访问数组元素)
```shell
一、使用动态初始化数组的时候，其中的元素将会自动拥有一个默认值。规则如下：
    如果是整数类型，那么默认为0；
    如果是浮点类型，那么默认为0.0；
    如果是字符类型，那么默认为'\u0000'；
    如果是布尔类型，那么默认为false；
    如果是引用类型，那么默认为null。

二、注意事项：
    静态初始化其实也有默认值的过程，只不过系统自动马上将默认值替换成为了大括号当中的具体数值。
```

### Demo06ArrayOne.java(只有一个数组的内存图)
<p align="center">
    <span>java中的内存划分</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/01-Java中的内存划分.png"/>
    <br/>
    <span>只有一个数组的内存图</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/02-只有一个数组的内存图.png"/>
</p>

```shell
只有一个数组的内存图
```

### Demo07ArrayTwo.java(两个独立数组的内存图)
<p align="center">
    <span>有两个独立数组的内存图</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/03-有两个独立数组的内存图.png"/>
</p>

```shell
两个独立数组的内存图
```

### Demo08ArraySame.java(两个引用指向同一个数组的内存图)
<p align="center">
    <span>两个引用指向同一个数组的内存图</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/04-两个引用指向同一个数组的内存图.png"/>
</p>

```shell
两个引用指向同一个数组的内存图
```

### Demo09ArrayIndex.java(数组索引越界异常)
```shell
一、数组的索引编号从0开始，一直到“数组的长度-1”为止。

二、如果访问数组元素的时候，索引编号并不存在，
那么将会发生:
数组索引越界异常 ArrayIndexOutOfBoundsException

三、原因：索引编号写错了。

四、解决：修改成为存在的正确索引编号。
```

### Demo10ArrayNull.java(数组空指针异常)
```shell
一、所有的引用类型变量，都可以赋值为一个null值。但是代表其中什么都没有。

二、数组必须进行new初始化才能使用其中的元素。
如果只是赋值了一个null，没有进行new创建，
那么将会发生：
空指针异常 NullPointerException

三、原因：忘了new

四、解决：补上new
```

### Demo11ArrayLength.java(获取数组的长度)
<p align="center">
    <span>数组的长度运行期间不可改变</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/05-数组的长度运行期间不可改变.png"/>
</p>

```shell
一、如何获取数组的长度，格式：
数组名称.length

二、这将会得到一个int数字，代表数组的长度。

三、数组一旦创建，程序运行期间，长度不可改变。
```

### Demo12Array.java(遍历数组)
```shell
遍历数组，说的就是对数组当中的每一个元素进行逐一、挨个儿处理。默认的处理方式就是打印输出。
```

### Demo13ArrayMax.java(获取数组最大值)
<p align="center">
    <span>比武招亲的示意图:[获取数组最值]</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/06-比武招亲的示意图.png"/>
</p>

```shell
获取数组最大值
```

### Demo14ArrayMin.java(获取数组最小值)
```shell
获取数组最小值
```

### Demo15ArrayReverse.java(数组元素的反转)
<p align="center">
    <span>数组元素反转的思路</span>
    <img width="300" src="https://raw.githubusercontent.com/maxiaoqu/JavaBasis/master/src/image/day05/07-数组元素反转的思路.png"/>
</p>

```shell
一、数组元素的反转：
    本来的样子：[1, 2, 3, 4]
    之后的样子：[4, 3, 2, 1]

二、要求不能使用新数组，就用原来的唯一一个数组。
```

### Demo16ArrayParam.java(数组作为方法参数：传递地址)
```shell
一、数组可以作为方法的参数。
当调用方法的时候，向方法的小括号进行传参，传递进去的其实是数组的地址值。
```

### Demo17ArrayReturn.java(数组作为方法返回值：返回地址)
```shell
一、一个方法可以有0、1、多个参数；但是只能有0或者1个返回值，不能有多个返回值。
如果希望一个方法当中产生了多个结果数据进行返回，怎么办？
解决方案：使用一个数组作为返回值类型即可。

二、任何数据类型都能作为方法的参数类型，或者返回值类型。

三、数组作为方法的参数，传递进去的其实是数组的地址值。

四、数组作为方法的返回值，返回的其实也是数组的地址值。
```


