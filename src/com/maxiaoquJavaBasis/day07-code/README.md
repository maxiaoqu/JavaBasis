## Api的使用：Scanner、Random、ArrayList

[api文档：JDK_API_1_6_zh_CN.CHM](./JDK_API_1_6_zh_CN.CHM)
【PS:找不到时，直接看该目录的JDK_API_1_6_zh_CN.CHM文件即可】

> ## 第一部分：Scanner类的使用、练习

### demo01.Demo01Scanner.java(Scanner类的功能、使用)
```shell
一、Scanner类的功能：可以实现键盘输入数据，到程序当中。
    引用类型的一般使用步骤：
    1. 导包
        import 包路径.类名称;
        如果需要使用的目标类，和当前类位于同一个包下，则可以省略导包语句不写。
        只有java.lang包下的内容不需要导包，其他的包都需要import语句。
    2. 创建
        类名称 对象名 = new 类名称();
    3. 使用
        对象名.成员方法名()

二、获取键盘输入的一个int数字：
    int num = sc.nextInt();

三、获取键盘输入的一个字符串：
    String str = sc.next();
```

### demo01.Demo01ScannerSum.java(Scanner类的练习)
```shell
一、题目：
    键盘输入两个int数字，并且求出和值。

二、思路：
    1. 既然需要键盘输入，那么就用Scanner
    2. Scanner的三个步骤：导包、创建、使用
    3. 需要的是两个数字，所以要调用两次nextInt方法
    4. 得到了两个数字，就需要加在一起。
    5. 将结果打印输出。
```

### demo01.Demo01ScannerMax.java(Scanner类的练习)
```shell
一、题目：
    键盘输入三个int数字，然后求出其中的最大值。

二、思路：
    1. 既然是键盘输入，肯定需要用到Scanner
    2. Scanner三个步骤：导包、创建、使用nextInt()方法
    3. 既然是三个数字，那么调用三次nextInt()方法，得到三个int变量
    4. 无法同时判断三个数字谁最大，应该转换成为两个步骤：
        4.1 首先判断前两个当中谁最大，拿到前两个的最大值
        4.2 拿着前两个中的最大值，再和第三个数字比较，得到三个数字当中的最大值
    5. 打印最终结果
```


> ## 第二部分：创建对象的标准格式、Scanner类使用方式

### demo02.PersonDay72.java(创建一个PersonDay72类)
```shell
创建一个PersonDay72类
```

### demo02.Demo01Anonymous.java(创建对象的标准格式)
```shell
一、创建对象的标准格式：
    类名称 对象名 = new 类名称();

二、匿名对象就是只有右边的对象，没有左边的名字和赋值运算符。
    new 类名称();

三、注意事项：
    匿名对象只能使用唯一的一次，下次再用不得不再创建一个新对象。

四、使用建议：
如果确定有一个对象只需要使用唯一的一次，就可以用匿名对象。
```

### demo02.Demo02Anonymous.java(Scanner类，创建对象使用方式)
```shell
创建对象使用方式
    普通使用方式
    匿名对象的方式
    使用一般写法传入参数
    使用匿名对象来进行传参
```

> ## 第三部分：Random类、练习

### demo03.Demo01Random.java(Random类用来生成随机数字)
```shell
一、Random类用来生成随机数字。使用起来也是三个步骤：
    1. 导包
        import java.util.Random;
    2. 创建
        Random r = new Random(); // 小括号当中留空即可
    3. 使用
        获取一个随机的int数字（范围是int所有范围，有正负两种）：int num = r.nextInt()
        获取一个随机的int数字（参数代表了范围，左闭右开区间）：int num = r.nextInt(3)
        实际上代表的含义是：[0,3)，也就是0~2
```

### demo03.Demo02Random.java(Random类练习，Random的取值范围)
```shell
Random类练习，Random的取值范围
```

### demo03.Demo03Random.java(Random类练习)
```shell
一、题目要求：
    根据int变量n的值，来获取随机数字，范围是[1,n]，可以取到1也可以取到n。

二、思路：
    1. 定义一个int变量n，随意赋值
    2. 要使用Random：三个步骤，导包、创建、使用
    3. 如果写10，那么就是0~9，然而想要的是1~10，可以发现：整体+1即可。
    4. 打印随机数字
```

### demo03.Demo04RandomGame.java(Random类练习)
```shell
一、题目：
    用代码模拟猜数字的小游戏。（二分查找法）

二、思路：
    1. 首先需要产生一个随机数字，并且一旦产生不再变化。用Random的nextInt方法
    2. 需要键盘输入，所以用到了Scanner
    3. 获取键盘输入的数字，用Scanner当中的nextInt方法
    4. 已经得到了两个数字，判断（if）一下：
        如果太大了，提示太大，并且重试；
        如果太小了，提示太小，并且重试；
        如果猜中了，游戏结束。
    5. 重试就是再来一次，循环次数不确定，用while(true)。
```

> ## 第四部分：ArrayList类、使用、练习

### demo04.PersonDay74.java(创建一个PersonDay74类)
```shell
创建一个PersonDay74类
```

### demo04.Demo01Array.java(复习数组的创建)
```shell
一、题目：
    定义一个数组，用来存储3个Person对象。

二、数组有一个缺点：
    一旦创建，程序运行期间长度不可以发生改变。
```

### demo04.Demo02ArrayList.java(ArrayList类、创建)
```shell
一、特点
    数组的长度不可以发生改变。
    但是ArrayList集合的长度是可以随意变化的。

二、对于ArrayList来说，有一个尖括号<E>代表泛型。
    泛型：也就是装在集合当中的所有元素，全都是统一的什么类型。
    注意：泛型只能是引用类型，不能是基本类型。

三、注意事项：
    对于ArrayList集合来说，直接打印得到的不是地址值，而是内容。
    如果内容是空，得到的是空的中括号：[]
```

### demo04.Demo03ArrayListMethod.java(ArrayList当中的常用方法)
```shell
一、ArrayList当中的常用方法有：

    public boolean add(E e)：
        向集合当中添加元素，参数的类型和泛型一致。返回值代表添加是否成功。
        备注：对于ArrayList集合来说，add添加动作一定是成功的，所以返回值可用可不用。
        但是对于其他集合（今后学习）来说，add添加动作不一定成功。
  
    public E get(int index)：
        从集合当中获取元素，参数是索引编号，返回值就是对应位置的元素。
  
    public E remove(int index)：
        从集合当中删除元素，参数是索引编号，返回值就是被删除掉的元素。
  
    public int size()：
        获取集合的尺寸长度，返回值是集合中包含的元素个数。
```

### demo04.Demo04ArrayListEach.java(遍历ArrayList创建的数组)
```shell
遍历ArrayList创建的数组
```

### demo04.Demo05ArrayListBasic.java(ArrayList当中存储基本类型数据的“包装类”)
```shell
一、如果希望向集合ArrayList当中存储基本类型数据，必须使用基本类型对应的“包装类”。
    基本类型    包装类（引用类型，包装类都位于java.lang包下）
    byte        Byte
    short       Short
    int         Integer     【特殊】
    long        Long
    float       Float
    double      Double
    char        Character   【特殊】
    boolean     Boolean

二、从JDK 1.5+开始，支持自动装箱、自动拆箱。
    自动装箱：基本类型 --> 包装类型
    自动拆箱：包装类型 --> 基本类型
```

> ## 第五部分：ArrayList类、使用、练习

### demo05.Demo01ArrayListRandom.java(Random类、ArrayList类的练习)
```shell
一、题目：
    生成6个1~33之间的随机整数，添加到集合，并遍历集合。

二、思路：
    1. 需要存储6个数字，创建一个集合，<Integer>
    2. 产生随机数，需要用到Random
    3. 用循环6次，来产生6个随机数字：for循环
    4. 循环内调用r.nextInt(int n)，参数是33，0~32，整体+1才是1~33
    5. 把数字添加到集合中：add
    6. 遍历集合：for、size、get
```

### demo05.StudentDay75.java(创建一个StudentDay75类)
```shell
创建一个StudentDay75类
```

### demo05.Demo02ArrayListStudent.java(StudentDay75类、ArrayList类的练习)
```shell
一、题目：
    自定义4个学生对象，添加到集合，并遍历。

二、思路：
    1. 自定义Student学生类，四个部分。
    2. 创建一个集合，用来存储学生对象。泛型：<Student>
    3. 根据类，创建4个学生对象。
    4. 将4个学生对象添加到集合中：add
    5. 遍历集合：for、size、get
```

### demo05.Demo03ArrayListPrint.java(ArrayList类的练习)
```shell
一、题目：
    定义以指定格式打印集合的方法(ArrayList类型作为参数)，使用{}扩起集合，使用@分隔每个元素。
    格式参照 {元素@元素@元素}。

二、思路：
    System.out.println(list);       [10, 20, 30]
    printArrayList(list);           {10@20@30}
```

### demo05.Demo04ArrayListReturn.java(ArrayList类的练习)
```shell
一、题目：
    用一个大集合存入20个随机数字，然后筛选其中的偶数元素，放到小集合当中。
    要求使用自定义的方法来实现筛选。
  
二、分析：
    1. 需要创建一个大集合，用来存储int数字：<Integer>
    2. 随机数字就用Random nextInt
    3. 循环20次，把随机数字放入大集合：for循环、add方法
    4. 定义一个方法，用来进行筛选。
        筛选：
            根据大集合，筛选符合要求的元素，得到小集合。
        三要素：
            返回值类型：ArrayList小集合（里面元素个数不确定）
            方法名称：getSmallList
            参数列表：ArrayList大集合（装着20个随机数字）
    5. 判断（if）是偶数：num % 2 == 0
    6. 如果是偶数，就放到小集合当中，否则不放。
```