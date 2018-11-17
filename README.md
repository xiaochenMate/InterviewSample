	
整理了最新的Adroid面试题，持续更新中...
=======================================
[我的博客](https://blog.csdn.net/a458339341)  
----------------------------------------------
主要分为以下几部分：	
-------------------------
	（1）java面试题
	（2）Android面试题
	（3）混合开发面试题
	（4）高端技术面试题
	（5）非技术性问题&HR问题汇总
 
 
<br> 一、java面试题
 
<br> 熟练掌握java是很关键的，大公司不仅仅要求你会使用几个api，更多的是要你熟悉源码实现原理，甚至要你知道有哪些不足，怎么改进，还有一些java有关的一些算法，设计模式等等。
 
<br> （一） java基础面试知识点
 
<br>  java中==和equals和hashCode的区别
<br> int、char、long各占多少字节数
<br> Java基本类型占用的字节数：
<br> 1字节： byte , boolean
<br> 2字节： short , char
<br> 4字节： int , float
<br> 8字节： long , double
<br> 编码与中文：
<br> Unicode/GBK： 中文2字节
<br> UTF-8： 中文通常3字节，在拓展B区之后的是4字节
<br> 综上，中文字符在编码中占用的字节数一般是2-4个字节。
<br> C语言中short通常是2字节，具体可能和平台编译器相关。
<br> ü int与integer的区别
<br> 　①、Integer 是 int 包装类，int 是八大基本数据类型之一（byte,char,short,int,long,float,double,boolean）
<br>  
<br> 　　②、Integer 是类，默认值为null，int是基本数据类型，默认值为0；
<br>  
<br> 　　③、Integer 表示的是对象，用一个引用指向这个对象，而int是基本数据类型，直接存储数值。
<br> ü 谈谈对java多态的理解
<br> <br> 继承：继承是从已有类得到继承信息创建新类的过程。提供继承信息的类被称为父类（超类、基类）；得到继承信息的类被称为子类（派生类）。继承让变化中的软件系统有了一定的延续性，同时继承也是封装程序中可变因素的重要手段。
<br> <br> 封装：通常认为封装是把数据和操作数据的方法绑定起来，对数据的访问只能通过已定义的接口。面向对象的本质就是将现实世界描绘成一系列完全自治、封闭的对象。我们在类中编写的方法就是对实现细节的一种封装；我们编写一个类就是对数据和数据操作的封装。可以说，封装就是隐藏一切可隐藏的东西，只向外界提供最简单的编程接口（可以想想普通洗衣机和全自动洗衣机的差别，明显全自动洗衣机封装更好因此操作起来更简单；我们现在使用的智能手机也是封装得足够好的，因为几个按键就搞定了所有的事情）。
<br> <br> 多态：多态性是指允许不同子类型的对象对同一消息作出不同的响应。简单的说就是用同样的对象引用调用同样的方法但是做了不同的事情。多态性分为编译时的多态性和运行时的多态性。如果将对象的方法视为对象向外界提供的服务，那么运行时的多态性可以解释为：当A系统访问B系统提供的服务时，B系统有多种提供服务的方式，但一切对A系统来说都是透明的（就像电动剃须刀是A系统，它的供电系统是B系统，B系统可以使用电池供电或者用交流电，甚至还有可能是太阳能，A系统只会通过B类对象调用供电的方法，但并不知道供电系统的底层实现是什么，究竟通过何种方式获得了动力）。方法重载（overload）实现的是编译时的多态性（也称为前绑定），而方法重写（override）实现的是运行时的多态性（也称为后绑定）。运行时的多态是面向对象最精髓的东西，要实现多态需要做两件事：1. 方法重写（子类继承父类并重写父类中已有的或抽象的方法）；2. 对象造型（用父类型引用引用子类型对象，这样同样的引用调用同样的方法就会根据子类对象的不同而表现出不同的行为）。
<br> <br> ü String、StringBuffer、StringBuilder区别
Java 平台提供了两种类型的字符串：String和StringBuffer / StringBuilder，它们可以储存和操作字符串。其中String是只读字符串，也就意味着String引用的字符串内容是不能被改变的。而StringBuffer和StringBulder类表示的字符串对象可以直接进行修改。StringBuilder是JDK1.5引入的，它和StringBuffer的方法完全相同，区别在于它是单线程环境下使用的，因为它的所有方面都没有被synchronized修饰，因此它的效率也比StringBuffer略高。
<br> <br> ü 什么是内部类？内部类的作用
<br> <br> 可以将一个类的定义放在另一个类的定义的内部，这就是内部类。
<br> <br> 内部类的作用：
<br> <br> 1、内部类可以很好的实现隐藏
<br> <br> 2、内部类拥有外围类的所有元素的访问权限
<br> <br> 3、可以实现多重继承
<br> <br> 4、可以避免接口中的方法和同一个类中的方法同名的问题
<br> <br> ü 抽象类和接口区别
<br> 抽象类和接口都不能够实例化，但可以定义抽象类和接口类型的引用。一个类如果继承了某个抽象类或者实现了某个接口都需要对其中的抽象方法全部进行实现，否则该类仍然需要被声明为抽象类。接口比抽象类更加抽象，因为抽象类中可以定义构造器，可以有抽象方法和具体方法，而接口中不能定义构造器而且其中的方法全部都是抽象方法。抽象类中的成员可以是private、默认、protected、public的，而接口中的成员全都是public的。抽象类中可以定义成员变量，而接口中定义的成员变量实际上都是常量。有抽象方法的类必须被声明为抽象类，而抽象类未必要有抽象方法。
<br> ü 抽象类的意义
<br> 抽象类：
<br> 一个类中如果包含抽象方法，这个类应该用abstract关键字声明为抽象类。
<br> 意义：
<br> 1，为子类提供一个公共的类型；
<br> 2，封装子类中重复内容（成员变量和方法）；
<br> 3，定义有抽象方法，子类虽然有不同的实现，但该方法的定义是一致的。
<br> ü 抽象类与接口的应用场景
<br> <br> <br> interface的应用场合
 <br> <br> <br>     A. 类与类之前需要特定的接口进行协调，而不在乎其如何实现。
 <br> <br> <br>     B. 作为能够实现特定功能的标识存在，也可以是什么接口方法都没有的纯粹标识。
 <br> <br> <br>     C. 需要将一组类视为单一的类，而调用者只通过接口来与这组类发生联系。
 <br> <br> <br>     D. 需要实现特定的多项功能，而这些功能之间可能完全没有任何联系。
<br> <br> <br> abstract class的应用场合
<br> <br> <br>      一句话，在既需要统一的接口，又需要实例变量或缺省的方法的情况下，就可以使用它。最常见的有：
<br> <br> <br>      A. 定义了一组接口，但又不想强迫每个实现类都必须实现所有的接口。可以用abstract class定义一组方法体，甚至可以是空方法体，然后由子类选择自己所感兴趣的方法来覆盖。
<br> <br> <br>      B. 某些场合下，只靠纯粹的接口不能满足类与类之间的协调，还必需类中表示状态的变量来区别不同的关系。abstract的中介作用可以很好地满足这一点。
<br> <br> <br>      C. 规范了一组相互协调的方法，其中一些方法是共同的，与状态无关的，可以共享的，无需子类分别实现；而另一些方法却需要各个子类根据自己特定的状态来实现特定的功能
<br> <br> <br> ü 抽象类是否可以没有方法和属性？
抽象类中可以没有抽象方法，但有抽象方法的一定是抽象类。所以，java中 抽象类里面可以没有抽象方法。比如HttpServlet类。抽象类和普通类的区别就在于，抽象类不能被实例化，就是不能被new出来，即使抽象类里面没有抽象方法。 抽象类的作用在于子类对其的继承和实现，也就是多态；而没有抽象方法的抽象类的存在价值在于：实例化了没有意义，因为类已经定义好了，不能改变其中的方法体，但是实例化出来的对象却满足不了要求，只有继承并重写了他的子类才能满足要求。所以才把它定义为没有抽象方法的抽象类

<br> <br> ü 接口的意义
<br> <br> 1.根据客户提出的需求提出来，作为接口的；业务具体实现是通过实现接口类来完成的。 
<br> <br> 2.当客户提出新的需求时，只需编写该需求业务逻辑新的实现类。 
<br> <br> 3.假如采用了这种模式，业务逻辑更加清晰，增强代码可读性，扩展性，可维护性。 
<br> <br> 4.接口和实现分离，适合团队协作开发。 
<br> <br> 5.实现松散耦合的系统，便于以后升级，扩展。
<br> <br> ü 泛型中extends和super的区别
<br> <br> <? extends T>：是指 “上界通配符（Upper Bounds Wildcards）”
<br> <br> <? super T>：是指 “下界通配符（Lower Bounds Wildcards）”
<br> <br>    <? extends T>限定参数类型的上界：参数类型必须是T或T的子类型
<br> <br>      <? super T> 限定参数类型的下界：参数类型必须是T或T的超类型
<br> <br> 总结为：
<br> <br> <? extends T> 只能用于方法返回，告诉编译器此返参的类型的最小继承边界为T，T和T的父类都能接收，但是入参类型无法确定，只能接受null的传入
<br> <br> <? super T>只能用于限定方法入参，告诉编译器入参只能是T或其子类型，而返参只能用Object类接收
<br> <br> ? 既不能用于入参也不能用于返参
<br> <br> ü 父类的静态方法能否被子类重写
<br> <br>  父类的静态方法可以被子类继承，但是不能重写。
<br> <br> ü 进程和线程的区别
<br>  根本区别：进程是操作系统资源分配的基本单位，而线程是任务调度和执行的基本单位

<br> 在开销方面：每个进程都有独立的代码和数据空间（程序上下文），程序之间的切换会有较大的开销；线程可以看做轻量级的进程，同一类线程共享代码和数据空间，每个线程都有自己独立的运行栈和程序计数器（PC），线程之间切换的开销小。

<br> 所处环境：在操作系统中能同时运行多个进程（程序）；而在同一个进程（程序）中有多个线程同时执行（通过CPU调度，在每个时间片中只有一个线程执行）

<br> 内存分配方面：系统在运行的时候会为每个进程分配不同的内存空间；而对线程而言，除了CPU外，系统不会为线程分配内存（线程所使用的资源来自其所属进程的资源），线程组之间只能共享资源。

<br> 包含关系：没有线程的进程可以看做是单线程的，如果一个进程内有多个线程，则执行过程不是一条线的，而是多条线（线程）共同完成的；线程是进程的一部分，所以线程也被称为轻权进程或者轻量级进程。

<br> ü final，finally，finalize的区别
<br> final:用于声明属性，方法和类，分别表示属性不可变，方法不可覆盖，类不可继承。
<br> finally：异常处理结构语句的一部分  表示总是执行。
<br> finalize：object 类的一个方法，在垃圾收集器执行的时候会调用被回收对象的此方法，可以覆盖次方法提供垃圾收集时的其他资源回收，例如关闭文件等。JVM不保<br> 证次方法总是被调用。

<br> ü 序列化的方式
<br>  第一种是实现Serializable接口（是JavaSE本身就支持的），第二种是实现Parcelable接口（是Android特有功能，效率比实现Serializable接口高效，可用于Intent数据传递，也可以用于进程间通信（IPC））。实现Serializable接口非常简单，声明一下就可以了，而实现Parcelable接口稍微复杂一些，但效率更高，推荐用这种方法提高性能。
<br> ü Serializable 和Parcelable 的区别
 编码上：
<br> Serializable代码量少，写起来方便
<br> Parcelable代码多一些
<br> 效率上：
<br> Parcelable的速度比Serializable 高十倍以上
<br> serializable的迷人之处在于你只需要对某个类以及它的属性实现Serializable 接口即可。Serializable 接口是一种标识接口（marker interface），这意味着无需实现方法，Java便会对这个对象进行高效的序列化操作。
<br> 这种方法的缺点是使用了反射，序列化的过程较慢。这种机制会在序列化的时候创建许多的临时对象，容易触发垃圾回收。
<br> Parcelable方式的实现原理是将一个完整的对象进行分解，而分解后的每一部分都是Intent所支持的数据类型，这样也就实现传递对象的功能了
<br> ü 静态属性和静态方法是否可以被继承？是否可以被重写？以及原因？
父类的静态方法可以被子类继承，但是不能重写。 随着类的加载而加载，不依赖任何对象，它与任何类都没有关系
<br> ü 静态内部类的设计意图
 静态内部类与非静态内部类之间存在一个最大的区别：非静态内部类在编译完成之后会隐含地保存着一个引用，该引用是指向创建它的外围内，但是静态内部类却没有。
没有这个引用就意味着：
它的创建是不需要依赖于外围类的。
它不能使用任何外围类的非static成员变量和方法。
<br> ü 成员内部类、静态内部类、局部内部类和匿名内部类的理解，以及项目中的应用
 对于成员内部类，必须先产生外部类的实例化对象，才能产生内部类的实例化对象。而静态内部类不用产生外部类的实例化对象即可产生内部类的实例化对象。
局部内部类是定义在一个方法或者一个作用域里面的类，它和成员内部类的区别在于局部内部类的访问仅限于方法内或者该作用域内。匿名内部类应该是平时我们编写代码时用得最多的，在编写事件监听的代码时使用匿名内部类不但方便，而且使代码更加容易维护。
<br> ü 谈谈对kotlin的理解
<br>  简介
<br>        Kotlin是一门静态语言，支持多种平台，包括移动端、服务端以及浏览器端，此外，Kotlin还是一门融合了面向对象与函数式编程的语言，支持泛型、安全的空判断，并且Kotlin与Java可以做到完全的交互。
<br> Kotlin特点
代码量少且代码末尾没有分号。
被调用的方法需放到上边。
<br> Kotlin是空安全的：在编译时期就处理了各种null的情况，避免了执行时异常。
它可扩展函数：我们也可以扩展任意类的更多的特性。
它也是函数式的：比如，使用lambda表达式来更方便地解决问题。
高度互操作性：你可以继续使用所有用Java写的代码和库，甚至可以在一个项目中使用Kotlin和Java两种语言混合编程

<br> ü 闭包和局部内部类的区别
 闭包： 是一种能够被调用的对象，它保存了创建它的作用域的信息。
局部内部类:是嵌套在方法和作用域内的，对于这个类的使用主要是应用与解决比较复杂的问题，想创建一个类来辅助我们的解决方案，到那时又不希望这个类是公共可用的，所以就产生了局部内部类，局部内部类和成员内部类一样被编译，只是它的作用域发生了改变，它只能在该方法和属性中被使用，出了该方法和属性就会失效。

<br> ü string 转换成 integer的方式及原理
 integer.parseInt(string str)方法调用Integer内部的 
parseInt(string str,10)方法,默认基数为10，parseInt内部首先 
判断字符串是否包含符号（-或者+），则对相应的negative和limit进行 
赋值，然后再循环字符串，对单个char进行数值计算Character.digit(char ch, int radix) 
在这个方法中，函数肯定进入到0-9字符的判断（相对于string转换到int）， 
否则会抛出异常，数字就是如上面进行拼接然后生成的int类型数值。

<br><br>原文：https://blog.csdn.net/itboy_libing/article/details/80393530 

 
<br>（二） java深入源码级的面试题（有难度）
 
<br>ü 哪些情况下的对象会被垃圾回收机制处理掉？
<br>. 引用计数法
<br>当有一个引用指向对象的时候counter就加一，当不在引用此对象时就让counter减一。所以，当counter等于零的时候虚拟机就认为此对象时可以被回收的
. 可达性分析算法
<br>虚拟机会先将一些对象定义为GC Roots，从GC Roots出发一直沿着引用链向下寻找，如果某个对象不能通过GC Roots寻找到，那么虚拟机就认为该对象可以被回收。
<br>ü 讲一下常见编码方式？
<br>ASCII码：共有128个，用一个字节的低7位表示
<br> ISO8859-1：在ASCII码的基础上涵盖了大多数西欧语言字符，仍然是单字节编码，它总共能表示256个字符 
<br>GB2312：全称为《信息交换用汉字编码字符集基本集》，它是双字节编码，总的编码范围是A1~F7 A1~A9 ·符号区 B0~F7 汉字区 
<br>GBK：《数字交换用汉字编码字符集》，它可能是单字节、双字节或者四字节编码，与GB2312编码兼容 
<br>UTF-16：具体定义了Unicode字符在计算机中的存取方法。采用2字节来表示Unicode转化格式，它是定长的表示方法，不论什么字符都可以用两个字节表示
<br> UTF-8： UTF-8采用一种变长技术，每个编码区域有不同的字码长度，不同的字符可以由1~6个字节组成。 如果一个字节，最高位为0，表示这是一个ASCII字符<br>（00~7F） 如果一个字节，以11开头，连续的1的个数暗示这个字符的字节数
<br>链接：https://www.jianshu.com/p/54a3b6988368
<br>ü utf-8编码中的中文占几个字节；int型几个字节？
<br>utf-8的编码规则：
<br>如果一个字节，最高位为0，表示这是一个ASCII字符（00~7F）
<br>如果一个字节，以11开头，连续的1的个数暗示这个字符的字节数
<br>一个utf8数字占1个字节
<br>一个utf8英文字母占1个字节
少数是汉字每个占用3个字节，多数占用4个字节。
ü 静态代理和动态代理的区别，什么场景使用？
<br>静态代理通常只代理一个类，动态代理是代理一个接口下的多个实现类。 
<br>静态代理事先知道要代理的是什么，而动态代理不知道要代理什么东西，只有在运行时才知道。 
动态代理是实现JDK里的InvocationHandler接口的invoke方法，但注意的是代理的是接口，也就是你的业务类必须要实现接口，<br>。 
<br>还有一种动态代理CGLIB，代理的是类，不需要业务类继承接口，通过派生的子类来实现代理。通过在运行时，动态修改字节码达到修改类的目的。
<br>原文：https://blog.csdn.net/Xinyeshuaiqi/article/details/80673008 

<br>ü Java的异常体系
<br>Java异常架构图

<br>Throwable Throwable是 Java 语言中所有错误或异常的超类。 Throwable包含两个子类: Error 和 Exception 。它们通常用于指示发生了异常情况。 Throwable包含了其线程创建时线程执行堆栈的快照，它提供了printStackTrace()等接口用于获取堆栈跟踪数据等信息。
<br>Exception Exception及其子类是 Throwable 的一种形式，它指出了合理的应用程序想要捕获的条件。
<br>RuntimeException RuntimeException是那些可能在 Java 虚拟机正常运行期间抛出的异常的超类。 编译器不会检查RuntimeException异常。 例如，除数为零时，抛出ArithmeticException异常。RuntimeException是ArithmeticException的超类。当代码发生除数为零的情况时，倘若既"没有通过throws声明抛出ArithmeticException异常"，也"没有通过try...catch...处理该异常"，也能通过编译。这就是我们所说的"编译器不会检查RuntimeException异常"！ 如果代码会产生RuntimeException异常，则需要通过修改代码进行避免。 例如，若会发生除数为零的情况，则需要通过代码避免该情况的发生！
Error 和Exception一样， Error也是Throwable的子类。 它用于指示合理的应用程序不应该试图捕获的严重问题，大多数这样的错误都是异常条件。 和RuntimeException一样， 编译器也不会检查Error。
<br>Java将可抛出(Throwable)的结构分为三种类型： 被检查的异常(Checked Exception)，运行时异常(RuntimeException)和错误(Error)。
<br>(01) 运行时异常 定义 : RuntimeException及其子类都被称为运行时异常。 特点 : Java编译器不会检查它。 也就是说，当程序中可能出现这类异常时，倘若既"没有通过throws声明抛出它"，也"没有用try-catch语句捕获它"，还是会编译通过。例如，除数为零时产生的ArithmeticException异常，数组越界时产生的IndexOutOfBoundsException异常，fail-fail机制产生的ConcurrentModificationException异常等，都属于运行时异常。 虽然Java编译器不会检查运行时异常，但是我们也可以通过throws进行声明抛出，也可以通过try-catch对它进行捕获处理。 如果产生运行时异常，则需要通过修改代码来进行避免。 例如，若会发生除数为零的情况，则需要通过代码避免该情况的发生！
<br>(02) 被检查的异常 定义 : Exception类本身，以及Exception的子类中除了"运行时异常"之外的其它子类都属于被检查异常。 特点 : Java编译器会检查它。 此类异常，要么通过throws进行声明抛出，要么通过try-catch进行捕获处理，否则不能通过编译。例如，CloneNotSupportedException就属于被检查异常。当通过clone()接口去克隆一个对象，而该对象对应的类没有实现Cloneable接口，就会抛出CloneNotSupportedException异常。 被检查异常通常都是可以恢复的。
<br>(03) 错误 定义 : Error类及其子类。 特点 : 和运行时异常一样，编译器也不会对错误进行检查。 当资源不足、约束失败、或是其它程序无法继续运行的条件发生时，就产生错误。程序本身无法修复这些错误的。例如，VirtualMachineError就属于错误。 按照Java惯例，我们是不应该是实现任何新的Error子类的！
对于上面的3种结构，我们在抛出异常或错误时，到底该哪一种？《Effective Java》中给出的建议是： 对于可以恢复的条件使用被检查异常，对于程序错误使用运行时异常。
<br>ü 谈谈你对解析与分派的认识。
<br>1.方法在程序真正运行之前就有一个可确定的调用版本，并且这个方法的调用版本在运行期间是不可变的，即“编译时可知，运行不可以变”，这类目标的方法的调用称之为解析
<br>2.解析调用一定是个静态的过程，在编译期就完全确定，在类加载的解析阶段就将涉及的符号引用全部转变为可以确定的直接引用，不会延迟到运行期再去完成。而分派（Dispatch）调用则可能是静态的也可能是动的。于是分派方式就有静态分派和动态分派。
静态分派的最直接的解释是在重载的时候是通过参数的静态类型而不是实际类型作为判断依据的。因此在编译阶段，Javac编译器会根据参数的静态类型决定使用哪个重载版本。
显然这里不可能根据静态类型来决定调用那个方法。导致这个现象很明显的原因是因为这两个变量的实际类型不一样，jvm根据实际类型来分派方法执行版本。
链接：https://www.jianshu.com/p/985534b21089
<br>ü 修改对象A的equals方法的签名，那么使用HashMap存放这个对象实例的时候，会调用哪个equals方法？
会调用对象对象的equals方法。
<br>“==”如果是基本类型的话就是看他们的数据值是否相等就可以。
<br>如果是引用类型的话，比较的是栈内存局部变量表中指向堆内存中的指针的值是否相等
<br>“equals”如果对象的equals方法没有重写的话，equals方法和“==”是同一种。
<br>hashcod是返回对象实例内存地址的hash映射。
<br>理论上所有对象的hash映射都是不相同的。
问题：
<br>1.你用过hashmap么？
答：是的，然后回答HashMap的一些特性，譬如HashMap可以接受null键值和值，而Hashtable则不能；HashMap是非synchronized;HashMap很快；以及HashMap储存的是键值对等等。
<br>2.你知道hashmap的工作原理么？
答：HashMap是基于hashing的原理，我们使用put(key, value)存储对象到HashMap中，使用get(key)从HashMap中获取对象。当我们给put()方法传递键和值时，我们先对键调用hashCode()方法，返回的hashCode用于找到bucket位置来储存Entry对象。”这里关键点在于指出，HashMap是在bucket中储存键对象和值对象，作为Map.Entry。这一点有助于理解获取对象的逻辑。如果你没有意识到这一点，或者错误的认为仅仅只在bucket中存储值的话，你将不会回答如何从HashMap中获取对象的逻辑。这个答案相当的正确，也显示出面试者确实知道hashing以及HashMap的工作原理。但是这仅仅是故事的开始，当面试官加入一些Java程序员每天要碰到的实际场景的时候，错误的答案频现。
for (Map.Entry<Integer, Integer> entry : map.entrySet()) {
System.out.println(entry.getKey() + ":" + entry.getValue());
}
<br>3.当两个对象的hashcode相同会发生什么？
因为即使hashcode相同，但是equals不同。
因为hashcode相同，所以它们的bucket位置相同，‘碰撞’会发生。因为HashMap使用链表存储对象，这个Entry(包含有键值对的Map.Entry对象)会存储在链表中。
<br>4.如果两个键的hashcode相同，你如何获取值对象？
当我们调用get()方法，HashMap会使用键对象的hashcode找到bucket位置，然后获取值对象。
<br>5.面试官提醒他如果有两个值对象储存在同一个bucket？
将会遍历链表直到找到值对象
<br>6.因为你并没有值对象去比较，你是如何确定确定找到值对象的？
找到bucket位置之后，会调用keys.equals()方法去找到链表中正确的节点，最终找到要找的值对象。
--------------------------------------------------------------------------------
一些优秀的开发者会指出使用不可变的、声明作final的对象，并且采用合适的equals()和hashCode()方法的话，将会减少碰撞的发生，提高效率。不可变性使得能够缓存不同键的hashcode，这将提高整个获取对象的速度，使用String，Interger这样的wrapper类作为键是非常好的选择。

链接：https://www.jianshu.com/p/985534b21089

<br>ü Java中实现多态的机制是什么？
多态性是指允许不同子类型的对象对同一消息作出不同的响应。简单的说就是用同样的对象引用调用同样的方法但是做了不同的事情。多态性分为编译时的多态性和运行时的多态性。如果将对象的方法视为对象向外界提供的服务，那么运行时的多态性可以解释为：当A系统访问B系统提供的服务时，B系统有多种提供服务的方式，但一切对A系统来说都是透明的（就像电动剃须刀是A系统，它的供电系统是B系统，B系统可以使用电池供电或者用交流电，甚至还有可能是太阳能，A系统只会通过B类对象调用供电的方法，但并不知道供电系统的底层实现是什么，究竟通过何种方式获得了动力）。方法重载（overload）实现的是编译时的多态性（也称为前绑定），而方法重写（override）实现的是运行时的多态性（也称为后绑定）。运行时的多态是面向对象最精髓的东西，要实现多态需要做两件事：1. 方法重写（子类继承父类并重写父类中已有的或抽象的方法）；2. 对象造型（用父类型引用引用子类型对象，这样同样的引用调用同样的方法就会根据子类对象的不同而表现出不同的行为）。
流程：调用方法时，虚拟机通过对象引用得到方法区中类型信息的方法表的指针入口，查询类的方法表 ，根据实例方法的符号引用解析出该方法在方法表的偏移量，子类对象声明为父类类型时，形式上调用的是父类的方法，此时虚拟机会从实际的方法表中找到方法地址，从而定位到实际类的方法。 注：所有引用为父类，但方法区的类型信息中存放的是子类的信息，所以调用的是子类的方法表。
<br>ü 如何将一个Java对象序列化到文件里？
1）对象需要实现Seralizable接口
public class StudentBean implements Serializable {
······
}
2）通过ObjectOutputStream的writeObject()方法写入
和ObjectInputStream的readObject()方法来进行读取
//存进去
try {
ObjectOutputStream os = new ObjectOutputStream(
new FileOutputStream("D:/student.txt"));
os.writeObject(studentList);
os.close();
} catch (FileNotFoundException e) {
// TODO Auto-generated catch block
e.printStackTrace();
} catch (IOException e) {
// TODO Auto-generated catch block
e.printStackTrace();
}
//读出来
try {
ObjectInputStream is = new ObjectInputStream(
new FileInputStream("D:/student.txt"));
ArrayList<StudentBean> list = new ArrayList<StudentBean>();
list = (ArrayList<StudentBean>) is.readObject();
for (int i = 0; i < list.size(); i++) {
System.out.println(list.get(i).toString());
}
} catch (FileNotFoundException e) {
// TODO Auto-generated catch block
e.printStackTrace();
} catch (IOException e) {
// TODO Auto-generated catch block
e.printStackTrace();
} catch (ClassNotFoundException e) {
// TODO Auto-generated catch block
e.printStackTrace();
}
链接：https://www.jianshu.com/p/cb970e5cd5b8
<br>ü 说说你对Java反射的理解
JAVA反射机制是在运行状态中, 对于任意一个类, 都能够知道这个类的所有属性和方法; 对于任意一个对象, 都能够调用它的任意一个方法和属性; 这种动态获取的信息以及动态调用对象的方法的功能称为java语言的反射机制.
主要作用有三：
运行时取得类的方法和字段的相关信息。
创建某个类的新实例(.newInstance())
取得字段引用直接获取和设置对象字段，无论访问修饰符是什么。
用处如下：
观察或操作应用程序的运行时行为。
调试或测试程序，因为可以直接访问方法、构造函数和成员字段。
通过名字调用不知道的方法并使用该信息来创建对象和调用方法。
第一步：获取该类的类类型（这一步非常关键）

那么我们怎么去获取呢：
其实很简答，一共有三种方法：
1.利用Class c  = Class.forName("")----------传就来要获取类的路径，会出现异常。
2.利用Class c = A.class ---------------------A代表该类的类名
3.利用Class c = a.getClass();---------------a代表的就是该类的实例化对象，也就是 A a = new A()；这一步
通过上面的方法我们就获取了该类的一个实例对象，那么我们怎么调用类里面的成员函数，成员变量呢？（注意都是public的）如果要访问私有的要在你要获取的变量后加上setAccessible(true)；例如 Filed[] filed = c.getFields(); field.setAccessible(true);
其实还是很简单：
1.c.getName（）-------------------获取该类的类名；返回String类型的值
2.c.getFileds()------------------------获取该类的所有成员变量   c.getDeclaredFields()--------自己声明的类的成员变量；
3.c.getType()---------------------------获取该类的类型
4.c.getMethods()----------------------获取所有的方法     c.getDeclaredMethod（）-----------所有声明过的方法。
分为三步：
第一：获取类的；类类型
Class c = a.getClass();
第二步：获取类的方法
Method m = c.getMethod("方法的名称"，参数的类类型new Class[]{...,.....});
第三部：传入参数，利用invoke（）函数
Object  o = m.invoke(a(实例化对象),执行函数要传进来的参数)；
原文：https://blog.csdn.net/yqynsmile/article/details/52203433 
ü 说说你对Java注解的理解
如果注解难于理解，你就把它类同于标签，标签为了解释事物，注解为了解释代码。
注解的基本语法，创建如同接口，但是多了个 @ 符号。
注解的元注解。
注解的属性。
注解主要给编译器及工具类型的软件用的。
注解的提取需要借助于 Java 的反射技术，反射比较慢，所以注解使用时也需要谨慎计较时间成本。
原文：https://blog.csdn.net/briblue/article/details/73824058 

ü 说说你对依赖注入的理解
ü 说一下泛型原理，并举例说明
泛型是Java 1.5的新特性，泛型的本质是参数化类型，也就是说所操作的数据类型被指定为一个参数。这种参数类型可以用在类、接口和方法的创建中，分别称为泛型类、泛型接口、泛型方法。

   Java泛型被引入的好处是安全简单。

在Java SE 1.5之前，没有泛型的情况的下，通过对类型Object的引用来实现参数的“任意化”，“任意化”带来的缺点是要做显式的强制类型转换，而这种转换是要求开发者对实际参数类型可以预知的情况下进行的。对于强制类型转换错误的情况，编译器可能不提示错误，在运行的时候才出现异常，这是一个安全隐患。
泛型的好处是在编译的时候检查类型安全，并且所有的强制转换都是自动和隐式的，提高代码的重用率。
泛型在使用中还有一些规则和限制： 
1、泛型的类型参数只能是类类型（包括自定义类），不能是简单类型。
2、同一种泛型可以对应多个版本（因为参数类型是不确定的），不同版本的泛型类实例是不兼容的。
3、泛型的类型参数可以有多个。
4、泛型的参数类型可以使用extends语句，例如。习惯上成为“有界类型”。
5、泛型的参数类型还可以是通配符类型。
二、泛型的作用： 
（1）、限定类型就已经有很大作用了，特别是写基础架构的时候，不需要以前那样的检查，我们的代码量和开发速度都可以提升一大截； 
（2）、Think IN JAVA : 能够进行编译期间类型检查；（官方） 
（3）、限定类型啊 通俗点比喻 （箱子贴标签）这个箱子是放苹果的 那个箱子是放橘子的 
 ( 4 )、封装一些共性问题，可以简化很多代码，使代码更加有层次，简单 
（5）、比object类范围明显缩小了，提高了程序运行的效率

原文：https://blog.csdn.net/shinecjj/article/details/52075499 

public class GenericType {
    public static void main(String[] args) {  
        ArrayList<String> arrayString=new ArrayList<String>();   
        ArrayList<Integer> arrayInteger=new ArrayList<Integer>();   
        System.out.println(arrayString.getClass()==arrayInteger.getClass());  
    }  
}
输出：
true

在这个例子中，我们定义了两个ArrayList数组，不过一个是ArrayList<String>泛型类型，只能存储字符串。一个是ArrayList<Integer>泛型类型，只能存储整型。最后，我们通过arrayString对象和arrayInteger对象的getClass方法获取它们的类信息并比较，发现结果为true。

这是为什么呢，明明我们定义了两种不同的类型？因为，在编译期间，所有的泛型信息都会被擦除，List<Integer>和List<String>类型，在编译后都会变成List类型（原始类型）。Java中的泛型基本上都是在编译器这个层次来实现的，这也是Java的泛型被称为“伪泛型”的原因。

原始类型

原始类型就是泛型类型擦除了泛型信息后，在字节码中真正的类型。无论何时定义一个泛型类型，相应的原始类型都会被自动提供。原始类型的名字就是删去类型参数后的泛型类型的类名。擦除类型变量，并替换为限定类型（T为无限定的类型变量，用Object替换）。

//泛型类型
class Pair<T> {  
    private T value;  
    public T getValue() {  
        return value;  
    }  
    public void setValue(T  value) {  
        this.value = value;  
    }  
}
//原始类型
class Pair {  
    private Object value;  
    public Object getValue() {  
        return value;  
    }  
    public void setValue(Object  value) {  
        this.value = value;  
    }  
}  
因为在Pair<T>中，T是一个无限定的类型变量，所以用Object替换。如果是Pair<T extends Number>，擦除后，类型变量用Number类型替换。


public class ReflectInGeneric {
    public static void main(String[] args) throws IllegalArgumentException, 
                        SecurityException, IllegalAccessException, InvocationTargetException, NoSuchMethodException {  
        ArrayList<Integer> array=new ArrayList<Integer>();  
        array.add(1);//这样调用add方法只能存储整形，因为泛型类型的实例为Integer  
        array.getClass().getMethod("add", Object.class).invoke(array, "asd");  
        for (int i=0;i<array.size();i++) {  
            System.out.println(array.get(i));  
        }  
    }  
}
输出：

1
asd

为什么呢？我们在介绍泛型时指出向ArrayList<Integer>中插入String类型的对象，编译时会报错。现在为什么又可以了呢？

我们在程序中定义了一个ArrayList<Integer>泛型类型，如果直接调用add方法，那么只能存储整形的数据。不过当我们利用反射调用add方法的时候，却可以存储字符串。这说明ArrayList<Integer>泛型信息在编译之后被擦除了，只保留了原始类型，类型变量（T）被替换为Object，在运行时，我们可以行其中插入任意类型的对象。

但是，并不推荐以这种方式操作泛型类型，因为这违背了泛型的初衷（减少强制类型转换以及确保类型安全）。当我们从集合中获取元素时，默认会将对象强制转换成泛型参数指定的类型（这里是Integer），如果放入了非法的对象这个强制转换过程就会出现异常。

泛型方法的类型推断
在调用泛型方法的时候，可以指定泛型类型，也可以不指定。

在不指定泛型类型的情况下，泛型类型为该方法中的几种参数类型的共同父类的最小级，直到Object。

在指定泛型类型的时候，该方法中的所有参数类型必须是该泛型类型或者其子类。


public class Test { 
    public static void main(String[] args) {  
        /**不指定泛型的时候*/  
        int i=Test.add(1, 2); //这两个参数都是Integer，所以T替换为Integer类型  
        Number f=Test.add(1, 1.2);//这两个参数一个是Integer，另一个是Float，所以取同一父类的最小级，为Number  
        Object o=Test.add(1, "asd");//这两个参数一个是Integer，另一个是String，所以取同一父类的最小级，为Object
  
        /**指定泛型的时候*/  
        int a=Test.<Integer>add(1, 2);//指定了Integer，所以只能为Integer类型或者其子类  
        int b=Test.<Integer>add(1, 2.2);//编译错误，指定了Integer，不能为Float  
        Number c=Test.<Number>add(1, 2.2); //指定为Number，所以可以为Integer和Float  
    }  
      
    //这是一个简单的泛型方法  
    public static <T> T add(T x,T y){  
        return y;  
    } 
}
正确的运转

既然说类型变量会在编译的时候擦除掉，那为什么定义了ArrayList<Integer>泛型类型，而不允许向其中插入String对象呢？不是说泛型变量Integer会在编译时候擦除变为原始类型Object吗，为什么不能存放别的类型呢？既然类型擦除了，如何保证我们只能使用泛型变量限定的类型呢？
java是如何解决这个问题的呢？java编译器是通过先检查代码中泛型的类型，然后再进行类型擦除，再进行编译的。以如下代码为例：

        Pair<Integer> pair=new Pair<Integer> ();
        pair.setValue(3);
        Integer integer=pair.getValue();
        System.out.println(integer);
擦除getValue()的返回类型后将返回Object类型，编译器自动插入Integer的强制类型转换。也就是说，编译器把这个方法调用翻译为两条字节码指令：
1、对原始方法Pair.getValue的调用

2、将返回的Object类型强制转换为Integer

此外，存取一个泛型域时，也要插入强制类型转换。因此，我们说Java的泛型是在编译器层次进行实现的，被称为“伪泛型”，相对于C++。

原文：https://blog.csdn.net/sunxianghuang/article/details/51982979 

ü Java中String的了解
一、String类
想要了解一个类，最好的办法就是看这个类的实现源代码，来看一下String类的源码：

public final class String
    implements java.io.Serializable, Comparable<String>, CharSequence
{
    /** The value is used for character storage. */
    private final char value[];

    /** The offset is the first index of the storage that is used. */
    private final int offset;

    /** The count is the number of characters in the String. */
    private final int count;

    /** Cache the hash code for the string */
    private int hash; // Default to 0

    /** use serialVersionUID from JDK 1.0.2 for interoperability */
    private static final long serialVersionUID = -6849794470754667710L;

    ........
}

从上面可以看出几点：
1）String类是final类，也即意味着String类不能被继承，并且它的成员方法都默认为final方法。在Java中，被final修饰的类是不允许被继承的，并且该类中的成员方法都默认为final方法。
2）上面列举出了String类中所有的成员属性，从上面可以看出String类其实是通过char数组来保存字符串的。
下面再继续看String类的一些方法实现：

public String substring(int beginIndex, int endIndex) {
    if (beginIndex < 0) {
        throw new StringIndexOutOfBoundsException(beginIndex);
    }
    if (endIndex > count) {
        throw new StringIndexOutOfBoundsException(endIndex);
    }
    if (beginIndex > endIndex) {
        throw new StringIndexOutOfBoundsException(endIndex - beginIndex);
    }
    return ((beginIndex == 0) && (endIndex == count)) ? this :
        new String(offset + beginIndex, endIndex - beginIndex, value);
}

public String concat(String str) {
    int otherLen = str.length();
    if (otherLen == 0) {
        return this;
    }
    char buf[] = new char[count + otherLen];
    getChars(0, count, buf, 0);
    str.getChars(0, otherLen, buf, count);
    return new String(0, count + otherLen, buf);
}

public String replace(char oldChar, char newChar) {
    if (oldChar != newChar) {
        int len = count;
        int i = -1;
        char[] val = value; /* avoid getfield opcode */
        int off = offset;   /* avoid getfield opcode */

        while (++i < len) {
        if (val[off + i] == oldChar) {
            break;
        }
        }
        if (i < len) {
        char buf[] = new char[len];
        for (int j = 0 ; j < i ; j++) {
            buf[j] = val[off+j];
        }
        while (i < len) {
            char c = val[off + i];
            buf[i] = (c == oldChar) ? newChar : c;
            i++;
        }
        return new String(0, len, buf);
        }
    }
    return this;
}

<br><br>，无论是sub操、concat还是replace操作都不是在原有的字符串上进行的，而是重新生成了一个新的字符串对象。也就是说进行这些操作<br><br>后，最原始的字符串并没有被改变。
<br><br>在这里要永远记住一点：“String对象一旦被创建就是固定不变的了，对String对象的任何改变都不影响到原对象，相关的任何change操作都会生成新的对象”。
二、字符串常量池
      我们知道字符串的分配和其他对象分配一样，是需要消耗高昂的时间和空间的，而且字符串我们使用的非常多。JVM为了提高性能和减少内存的开销，在实例化字<br><br>符串的时候进行了一些优化：使用字符串常量池。每当我们创建字符串常量时，JVM会首先检查字符串常量池，如果该字符串已经存在常量池中，那么就直接返回常量池<br><br>中的实例引用。如果字符串不存在常量池中，就会实例化该字符串并且将其放到常量池中。由于String字符串的不可变性我们可以十分肯定常量池中一定不存在两个相同<br><br>的字符串（这点对理解上面至关重要）。
<br><br>Java中的常量池，实际上分为两种形态：静态常量池和运行时常量池。
<br><br>所谓静态常量池，即*.class文件中的常量池，class文件中的常量池不仅仅包含字符串(数字)字面量，还包含类、方法的信息，占用class文件绝大部分空间。
<br><br>而运行时常量池，则是jvm虚拟机在完成类装载操作后，将class文件中的常量池载入到内存中，并保存在方法区中，我们常说的常量池，就是指方法区中的运行时常量<br><br>池。
来看下面的程序：
String a = "chenssy";
String b = "chenssy";
a、b和字面上的chenssy都是指向JVM字符串常量池中的"chenssy"对象，他们指向同一个对象。
String c = new String("chenssy");
new关键字一定会产生一个对象chenssy（注意这个chenssy和上面的chenssy不同），同时这个对象是存储在堆中。所以上面应该产生了两个对象：保存在栈中的c和保存堆中chenssy。但是在Java中根本就不存在两个完全一模一样的字符串对象。故堆中的chenssy应该是引用字符串常量池中chenssy。所以c、chenssy、池chenssy的关系应该是：c--->chenssy--->池chenssy。整个关系如下：

 通过上面的图我们可以非常清晰的认识他们之间的关系。所以我们修改内存中的值，他变化的是所有。
总结：虽然a、b、c、chenssy是不同的对象，但是从String的内部结构我们是可以理解上面的。String c = new String("chenssy");虽然c的内容是创建在堆中，但是他的内部value还是指向JVM常量池的chenssy的value，它构造chenssy时所用的参数依然是chenssy字符串常量。
下面再来看几个例子：
例子1：

/**
 * 采用字面值的方式赋值
 */
public void test1(){
    String str1="aaa";
    String str2="aaa";
    System.out.println("===========test1============");
    System.out.println(str1==str2);//true 可以看出str1跟str2是指向同一个对象 
}

执行上述代码，结果为：true。
分析：当执行String str1="aaa"时，JVM首先会去字符串池中查找是否存在"aaa"这个对象，如果不存在，则在字符串池中创建"aaa"这个对象，然后将池中"aaa"这个对象的引用地址返回给字符串常量str1，这样str1会指向池中"aaa"这个字符串对象；如果存在，则不创建任何对象，直接将池中"aaa"这个对象的地址返回，赋给字符串常量。当创建字符串对象str2时，字符串池中已经存在"aaa"这个对象，直接把对象"aaa"的引用地址返回给str2，这样str2指向了池中"aaa"这个对象，也就是说str1和str2指向了同一个对象，因此语句System.out.println(str1 == str2)输出：true。
例子2：

/**
 * 采用new关键字新建一个字符串对象
 */
public void test2(){
    String str3=new String("aaa");
    String str4=new String("aaa");
    System.out.println("===========test2============");
    System.out.println(str3==str4);//false 可以看出用new的方式是生成不同的对象 
}

 执行上述代码，结果为：false。
分析： 采用new关键字新建一个字符串对象时，JVM首先在字符串池中查找有没有"aaa"这个字符串对象，如果有，则不在池中再去创建"aaa"这个对象了，直接在堆中创建一个"aaa"字符串对象，然后将堆中的这个"aaa"对象的地址返回赋给引用str3，这样，str3就指向了堆中创建的这个"aaa"字符串对象；如果没有，则首先在字符串池中创建一个"aaa"字符串对象，然后再在堆中创建一个"aaa"字符串对象，然后将堆中这个"aaa"字符串对象的地址返回赋给str3引用，这样，str3指向了堆中创建的这个"aaa"字符串对象。当执行String str4=new String("aaa")时， 因为采用new关键字创建对象时，每次new出来的都是一个新的对象，也即是说引用str3和str4指向的是两个不同的对象，因此语句System.out.println(str3 == str4)输出：false。
例子3：

/**
 * 编译期确定
 */
public void test3(){
    String s0="helloworld";
    String s1="helloworld";
    String s2="hello"+"world";
    System.out.println("===========test3============");
    System.out.println(s0==s1); //true 可以看出s0跟s1是指向同一个对象 
    System.out.println(s0==s2); //true 可以看出s0跟s2是指向同一个对象 
}

执行上述代码，结果为：true、true。
分析：因为例子中的s0和s1中的"helloworld”都是字符串常量，它们在编译期就被确定了，所以s0==s1为true；而"hello”和"world”也都是字符串常量，当一个字符串由多个字符串常量连接而成时，它自己肯定也是字符串常量，所以s2也同样在编译期就被解析为一个字符串常量，所以s2也是常量池中"helloworld”的一个引用。所以我们得出s0==s1==s2。
例子4：

/**
 * 编译期无法确定
 */
public void test4(){
    String s0="helloworld"; 
    String s1=new String("helloworld"); 
    String s2="hello" + new String("world"); 
    System.out.println("===========test4============");
    System.out.println( s0==s1 ); //false  
    System.out.println( s0==s2 ); //false 
    System.out.println( s1==s2 ); //false
}

执行上述代码，结果为：false、false、false。
分析：用new String() 创建的字符串不是常量，不能在编译期就确定，所以new String() 创建的字符串不放入常量池中，它们有自己的地址空间。
s0还是常量池中"helloworld”的引用，s1因为无法在编译期确定，所以是运行时创建的新对象"helloworld”的引用，s2因为有后半部分new String(”world”)所以也无法在编译期确定，所以也是一个新创建对象"helloworld”的引用。
例子5：

/**
 * 继续-编译期无法确定
 */
<br>public void test5(){
 <br>   String str1="abc";   
    String str2="def";   
<br>    String str3=str1+str2;
<br>    System.out.println("===========test5============");
<br>    System.out.println(str3=="abcdef"); //false
}

<br>执行上述代码，结果为：false。
<br>分析：因为str3指向堆中的"abcdef"对象，而"abcdef"是字符串池中的对象，所以结果为false。JVM对String str="abc"对象放在常量池中是在编译时做的，而String str3=str1+str2是在运行时刻才能知道的。new对象也是在运行时才做的。而这段代码总共创建了5个对象，字符串池中两个、堆中三个。+运算符会在堆中建立<br>来两个String对象，这两个对象的值分别是"abc"和"def"，也就是说从字符串池中复制这两个值，然后在堆中创建两个对象，然后再建立对象str3,然后将"abcdef"的堆地址赋给str3。
步骤： 
1)栈中开辟一块中间存放引用str1，str1指向池中String常量"abc"。 
2)栈中开辟一块中间存放引用str2，str2指向池中String常量"def"。 
3)栈中开辟一块中间存放引用str3。
4)str1 + str2通过StringBuilder的最后一步toString()方法还原一个新的String对象"abcdef"，因此堆中开辟一块空间存放此对象。
5)引用str3指向堆中(str1 + str2)所还原的新String对象。 
6)str3指向的对象在堆中，而常量"abcdef"在池中，输出为false。
例子6：

/**
<br> * 编译期优化
 */
<br>public void test6(){
 <br>   String s0 = "a1"; 
 <br>   String s1 = "a" + 1; 
 <br>   System.out.println("===========test6============");
 <br>   System.out.println((s0 == s1)); //result = true  
 <br>   String s2 = "atrue"; 
    String s3= "a" + "true"; 
<br>    System.out.println((s2 == s3)); //result = true  
 <br>   String s4 = "a3.4"; 
<br>    String s5 = "a" + 3.4; 
<br>    System.out.println((s4 == s5)); //result = true
}

<br>执行上述代码，结果为：true、true、true。
<br>分析：在程序编译期，JVM就将常量字符串的"+"连接优化为连接后的值，拿"a" + 1来说，经编译器优化后在class中就已经是a1。在编译期其字符串常量的值就确定下<br>来，故上面程序最终的结果都为true。
<br>例子7：

<br>/**
<br> * 编译期无法确定
<br> */
<br>public void test7(){
<br>    String s0 = "ab"; 
<br> <br>   String s1 = "b"; 
<br>    String s2 = "a" + s1; 
<br>    System.out.println("===========test7============");
<br>    System.out.println((s0 == s2)); //result = false
<br>}
<br>
<br>执行上述代码，结果为：false。
<br>分析：JVM对于字符串引用，由于在字符串的"+"连接中，有字符串引用存在，而引用的值在程序编译期是无法确定的，即"a" + s1无法被编译器优化，只有在程序运行<br>期来动态分配并将连接后的新地址赋给s2。所以上面程序的结果也就为false。
<br>例子8：
<br>
<br>/**
<br> * 比较字符串常量的“+”和字符串引用的“+”的区别
<br> */
<br>public void test8(){
    String test="javalanguagespecification";
    String str="java";
    String str1="language";
    String str2="specification";
    System.out.println("===========test8============");
    System.out.println(test == "java" + "language" + "specification");
    System.out.println(test == str + str1 + str2);
}

执行上述代码，结果为：true、false。
分析：为什么出现上面的结果呢？这是因为，字符串字面量拼接操作是在Java编译器编译期间就执行了，也就是说编译器编译时，直接把"java"、"language"和"specification"这三个字面量进行"+"操作得到一个"javalanguagespecification" 常量，并且直接将这个常量放入字符串池中，这样做实际上是一种优化，将3个字面量合成一个，避免了创建多余的字符串对象。而字符串引用的"+"运算是在Java运行期间执行的，即str + str2 + str3在程序执行期间才会进行计算，它会在堆内存中重新创建一个拼接后的字符串对象。总结来说就是：字面量"+"拼接是在编译期间进行的，拼接后的字符串存放在字符串池中；而字符串引用的"+"拼接运算实在运行时进行的，新创建的字符串存放在堆中。
对于直接相加字符串，效率很高，因为在编译器便确定了它的值，也就是说形如"I"+"love"+"java"; 的字符串相加，在编译期间便被优化成了"Ilovejava"。对于间接相加（即包含字符串引用），形如s1+s2+s3; 效率要比直接相加低，因为在编译器不会对引用变量进行优化。
例子9：

/**
 * 编译期确定
 */
public void test9(){
    String s0 = "ab"; 
    final String s1 = "b"; 
    String s2 = "a" + s1;  
    System.out.println("===========test9============");
    System.out.println((s0 == s2)); //result = true
}

执行上述代码，结果为：true。
分析：和例子7中唯一不同的是s1字符串加了final修饰，对于final修饰的变量，它在编译时被解析为常量值的一个本地拷贝存储到自己的常量池中或嵌入到它的字节码流中。所以此时的"a" + s1和"a" + "b"效果是一样的。故上面程序的结果为true。
例子10：

/**
 * 编译期无法确定
 */
public void test10(){
    String s0 = "ab"; 
    final String s1 = getS1(); 
    String s2 = "a" + s1; 
    System.out.println("===========test10============");
    System.out.println((s0 == s2)); //result = false 
    
}

private static String getS1() {  
    return "b";   
}

执行上述代码，结果为：false。
分析：这里面虽然将s1用final修饰了，但是由于其赋值是通过方法调用返回的，那么它的值只能在运行期间确定，因此s0和s2指向的不是同一个对象，故上面程序的结果为false。
三、总结
1.String类初始化后是不可变的(immutable)
String使用private final char value[]来实现字符串的存储，也就是说String对象创建之后，就不能再修改此对象中存储的字符串内容，就是因为如此，才说String类型是不可变的(immutable)。程序员不能对已有的不可变对象进行修改。我们自己也可以创建不可变对象，只要在接口中不提供修改数据的方法就可以。
然而，String类对象确实有编辑字符串的功能，比如replace()。这些编辑功能是通过创建一个新的对象来实现的，而不是对原有对象进行修改。比如:
s = s.replace("World", "Universe");
上面对s.replace()的调用将创建一个新的字符串"Hello Universe!"，并返回该对象的引用。通过赋值，引用s将指向该新的字符串。如果没有其他引用指向原有字符串"Hello World!"，原字符串对象将被垃圾回收。

2.引用变量与对象
A aa;
这个语句声明一个类A的引用变量aa[我们常常称之为句柄]，而对象一般通过new创建。所以aa仅仅是一个引用变量，它不是对象。
3.创建字符串的方式
创建字符串的方式归纳起来有两类：
（1）使用""引号创建字符串;
（2）使用new关键字创建字符串。
结合上面例子，总结如下:
（1）单独使用""引号创建的字符串都是常量,编译期就已经确定存储到String Pool中；
（2）使用new String("")创建的对象会存储到heap中,是运行期新创建的；
new创建字符串时首先查看池中是否有相同值的字符串，如果有，则拷贝一份到堆中，然后返回堆中的地址；如果池中没有，则在堆中创建一份，然后返回堆中的地址（注意，此时不需要从堆中复制到池中，否则，将使得堆中的字符串永远是池中的子集，导致浪费池的空间）！
（3）使用只包含常量的字符串连接符如"aa" + "aa"创建的也是常量,编译期就能确定,已经确定存储到String Pool中；
（4）使用包含变量的字符串连接符如"aa" + s1创建的对象是运行期才创建的,存储在heap中；
4.使用String不一定创建对象
在执行到双引号包含字符串的语句时，如String a = "123"，JVM会先到常量池里查找，如果有的话返回常量池里的这个实例的引用，否则的话创建一个新实例并置入常量池里。所以，当我们在使用诸如String str = "abc"；的格式定义对象时，总是想当然地认为，创建了String类的对象str。担心陷阱！对象可能并没有被创建！而可能只是指向一个先前已经创建的对象。只有通过new()方法才能保证每次都创建一个新的对象。
5.使用new String，一定创建对象
在执行String a = new String("123")的时候，首先走常量池的路线取到一个实例的引用，然后在堆上创建一个新的String实例，走以下构造函数给value属性赋值，然后把实例引用赋值给a：

public String(String original) {
    int size = original.count;
    char[] originalValue = original.value;
    char[] v;
      if (originalValue.length > size) {
         // The array representing the String is bigger than the new
         // String itself.  Perhaps this constructor is being called
         // in order to trim the baggage, so make a copy of the array.
            int off = original.offset;
            v = Arrays.copyOfRange(originalValue, off, off+size);
     } else {
         // The array representing the String is the same
         // size as the String, so no point in making a copy.
        v = originalValue;
     }
    this.offset = 0;
    this.count = size;
    this.value = v;
    }

从中我们可以看到，虽然是新创建了一个String的实例，但是value是等于常量池中的实例的value，即是说没有new一个新的字符数组来存放"123"。
6.关于String.intern()
intern方法使用：一个初始为空的字符串池，它由类String独自维护。当调用 intern方法时，如果池已经包含一个等于此String对象的字符串（用equals(oject)方法确定），则返回池中的字符串。否则，将此String对象添加到池中，并返回此String对象的引用。
它遵循以下规则：对于任意两个字符串 s 和 t，当且仅当 s.equals(t) 为 true 时，s.intern() == t.intern() 才为 true。
String.intern(); 
再补充介绍一点：存在于.class文件中的常量池，在运行期间被jvm装载，并且可以扩充。String的intern()方法就是扩充常量池的一个方法；当一个String实例str调用intern()方法时，java查找常量池中是否有相同unicode的字符串常量，如果有，则返回其引用，如果没有，则在常量池中增加一个unicode等于str的字符串并返回它的引用。

/**
 * 关于String.intern()
 */
public void test11(){
    String s0 = "kvill"; 
    String s1 = new String("kvill"); 
    String s2 = new String("kvill"); 
    System.out.println("===========test11============");
    System.out.println( s0 == s1 ); //false
    System.out.println( "**********" ); 
    s1.intern(); //虽然执行了s1.intern(),但它的返回值没有赋给s1
    s2 = s2.intern(); //把常量池中"kvill"的引用赋给s2 
    System.out.println( s0 == s1); //flase
    System.out.println( s0 == s1.intern() ); //true//说明s1.intern()返回的是常量池中"kvill"的引用
    System.out.println( s0 == s2 ); //true
}

运行结果：false、false、true、true。
7.关于equals和==
（1）对于==，如果作用于基本数据类型的变量（byte,short,char,int,long,float,double,boolean ），则直接比较其存储的"值"是否相等；如果作用于引用类型的变量（String），则比较的是所指向的对象的地址（即是否指向同一个对象）。
（2）equals方法是基类Object中的方法，因此对于所有的继承于Object的类都会有该方法。在Object类中，equals方法是用来比较两个对象的引用是否相等，即是否指向同一个对象。
（3）对于equals方法，注意：equals方法不能作用于基本数据类型的变量。如果没有对equals方法进行重写，则比较的是引用类型的变量所指向的对象的地址；而String类对equals方法进行了重写，用来比较指向的字符串对象所存储的字符串是否相等。其他的一些类诸如Double，Date，Integer等，都对equals方法进行了重写用来比较指向的对象所存储的内容是否相等。

/**
 * 关于equals和==
 */
public void test12(){
    String s1="hello";
    String s2="hello";
    String s3=new String("hello");
    System.out.println("===========test12============");
    System.out.println( s1 == s2); //true,表示s1和s2指向同一对象，它们都指向常量池中的"hello"对象
    //flase,表示s1和s3的地址不同，即它们分别指向的是不同的对象,s1指向常量池中的地址，s3指向堆中的地址
    System.out.println( s1 == s3); 
    System.out.println( s1.equals(s3)); //true,表示s1和s3所指向对象的内容相同
}

8.String相关的+：
String中的 + 常用于字符串的连接。看下面一个简单的例子：

/**
 * String相关的+
 */
public void test13(){
    String a = "aa";
    String b = "bb";
    String c = "xx" + "yy " + a + "zz" + "mm" + b;
    System.out.println("===========test13============");
    System.out.println(c);
}

编译运行后，主要字节码部分如下：

public static main([Ljava/lang/String;)V
   L0
    LINENUMBER 5 L0
    LDC "aa"
    ASTORE 1
   L1
    LINENUMBER 6 L1
    LDC "bb"
    ASTORE 2
   L2
    LINENUMBER 7 L2
    NEW java/lang/StringBuilder
    DUP
    LDC "xxyy "
    INVOKESPECIAL java/lang/StringBuilder.<init> (Ljava/lang/String;)V
    ALOAD 1
    INVOKEVIRTUAL java/lang/StringBuilder.append (Ljava/lang/String;)Ljava/lang/StringBuilder;
    LDC "zz"
    INVOKEVIRTUAL java/lang/StringBuilder.append (Ljava/lang/String;)Ljava/lang/StringBuilder;
    LDC "mm"
    INVOKEVIRTUAL java/lang/StringBuilder.append (Ljava/lang/String;)Ljava/lang/StringBuilder;
    ALOAD 2
    INVOKEVIRTUAL java/lang/StringBuilder.append (Ljava/lang/String;)Ljava/lang/StringBuilder;
    INVOKEVIRTUAL java/lang/StringBuilder.toString ()Ljava/lang/String;
    ASTORE 3
   L3
    LINENUMBER 8 L3
    GETSTATIC java/lang/System.out : Ljava/io/PrintStream;
    ALOAD 3
    INVOKEVIRTUAL java/io/PrintStream.println (Ljava/lang/String;)V
   L4
    LINENUMBER 9 L4
    RETURN
   L5
    LOCALVARIABLE args [Ljava/lang/String; L0 L5 0
    LOCALVARIABLE a Ljava/lang/String; L1 L5 1
    LOCALVARIABLE b Ljava/lang/String; L2 L5 2
    LOCALVARIABLE c Ljava/lang/String; L3 L5 3
    MAXSTACK = 3
    MAXLOCALS = 4
}

显然，通过字节码我们可以得出如下几点结论：
(1).String中使用 + 字符串连接符进行字符串连接时，连接操作最开始时如果都是字符串常量，编译后将尽可能多的直接将字符串常量连接起来，形成新的字符串常量参与后续连接（通过反编译工具jd-gui也可以方便的直接看出）；
(2).接下来的字符串连接是从左向右依次进行，对于不同的字符串，首先以最左边的字符串为参数创建StringBuilder对象，然后依次对右边进行append操作，最后将StringBuilder对象通过toString()方法转换成String对象（注意：中间的多个字符串常量不会自动拼接）。
也就是说String c = "xx" + "yy " + a + "zz" + "mm" + b; 实质上的实现过程是： String c = new StringBuilder("xxyy ").append(a).append("zz").append("mm").append(b).toString();
由此得出结论：当使用+进行多个字符串连接时，实际上是产生了一个StringBuilder对象和一个String对象。
9.String的不可变性导致字符串变量使用+号的代价：
String s = "a" + "b" + "c"; 
String s1  =  "a"; 
String s2  =  "b"; 
String s3  =  "c"; 
String s4  =  s1  +  s2  +  s3;
分析：变量s的创建等价于 String s = "abc"; 由上面例子可知编译器进行了优化，这里只创建了一个对象。由上面的例子也可以知道s4不能在编译期进行优化，其对象创建相当于：
StringBuilder temp = new StringBuilder();   
temp.append(a).append(b).append(c);   
String s = temp.toString();
由上面的分析结果，可就不难推断出String 采用连接运算符（+）效率低下原因分析，形如这样的代码：

public class Test {
    public static void main(String args[]) {
        String s = null;
        for(int i = 0; i < 100; i++) {
            s += "a";
        }
    }
}

每做一次 + 就产生个StringBuilder对象，然后append后就扔掉。下次循环再到达时重新产生个StringBuilder对象，然后 append 字符串，如此循环直至结束。 如果我们直接采用 StringBuilder 对象进行 append 的话，我们可以节省 N - 1 次创建和销毁对象的时间。所以对于在循环中要进行字符串连接的应用，一般都是用StringBuffer或StringBulider对象来进行append操作。
10.String、StringBuffer、StringBuilder的区别
（1）可变与不可变：String是不可变字符串对象，StringBuilder和StringBuffer是可变字符串对象（其内部的字符数组长度可变）。
（2）是否多线程安全：String中的对象是不可变的，也就可以理解为常量，显然线程安全。StringBuffer 与 StringBuilder 中的方法和功能完全是等价的，只是StringBuffer 中的方法大都采用了synchronized 关键字进行修饰，因此是线程安全的，而 StringBuilder 没有这个修饰，可以被认为是非线程安全的。
（3）String、StringBuilder、StringBuffer三者的执行效率：
StringBuilder > StringBuffer > String 当然这个是相对的，不一定在所有情况下都是这样。比如String str = "hello"+ "world"的效率就比 StringBuilder st  = new StringBuilder().append("hello").append("world")要高。因此，这三个类是各有利弊，应当根据不同的情况来进行选择使用：
当字符串相加操作或者改动较少的情况下，建议使用 String str="hello"这种形式；
当字符串相加操作较多的情况下，建议使用StringBuilder，如果采用了多线程，则使用StringBuffer。
11.String中的final用法和理解
final StringBuffer a = new StringBuffer("111");
final StringBuffer b = new StringBuffer("222");
a=b;//此句编译不通过

final StringBuffer a = new StringBuffer("111");
a.append("222");//编译通过
可见，final只对引用的"值"(即内存地址)有效，它迫使引用只能指向初始指向的那个对象，改变它的指向会导致编译期错误。至于它所指向的对象的变化，final是不负责的。
12.关于String str = new String("abc")创建了多少个对象？
这个问题在很多书籍上都有说到比如《Java程序员面试宝典》，包括很多国内大公司笔试面试题都会遇到，大部分网上流传的以及一些面试书籍上都说是2个对象，这种说法是片面的。
首先必须弄清楚创建对象的含义，创建是什么时候创建的？这段代码在运行期间会创建2个对象么？毫无疑问不可能，用javap -c反编译即可得到JVM执行的字节码内容：

很显然，new只调用了一次，也就是说只创建了一个对象。而这道题目让人混淆的地方就是这里，这段代码在运行期间确实只创建了一个对象，即在堆上创建了"abc"对象。而为什么大家都在说是2个对象呢，这里面要澄清一个概念，该段代码执行过程和类的加载过程是有区别的。在类加载的过程中，确实在运行时常量池中创建了一个"abc"对象，而在代码执行过程中确实只创建了一个String对象。
因此，这个问题如果换成 String str = new String("abc")涉及到几个String对象？合理的解释是2个。
个人觉得在面试的时候如果遇到这个问题，可以向面试官询问清楚”是这段代码执行过程中创建了多少个对象还是涉及到多少个对象“再根据具体的来进行回答。
13.字符串池的优缺点：
字符串池的优点就是避免了相同内容的字符串的创建，节省了内存，省去了创建相同字符串的时间，同时提升了性能；另一方面，字符串池的缺点就是牺牲了JVM在常量池中遍历对象所需要的时间，不过其时间成本相比而言比较低。
四、综合实例

package com.spring.test;

public class StringTest {
    public static void main(String[] args) {  
        /** 
         * 情景一：字符串池 
          * JAVA虚拟机(JVM)中存在着一个字符串池，其中保存着很多String对象; 
         * 并且可以被共享使用，因此它提高了效率。 
         * 由于String类是final的，它的值一经创建就不可改变。 
         * 字符串池由String类维护，我们可以调用intern()方法来访问字符串池。  
         */  
        String s1 = "abc";     
        //↑ 在字符串池创建了一个对象  
        String s2 = "abc";     
        //↑ 字符串pool已经存在对象“abc”(共享),所以创建0个对象，累计创建一个对象  
        System.out.println("s1 == s2 : "+(s1==s2));    
        //↑ true 指向同一个对象，  
        System.out.println("s1.equals(s2) : " + (s1.equals(s2)));    
        //↑ true  值相等  
        //↑------------------------------------------------------over  
        /** 
         * 情景二：关于new String("") 
         *  
         */  
        String s3 = new String("abc");  
        //↑ 创建了两个对象，一个存放在字符串池中，一个存在与堆区中；  
        //↑ 还有一个对象引用s3存放在栈中  
        String s4 = new String("abc");  
        //↑ 字符串池中已经存在“abc”对象，所以只在堆中创建了一个对象  
        System.out.println("s3 == s4 : "+(s3==s4));  
        //↑false   s3和s4栈区的地址不同，指向堆区的不同地址；  
        System.out.println("s3.equals(s4) : "+(s3.equals(s4)));  
        //↑true  s3和s4的值相同  
        System.out.println("s1 == s3 : "+(s1==s3));  
        //↑false 存放的地区多不同，一个栈区，一个堆区  
        System.out.println("s1.equals(s3) : "+(s1.equals(s3)));  
        //↑true  值相同  
        //↑------------------------------------------------------over  
        /** 
         * 情景三：  
         * 由于常量的值在编译的时候就被确定(优化)了。 
         * 在这里，"ab"和"cd"都是常量，因此变量str3的值在编译时就可以确定。 
         * 这行代码编译后的效果等同于： String str3 = "abcd"; 
         */  
        String str1 = "ab" + "cd";  //1个对象  
        String str11 = "abcd";   
        System.out.println("str1 = str11 : "+ (str1 == str11));  
        //↑------------------------------------------------------over  
        /** 
         * 情景四：  
         * 局部变量str2,str3存储的是存储两个拘留字符串对象(intern字符串对象)的地址。 
         *  
         * 第三行代码原理(str2+str3)： 
         * 运行期JVM首先会在堆中创建一个StringBuilder类， 
         * 同时用str2指向的拘留字符串对象完成初始化， 
         * 然后调用append方法完成对str3所指向的拘留字符串的合并， 
         * 接着调用StringBuilder的toString()方法在堆中创建一个String对象， 
         * 最后将刚生成的String对象的堆地址存放在局部变量str3中。 
         *  
         * 而str5存储的是字符串池中"abcd"所对应的拘留字符串对象的地址。 
         * str4与str5地址当然不一样了。 
         *  
         * 内存中实际上有五个字符串对象： 
         *       三个拘留字符串对象、一个String对象和一个StringBuilder对象。 
         */  
        String str2 = "ab";  //1个对象  
        String str3 = "cd";  //1个对象                                         
        String str4 = str2+str3;                                        
        String str5 = "abcd";    
        System.out.println("str4 = str5 : " + (str4==str5)); // false  
        //↑------------------------------------------------------over  
        /** 
         * 情景五： 
         *  JAVA编译器对string + 基本类型/常量 是当成常量表达式直接求值来优化的。 
         *  运行期的两个string相加，会产生新的对象的，存储在堆(heap)中 
         */  
        String str6 = "b";  
        String str7 = "a" + str6;  
        String str67 = "ab";  
        System.out.println("str7 = str67 : "+ (str7 == str67));  
        //↑str6为变量，在运行期才会被解析。  
        final String str8 = "b";  
        String str9 = "a" + str8;  
        String str89 = "ab";  
        System.out.println("str9 = str89 : "+ (str9 == str89));  
        //↑str8为常量变量，编译期会被优化  
        //↑------------------------------------------------------over  
    }
}

运行结果：
s1 == s2 : true
s1.equals(s2) : true
s3 == s4 : false
s3.equals(s4) : true
s1 == s3 : false
s1.equals(s3) : true
str1 = str11 : true
str4 = str5 : false
str7 = str67 : false
str9 = str89 : true
https://www.cnblogs.com/xiaoxi/p/6036701.html
ü String为什么要设计成不可变的？

这是一个老生常谈的话题(This is an old yet still popular question). 在Java中将String设计成不可变的是综合考虑到各种因素的结果,想要理解这个问题,需要综合内存,同步,数据结构以及安全等方面的考虑. 在下文中,我将为各种原因做一个小结。
1. 字符串常量池的需要
字符串常量池(String pool, String intern pool, String保留池) 是Java堆内存中一个特殊的存储区域, 当创建一个String对象时,假如此字符串值已经存在于常量池中,则不会创建一个新的对象,而是引用已经存在的对象。
如下面的代码所示,将会在堆内存中只创建一个实际String对象.
String s1 = "abcd";
String s2 = "abcd";
示意图如下所示:

图1
假若字符串对象允许改变,那么将会导致各种逻辑错误,比如改变一个对象会影响到另一个独立对象. 严格来说，这种常量池的思想,是一种优化手段.
请思考: 假若代码如下所示，s1和s2还会指向同一个实际的String对象吗?
String s1= "ab" + "cd";
String s2= "abc" + "d";
也许这个问题违反新手的直觉, 但是考虑到现代编译器会进行常规的优化, 所以他们都会指向常量池中的同一个对象. 或者,你可以用 jd-gui之类的工具查看一下编译后的class文件.
2. 允许String对象缓存HashCode
Java中String对象的哈希码被频繁地使用, 比如在hashMap 等容器中。
字符串不变性保证了hash码的唯一性,因此可以放心地进行缓存.这也是一种性能优化手段,意味着不必每次都去计算新的哈希码. 在String类的定义中有如下代码:
private int hash;//用来缓存HashCode
3. 安全性
String被许多的Java类(库)用来当做参数,例如 网络连接地址URL,文件路径path,还有反射机制所需要的String参数等, 假若String不是固定不变的,将会引起各种安全隐患。
假如有如下的代码:
boolean connect(string s){
    if (!isSecure(s)) { 
throw new SecurityException(); 
}
    // 如果在其他地方可以修改String,那么此处就会引起各种预料不到的问题/错误 
    causeProblem(s);
}

总体来说, String不可变的原因包括 设计考虑,效率优化问题,以及安全性这三大方面. 事实上,这也是Java面试中的许多 "为什么" 的答案。
https://blog.csdn.net/renfufei/article/details/16808775
ü Object类的equal和hashCode方法重写，为什么？ 
 那为什么在重写equals方法时都要重写hashCode方法呢：
首先equals与hashcode间的关系是这样的：
1、如果两个对象相同（即用equals比较返回true），那么它们的hashCode值一定要相同；
2、如果两个对象的hashCode相同，它们并不一定相同(即用equals比较返回false)   
自我的理解：
由于为了提高程序的效率才实现了hashcode方法，先进行hashcode的比较，如果不同，那没就不必在进行equals的比较了，这样就大大减少了equals比较的次数，这对比需要比较的数量很大的效率提高是很明显的，一个很好的例子就是在集合中的使用；
我们都知道java中的List集合是有序的，因此是可以重复的，而set集合是无序的，因此是不能重复的，那么怎么能保证不能被放入重复的元素呢，但靠equals方法一样比较的话，如果原来集合中以后又10000个元素了，那么放入10001个元素，难道要将前面的所有元素都进行比较，看看是否有重复，欧码噶的，这个效率可想而知，因此hashcode就应遇而生了，java就采用了hash表，利用哈希算法（也叫散列算法），就是将对象数据根据该对象的特征使用特定的算法将其定义到一个地址上，那么在后面定义进来的数据只要看对应的hashcode地址上是否有值，那么就用equals比较，如果没有则直接插入，只要就大大减少了equals的使用次数，执行效率就大大提高了。
继续上面的话题，为什么必须要重写hashcode方法，其实简单的说就是为了保证同一个对象，保证在equals相同的情况下hashcode值必定相同，如果重写了equals而未重写hashcode方法，可能就会出现两个没有关系的对象equals相同的（因为equal都是根据对象的特征进行重写的），但hashcode确实不相同的。
（三） 数据结构
 
ü 常用数据结构简介
Map图接口（包含HashMap和TreeMap）;
Collection集合接口（包含List接口和Set接口）：
List线性表接口（包含ArrayList和LinkedList）;
Set集合接口（包含HashSet和TreeSet）;
Java集合大致可分为Set、List和Map三种体系，其中Set代表无序、不可重复的集合；List代表有序、重复的集合；而Map则代表具有映射关系的集合。Java 5之后，增加了Queue体系集合，代表一种队列集合实现。
ü 并发集合了解哪些？
并发List
	Vector和CopyOnWriteArrayList是两个线程安全的List，Vector读写操作都用了同步，相对来说更适用于写多读少的场合，CopyOnWriteArrayList在写的时候会复制一个副本，对副本写，写完用副本替换原值，读的时候不需要同步，适用于写少读多的场合。

并发Set
       CopyOnWriteArraySet基于CopyOnWriteArrayList来实现的，只是在不允许存在重复的对象这个特性上遍历处理了一下。

并发Map
       ConcurrentHashMap是专用于高并发的Map实现，内部实现进行了锁分离，get操作是无锁的。

并发的Queue
       在并发队列上JDK提供了两套实现，一个是以ConcurrentLinkedQueue为代表的高性能队列，一个是以BlockingQueue接口为代表的阻塞队列。ConcurrentLinkedQueue适用于高并发场景下的队列，通过无锁的方式实现，通常ConcurrentLinkedQueue的性能要优于BlockingQueue。BlockingQueue的典型应用场景是生产者-消费者模式中，如果生产快于消费，生产队列装满时会阻塞，等待消费。

并发的Dueue
       Queue是一种双端队列，它允许在队列的头部和尾部进行出队和入队的操作。Dueue实现类有非线程安全的LinkedList、ArrayDueue和线程安全的LinkedBlockingDueue。LinkedBlockingDueue没有进行读写锁的分离，因此同一时间只能有一个线程对其操作，因此在高并发应用中，它的性能要远远低于LinkedBlockingQueue，更低于ConcurrentLinkedQueue。
 
并发锁重入锁ReentrantLock
       ReentrantLock是一种互斥锁的实现，就是一次最多只能一个线程拿到锁；

读写锁ReadWriteLock
       读写锁有读取和写入两种锁，读取锁允许多个读取的线程同时持有，而写入锁只能有一个线程持有。

条件Condition       
	调用Condition对象的相关方法，可以方便的挂起和唤醒线程。
ü 列举java的集合以及集合之间的继承关系

ü 集合类以及集合框架

ü 容器类介绍以及之间的区别（容器类估计很多人没听这个词，Java容器主要可以划分为4个部分：List列表、Set集合、Map映射、工具类（Iterator迭代器、Enumeration枚举类、Arrays和Collections），具体的可以看看这篇博文 Java容器类）
ü List,Set,Map的区别
Java集合大致可分为Set、List和Map三种体系，其中Set代表无序、不可重复的集合；List代表有序、重复的集合；而Map则代表具有映射关系的集合。Java 5之后，增加了Queue体系集合，代表一种队列集合实现。
ü List和Map的实现方式以及存储方式
ü HashMap的实现原理
简单来说，HashMap由数组+链表组成的，数组是HashMap的主体，链表则是主要为了解决哈希冲突而存在的，如果定位到的数组位置不含链表（当前entry的next指向null）,那么对于查找，添加等操作很快，仅需一次寻址即可；如果定位到的数组包含链表，对于添加操作，其时间复杂度为O(n)，首先遍历链表，存在即覆盖，否则新增；对于查找操作来讲，仍需遍历链表，然后通过key对象的equals方法逐一比对查找。所以，性能考虑，HashMap中的链表出现越少，性能才会越好。
HashMap是基于哈希表的Map接口的非同步实现，允许使用null值和null键，但不保证映射的顺序。
底层使用数组实现，数组中每一项是个单向链表，即数组和链表的结合体；当链表长度大于一定阈值时，链表转换为红黑树，这样减少链表查询时间。
HashMap在底层将key-value当成一个整体进行处理，这个整体就是一个Node对象。HashMap底层采用一个Node[]数组来保存所有的key-value对，当需要存储一个Node对象时，会根据key的hash算法来决定其在数组中的存储位置，在根据equals方法决定其在该数组位置上的链表中的存储位置；当需要取出一个Node时，也会根据key的hash算法找到其在数组中的存储位置，再根据equals方法从该位置上的链表中取出该Node。
HashMap进行数组扩容需要重新计算扩容后每个元素在数组中的位置，很耗性能
采用了Fail-Fast机制，通过一个modCount值记录修改次数，对HashMap内容的修改都将增加这个值。迭代器初始化过程中会将这个值赋给迭代器的expectedModCount，在迭代过程中，判断modCount跟expectedModCount是否相等，如果不相等就表示已经有其他线程修改了Map，马上抛出异常
原文：https://blog.csdn.net/xzp_12345/article/details/79251174 
ü HashMap数据结构？
ü HashMap源码理解
ü HashMap如何put数据（从HashMap源码角度讲解）？
ü HashMap怎么手写实现？
ü ConcurrentHashMap的实现原理
ü ArrayMap和HashMap的对比
ü HashTable实现原理
Hashtable是基于哈希表的Map接口的同步实现，不允许使用null值和null键
底层使用数组实现，数组中每一项是个单链表，即数组和链表的结合体
Hashtable在底层将key-value当成一个整体进行处理，这个整体就是一个Entry对象。Hashtable底层采用一个Entry[]数组来保存所有的key-value对，当需要存储一个Entry对象时，会根据key的hash算法来决定其在数组中的存储位置，在根据equals方法决定其在该数组位置上的链表中的存储位置；当需要取出一个Entry时，也会根据key的hash算法找到其在数组中的存储位置，再根据equals方法从该位置上的链表中取出该Entry。
synchronized是针对整张Hash表的，即每次锁住整张表让线程独占
原文：https://blog.csdn.net/xzp_12345/article/details/79251174 
ü TreeMap具体实现
ü HashMap和HashTable的区别
ü HashMap与HashSet的区别
ü HashSet与HashMap怎么判断集合元素重复？
ü 集合Set实现Hash怎么防止碰撞
弄清怎么个逻辑达到元素不重复的，源码先上 
HashSet 类中的add()方法：

public boolean add(E e) {
    return map.put(e, PRESENT)==null;
  }
1
2
3
类中map和PARENT的定义：

private transient HashMap<E,Object> map;
 // Dummy value to associate with an Object in the backing Map用来匹配Map中后面的对象的一个虚拟值
private static final Object PRESENT = new Object();
1
2
3
put()方法：

 public V put(K key, V value) {
        if (key == null)
            return putForNullKey(value);
        int hash = hash(key.hashCode());
        int i = indexFor(hash, table.length);
        for (Entry<K,V> e = table[i]; e != null; e = e.next) {
            Object k;
            if (e.hash == hash && ((k = e.key) == key || key.equals(k))) {
                V oldValue = e.value;
                e.value = value;
                e.recordAccess(this);
                return oldValue;
            }
        }
        modCount++;
        addEntry(hash, key, value, i);
        return null;
    }
可以看到for循环中，遍历table中的元素， 
1，如果hash码值不相同，说明是一个新元素，存；

如果没有元素和传入对象（也就是add的元素）的hash值相等，那么就认为这个元素在table中不存在，将其添加进table；

2（1），如果hash码值相同，且equles判断相等，说明元素已经存在，不存；

2（2），如果hash码值相同，且equles判断不相等，说明元素不存在，存；

如果有元素和传入对象的hash值相等，那么，继续进行equles()判断，如果仍然相等，那么就认为传入元素已经存在，不再添加，结束，否则仍然添加；

原文：https://blog.csdn.net/u010698072/article/details/52802179 

ü ArrayList和LinkedList的区别，以及应用场景
1、ArrayList是基于数组实现的，其构造函数为：
private transient Object[] elementData;
private int size;
ArryList初始化时，elementData数组大小默认为10；
每次add（）时，先调用ensureCapacity（）保证数组不会溢出，如果此时已满，会扩展为数组length的1.5倍+1，然后用array.copy的方法，将原数组拷贝到新的数组中；
ArrayList线程不安全，Vector方法是同步的，线程安全；
2、LinkedList是基于双链表实现的：
Object element;
Entry next,
          previous;
初始化时，有个header Entry，值为null；
使用header的优点是：在任何一个条目（包括第一个和最后一个）都有一个前置条目和一个后置条目，因此在LinkedList对象的开始或者末尾进行插入操作没有特殊的地方；
使用场景：
（1）如果应用程序对各个索引位置的元素进行大量的存取或删除操作，ArrayList对象要远优于LinkedList对象；
  ( 2 ) 如果应用程序主要是对列表进行循环，并且循环时候进行插入或者删除操作，LinkedList对象要远优于ArrayList对象；
原文：https://blog.csdn.net/sherry_rui/article/details/51068247 

ü 数组和链表的区别
1）存储位置上：
数组逻辑上相邻的元素在物理存储位置上也相邻，而链表不一定；
（2）存储空间上：
链表存放的内存空间可以是连续的，也可以是不连续的，数组则是连续的一段内存空间。一般情况下存放相同多的数
据数组占用较小的内存，而链表还需要存放其前驱和后继的空间。
（3）长度的可变性：
链表的长度是按实际需要可以伸缩的，而数组的长度是在定义时要给定的，如果存放的数据个数超过了数组的初始大
小，则会出现溢出现象。
（4）按序号查找时，数组可以随机访问，时间复杂度为O(1)，而链表不支持随机访问，平均需要O(n)；　
（5）按值查找时，若数组无序，数组和链表时间复杂度均为O(1)，但是当数组有序时，可以采用折半查找将时间复
杂度降为O(logn)；　
（6）插入和删除时，数组平均需要移动n/2个元素，而链表只需修改指针即可；　
（7）空间分配方面： 
数组在静态存储分配情形下，存储元素数量受限制，动态存储分配情形下，虽然存储空间可以扩充，但需要移动大量
元素，导致操作效率降低，而且如果内存中没有更大块连续存储空间将导致分配失败； 即数组从栈中分配空间,，对
于程序员方便快速,但自由度小。
链表存储的节点空间只在需要的时候申请分配，只要内存中有空间就可以分配，操作比较灵活高效；即链表从堆中分
配空间, 自由度大但申请管理比较麻烦。
原文：https://blog.csdn.net/Mormont/article/details/53439772 

ü 二叉树的深度优先遍历和广度优先遍历的具体实现
ü 堆的结构
利用完全二叉树的结构来维护一组数据，然后进行相关操作，一般的操作进行一次的时间复杂度在
　　O(1)~O(logn)之间
ü 堆和树的区别
ü 堆和栈在内存中的区别是什么(解答提示：可以从数据结构方面以及实际实现方面两个方面去回答)？
ü 什么是深拷贝和浅拷贝
ü 手写链表逆序代码
ü 讲一下对树，B+树的理解
ü 讲一下对图的理解
ü 判断单链表成环与否？
ü 链表翻转（即：翻转一个单项链表）
递归法
经历了很多面试，面试官最爱考察的算法无非是斐波那契数列和单链表反转，尽管是这些都是基础知识，然而我对单链表反转有更多的想法。 
递归法是我早期最爱在面试中使用的算法，很有逼格，写起来非常优雅，非常好理解。

先定义链表数据结构

static class Node {
    Integer data;
    Node next;
}

static Node readyNode() {
    Node linkNode1 = new Node();
    linkNode1.data = 1;
    Node linkNode2 = new Node();
    linkNode2.data = 2;
    Node linkNode3 = new Node();
    linkNode3.data = 3;
    Node linkNode4 = new Node();
    linkNode4.data = 4;
    Node linkNode5 = new Node();
    linkNode5.data = 5;
    Node linkNode6 = new Node();
    linkNode6.data = 6;
    linkNode1.next = linkNode2;
    linkNode2.next = linkNode3;
    linkNode3.next = linkNode4;
    linkNode4.next = linkNode5;
    linkNode5.next = linkNode6;
    return linkNode1;
}
如上代码所示 


递归法会逐层确定该节点有没有next节点，若为空，则认定递归到最深层元素。同时将该层节点的next指向父节点，在递归栈中以此类推。

static Node reverseLinkedList(Node node) {
    if (node == null || node.next == null) {
        return node;
    } else {
        Node headNode = reverseLinkedList(node.next);
        node.next.next = node;
        node.next = null;
        return headNode;
    }
}

上图展示了递归后的效果。 
如果注释掉第7行，会发生如上图所示的1、2号节点闭环问题。由于1号节点的next没有置空，依旧指向2号节点，所以遍历时候肯定存在环。



遍历法

static Node reverseLinkedList(Node node) {
    Node previousNode = null;
    Node currentNode = node;
    Node headNode = null;
    while (currentNode != null) {
        Node nextNode = currentNode.next;
        if (nextNode == null) {
            headNode = currentNode;
        }
        currentNode.next = previousNode;
        previousNode = currentNode;
        currentNode = nextNode;
    }
    return headNode;
}
LinkedList的反转

LinkedList没有提供反转链表的相关函数，以下是通过foreach实现链表反转

static LinkedList reverseLinkedList(LinkedList linkedList) {
    LinkedList<Object> newLinkedList = new LinkedList<>();
    for (Object object : linkedList) {
        newLinkedList.add(0, object);
    }
    return newLinkedList;
}
--------------------- 
原文：https://blog.csdn.net/acquaintanceship/article/details/73011169 

ü 合并多个单有序链表（假设都是递增的）
 
（四） 线程、多线程和线程池
 
ü 开启线程的三种方式？
 创建线程的方式：
                   1.继承Thread类，并复写run方法，创建该类对象，调用start方法开启线程。
                   2.实现Runnable接口，复写run方法，创建Thread类对象，将Runnable子类对象传递给Thread类对象。调用start方法开启线程。
                   第二种方式好，将线程对象和线程任务对象分离开。降低了耦合性，利于维护    
                   3.创建FutureTask对象，创建Callable子类对象，复写call(相当于run)方法，将其传递给FutureTask对象（相当于一个Runnable）。
                     创建Thread类对象，将FutureTask对象传递给Thread对象。调用start方法开启线程。这种方式可以获得线程执行完之后的返回值。
第三种使用Runnable功能更加强大的一个子类.这个子类是具有返回值类型的任务方法.
第一种和第二种两种方式是run()方法运行完是没有返回值的.
ü 线程和进程的区别？
根本区别：进程是操作系统资源分配的基本单位，而线程是任务调度和执行的基本单位
ü 为什么要有线程，而不是仅仅用进程？
在开销方面：每个进程都有独立的代码和数据空间（程序上下文），程序之间的切换会有较大的开销；线程可以看做轻量级的进程，同一类线程共享代码和数据空间，每个线程都有自己独立的运行栈和程序计数器（PC），线程之间切换的开销小。
所处环境：在操作系统中能同时运行多个进程（程序）；而在同一个进程（程序）中有多个线程同时执行（通过CPU调度，在每个时间片中只有一个线程执行）
内存分配方面：系统在运行的时候会为每个进程分配不同的内存空间；而对线程而言，除了CPU外，系统不会为线程分配内存（线程所使用的资源来自其所属进程的资源），线程组之间只能共享资源。
包含关系：没有线程的进程可以看做是单线程的，如果一个进程内有多个线程，则执行过程不是一条线的，而是多条线（线程）共同完成的；线程是进程的一部分，所以线程也被称为轻权进程或者轻量级进程。
原文：https://blog.csdn.net/kuangsonghan/article/details/80674777 
ü run()和start()方法区别
在main方法中执行的run()方法不会创建新的线程，而在main方法中执行的start()方法会启动一个新的线程，新的线程会调用run方法
run方法可以多次执行，但是start方法不允许多次执行，多次执行start()方法会抛出一个一个运行时异常java.lang.IllegalThreadStateException
原文：https://blog.csdn.net/tianmlin1/article/details/79054304 
ü 如何控制某个方法允许并发访问线程的个数？
ü 在Java中wait和seelp方法的不同；
ü 谈谈wait/notify关键字的理解
ü 什么导致线程阻塞？
ü 线程如何关闭？
ü 讲一下java中的同步的方法
ü 数据一致性如何保证？
ü 如何保证线程安全？
ü 如何实现线程同步？
ü 两个进程同时要求写或者读，能不能实现？如何防止进程的同步？
ü 线程间操作List
ü Java中对象的生命周期
ü Synchronized用法
ü synchronize的原理
ü 谈谈对Synchronized关键字，类锁，方法锁，重入锁的理解
ü static synchronized 方法的多线程访问和作用
ü 同一个类里面两个synchronized方法，两个线程同时访问的问题
ü volatile的原理
ü 谈谈volatile关键字的用法
ü 谈谈volatile关键字的作用
ü 谈谈NIO的理解
ü synchronized 和volatile 关键字的区别
ü synchronized与Lock的区别
ü ReentrantLock 、synchronized和volatile比较
ü ReentrantLock的内部实现
ü lock原理
ü 死锁的四个必要条件？
ü 怎么避免死锁？
ü 对象锁和类锁是否会互相影响？
ü 什么是线程池，如何使用?
ü Java的并发、多线程、线程模型
ü 谈谈对多线程的理解
ü 多线程有什么要注意的问题？
ü 谈谈你对并发编程的理解并举例说明
ü 谈谈你对多线程同步机制的理解？
ü 如何保证多线程读写文件的安全？
ü 多线程断点续传原理
ü 断点续传的实现
 
（五）并发编程有关知识点（这个是一般Android开发用的少的，所以建议多去看看）：
 
平时Android开发中对并发编程可以做得比较少，Thread这个类经常会用到，但是我们想提升自己的话，一定不能停留在表面，,我们也应该去了解一下java的关于线程相关的源码级别的东西。
可以多去看一下文献，研究和学习一下相关技术点。
 
 
二、Android面试题
 
Android面试题包括Android基础，还有一些源码级别的、原理这些等。所以想去大公司面试，一定要多看看源码和实现方式，常用框架可以试试自己能不能手写实现一下，锻炼一下自己。
 
（一）Android基础知识点
 
ü 四大组件是什么
Android四大基本组件分别是Activity，Service服务,Content Provider内容提供者，BroadcastReceiver广播接收器。
Activity :
应用程序中，一个Activity通常就是一个单独的屏幕，它上面可以显示一些控件也可以监听并处理用户的事件做出响应。
BroadcastReceive广播接收器:
你的应用可以使用它对外部事件进行过滤只对感兴趣的外部事件(如当电话呼入时，或者数据网络可用时)进行接收并做出响应。广播接收器没有用户界面。然而，它们可以启动一个activity或serice 来响应它们收到的信息，或者用NotificationManager 来通知用户。
Service 服务:
一个Service 是一段长生命周期的，没有用户界面的程序，可以用来开发如监控类程序。
android平台提供了Content Provider使一个应用程序的指定数据集提供给其他应用程序。这些数据可以存储在文件系统中、在一个SQLite数据库、或以任何其他合理的方式,
Content Provider内容提供者 :
其他应用可以通过ContentResolver类(见ContentProviderAccessApp例子)从该内容提供者中获取或存入数据.(相当于在应用外包了一层壳),
只有需要在多个应用程序间共享数据是才需要内容提供者。例如，通讯录数据被多个应用程序使用，且必须存储在一个内容提供者中
它的好处:统一数据访问方式。
ü 四大组件的生命周期和简单用法

BroadcastReceive广播接收器生命周期：
生命周期只有十秒左右，如果在 onReceive() 内做超过十秒内的事情，就会报ANR(Application No Response) 程序无响应的错误信息
它的生命周期为从回调onReceive()方法开始到该方法返回结果后结束


ü Activity之间的通信方式
Intent
借助类的静态变量
借助全局变量/Application
借助外部工具 
– 借助SharedPreference 
– 使用Android数据库SQLite 
– 赤裸裸的使用File 
– Android剪切板
借助Service
ü Activity各种情况下的生命周期
启动Activity: onCreate()—>onStart()—>onResume()，Activity进入运行状态。
Activity退居后台: 当前Activity转到新的Activity界面或按Home键回到主屏： onPause()—>onStop()，进入停滞状态。
Activity返回前台: onRestart()—>onStart()—>onResume()，再次回到运行状态。
Activity退居后台，且系统内存不足， 系统会杀死这个后台状态的Activity（此时这个Activity引用仍然处在任务栈中，只是这个时候引用指向的对象已经为null），若再次回到这个Activity,则会走onCreate()–>onStart()—>onResume()(将重新走一次Activity的初始化生命周期)
锁屏：onPause()->onStop()
解锁：onStart()->onResume()



ü 横竖屏切换的时候，Activity 各种情况下的生命周期
1、不设置Activity的android:configChanges时，切屏会重新调用各个生命周期，切横屏时会执行一次，切竖屏时会执行两次
2、设置Activity的android:configChanges="orientation"时，切屏还是会重新调用各个生命周期，切横、竖屏时只会执行一次
3、设置Activity的android:configChanges="orientation|keyboardHidden"时，切屏不会重新调用各个生命周期，只会执行onConfigurationChanged方法
ü Activity与Fragment之间生命周期比较

ü Activity上有Dialog的时候按Home键时的生命周期
当前Activity产生事件弹出Toast和AlertDialog的时候Activity的生命周期不会有改变
Activity运行时按下HOME键(跟被完全覆盖是一样的)：onSaveInstanceState --> onPause --> onStop，再次进入激活状态时： onRestart -->onStart--->onResume
ü 两个Activity 之间跳转时必然会执行的是哪几个方法？
ü 前台切换到后台，然后再回到前台，Activity生命周期回调方法。弹出Dialog，生命值周期回调方法。
ü Activity的四种启动模式对比
一、standard模式
    特点：1.Activity的默认启动模式
              2.每启动一个Activity就会在栈顶创建一个新的实例。例如：闹钟程序
    缺点：当Activity已经位于栈顶时，而再次启动Activity时还需要在创建一个新的实例，不能直接复用。
二、singleTop模式
    特点：该模式会判断要启动的Activity实例是否位于栈顶，如果位于栈顶直接复用，否则创建新的实例。 例如：浏览器的书签
    缺点：如果Activity并未处于栈顶位置，则可能还会创建多个实例。
三、singleTask模式
    特点：使Activity在整个应用程序中只有一个实例。每次启动Activity时系统首先检查栈中是否存在当前Activity实例，如果存在
              则直接复用，并把当前Activity之上所有实例全部出栈。例如：浏览器主界面
四、singleInstance模式
    特点：该模式的Activity会启动一个新的任务栈来管理Activity实例，并且该势力在整个系统中只有一个。无论从那个任务栈中    启动该Activity，都会是该Activity所在的任务栈转移到前台，从而使Activity显示。主要作用是为了在不同程序中共享一个Activity
        实例。
回调onNewIntent（）方法
原文：https://blog.csdn.net/qq_38217237/article/details/79038505 

ü Activity状态保存与恢复
如果我们希望保存更多临时的信息，而这些信息又没有必要写入到持久化的存储当中，这时候我们应该重写onSaveInstanceState方法，在该回调当中会传入一个Bundle对象，只需要把保存的信息放到里面，之后再在onRestoreInstanceState和onCreate方法中把它读取出来就可以了，这里面有两点需要注意的：
onRestoreInstance只有在Bundle不为空时才会回调，而在onCreate方法当中是通过判空操作来判断是否有需要恢复的状态的。
在重写onRestoreInstanceState方法时，应当先调用super方法，这样由系统负责保存的部分才能够恢复。

ü fragment各种情况下的生命周期
相比于Activity的生命周期多了如下几个方法
onAttach()：当Fragment与Activity发生关联时，该方法被调用
onCreateView()：创建Fragment的视图
onActivityCreate()：当Activity的onCreate()返回时被调用
onDestoryView()：与onCreateView()是对应的，当Fragment的视图被销毁时，该方法被调用
onDetach()： 与onAttach() 方法相对应，当Fragment与Activity的关联被取消时，该方法被调用
tivity中调用replace()方法时的生命周期
新替换的Fragment：onAttach > onCreate > onCreateView > onViewCreated > onActivityCreated > onStart > onResume
被替换的Fragment：onPause > onStop > onDestroyView > onDestroy > onDetach
Activity中调用replace()方法和addToBackStack()方法时的生命周期
新替换的Fragment（没有在BackStack中）：onAttach > onCreate > onCreateView > onViewCreated > onActivityCreated > onStart > onResume
新替换的Fragment（已经在BackStack中）：onCreateView > onViewCreated > onActivityCreated > onStart > onResume
被替换的Fragment：onPause > onStop > onDestroyView
Fragment在运行状态后跟随Activity的生命周期
Fragment在上述的各种情况下进入了onResume后，则进入了运行状态，以下4个生命周期方法将跟随所属的Activity一起被调用：
onPause > onStop > onStart > onResume
ü Fragment状态保存startActivityForResult是哪个类的方法，在什么情况下使用？*----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
ü 如何实现Fragment的滑动？
ü fragment之间传递数据的方式？
ü Activity 怎么和Service 绑定？
ü 怎么在Activity 中启动自己对应的Service？
ü service和activity怎么进行数据交互？
ü Service的开启方式
ü 请描述一下Service 的生命周期
ü 谈谈你对ContentProvider的理解
ü 说说ContentProvider、ContentResolver、ContentObserver 之间的关系
ü 请描述一下广播BroadcastReceiver的理解
ü 广播的分类
ü 广播使用的方式和场景
ü 在manifest 和代码中如何注册和使用BroadcastReceiver?
ü 本地广播和全局广播有什么差别？
ü BroadcastReceiver，LocalBroadcastReceiver 区别
ü AlertDialog,popupWindow,Activity区别
ü Application 和 Activity 的 Context 对象的区别
ü Android属性动画特性
ü 如何导入外部数据库?
ü LinearLayout、RelativeLayout、FrameLayout的特性及对比，并介绍使用场景。
ü 谈谈对接口与回调的理解
ü 回调的原理
ü 写一个回调demo
ü 介绍下SurfView
ü RecycleView的使用
ü 序列化的作用，以及Android两种序列化的区别
ü 差值器
ü 估值器
ü Android中数据存储方式
 
（二）Android源码相关分析
 
ü Android动画框架实现原理
ü Android各个版本API的区别
ü Requestlayout，onlayout，onDraw，DrawChild区别与联系
ü invalidate和postInvalidate的区别及使用
ü Activity-Window-View三者的差别
ü 谈谈对Volley的理解
ü 如何优化自定义View
ü 低版本SDK如何实现高版本api？
ü 描述一次网络请求的流程
ü HttpUrlConnection 和 okhttp关系
ü Bitmap对象的理解
ü looper架构
ü ActivityThread，AMS，WMS的工作原理
ü 自定义View如何考虑机型适配
ü 自定义View的事件
ü AstncTask+HttpClient 与 AsyncHttpClient有什么区别？
ü LaunchMode应用场景
ü AsyncTask 如何使用?
ü SpareArray原理
ü 请介绍下ContentProvider 是如何实现数据共享的？
ü AndroidService与Activity之间通信的几种方式
ü IntentService原理及作用是什么？
ü 说说Activity、Intent、Service 是什么关系
ü ApplicationContext和ActivityContext的区别
ü SP是进程同步的吗?有什么方法做到同步？
ü 谈谈多线程在Android中的使用
ü 进程和 Application 的生命周期
ü 封装View的时候怎么知道view的大小
ü RecycleView原理
ü AndroidManifest的作用与理解
 
（三）常见的一些原理性问题
 
ü Handler机制和底层实现
ü Handler、Thread和HandlerThread的差别
ü handler发消息给子线程，looper怎么启动？
ü 关于Handler，在任何地方new Handler 都是什么线程下?
ü ThreadLocal原理，实现及如何保证Local属性？
ü 请解释下在单线程模型中Message、Handler、Message Queue、Looper之间的关系
ü 请描述一下View事件传递分发机制
ü Touch事件传递流程
ü 事件分发中的onTouch 和onTouchEvent 有什么区别，又该如何使用？
ü View和ViewGroup分别有哪些事件分发相关的回调方法
ü View刷新机制
ü View绘制流程
ü 自定义控件原理
ü 自定义View如何提供获取View属性的接口？
ü Android代码中实现WAP方式联网
ü AsyncTask机制
ü AsyncTask原理及不足
ü 如何取消AsyncTask？
ü 为什么不能在子线程更新UI？
ü ANR产生的原因是什么？
ü ANR定位和修正
ü oom是什么？
ü 什么情况导致oom？
ü 有什么解决方法可以避免OOM？
ü Oom 是否可以try catch？为什么？
ü 内存泄漏是什么？
ü 什么情况导致内存泄漏？
ü 如何防止线程的内存泄漏？
ü 内存泄露场的解决方法
ü 内存泄漏和内存溢出区别？
ü LruCache默认缓存大小
ü ContentProvider的权限管理(解答：读写分离，权限控制-精确到表级，URL控制)
ü 如何通过广播拦截和abort一条短信？
ü 广播是否可以请求网络？
ü 广播引起anr的时间限制是多少？
ü 计算一个view的嵌套层级
ü Activity栈
ü Android线程有没有上限？
ü 线程池有没有上限？
ü ListView重用的是什么？
ü Android为什么引入Parcelable？
ü 有没有尝试简化Parcelable的使用？
 
（四）开发中常见的一些问题
 
ü ListView 中图片错位的问题是如何产生的?
ü 混合开发有了解吗？
ü 知道哪些混合开发的方式？说出它们的优缺点和各自使用场景？（解答：比如:RN，weex，H5，小程序，WPA等。做Android的了解一些前端js等还是很有好处的)
ü 屏幕适配的处理技巧都有哪些?
ü 服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达？
ü 动态布局的理解
ü 怎么去除重复代码？
ü 画出 Android 的大体架构图
ü Recycleview和ListView的区别
ü ListView图片加载错乱的原理和解决方案
ü 动态权限适配方案，权限组的概念
ü Android系统为什么会设计ContentProvider？
ü 下拉状态栏是不是影响activity的生命周期
ü 如果在onStop的时候做了网络请求，onResume的时候怎么恢复？
ü Bitmap 使用时候注意什么？
ü Bitmap的recycler()
ü Android中开启摄像头的主要步骤
ü ViewPager使用细节，如何设置成每次只初始化当前的Fragment，其他的不初始化？
ü 点击事件被拦截，但是想传到下面的View，如何操作？
ü 微信主页面的实现方式
ü 微信上消息小红点的原理
ü CAS介绍（这是阿里巴巴的面试题，我不是很了解，可以参考博客: CAS简介）
 
 
三、混合开发面试题
 
大厂除了技术深度之外，还要求你具备一些广度的知识，比如你要会前端知识，会混合开发，至少会一种脚本语言，C c++更不用说了，也是必会的。
 
ü Hybrid做过吗？
ü Hybrid通信原理是什么，有做研究吗？
ü react native有多少了解？讲一下原理。
ü weex了解吗？如何自己实现类似技术？
ü flutter了解吗？内部是如何实现跨平台的？
ü Dart语言有研究贵吗？
ü 快应用了解吗？跟其她方式相比有什么优缺点？
ü 说说你用过的混合开发技术有哪些？各有什么优缺点？
ü Python会吗？
ü 会不会PHP？
ü Gradle了解多少？groovy语法会吗？
 
 
四、高端技术面试题
 
这里讲的是大公司需要用到的一些高端Android技术，这里专门整理了一个文档，希望大家都可以看看。这些题目有点技术含量，需要好点时间去研究一下的。
 
（一）图片
 
ü 图片库对比
ü 图片库的源码分析
ü 图片框架缓存实现
ü LRUCache原理
LruCache中维护了一个集合LinkedHashMap，该LinkedHashMap是以访问顺序排序的。当调用put()方法时，就会在结合中添加元素，并调用trimToSize()判断缓存是否已满，如果满了就用LinkedHashMap的迭代器删除队尾元素，即近期最少访问的元素。当调用get()方法访问缓存对象时，就会调用LinkedHashMap的get()方法获得对应集合元素，同时会更新该元素到队头。
链接：https://www.jianshu.com/p/b49a111147ee
ü 图片加载原理
首次加载 Android App 时，肯定要通过网络交互来获取图片，之后我们可以将图片保存至本地SD卡和内存中
之后运行 App 时，优先访问内存中的图片缓存，若内存中没有，则加载本地SD卡中的图片
总之，只在初次访问新内容时，才通过网络获取图片资源
ü 自己去实现图片库，怎么做？
ü Glide源码解析
ü Glide使用什么缓存？
ü Glide内存缓存如何控制大小？
 
（二）网络和安全机制
 
ü 网络框架对比和源码分析
ü 自己去设计网络请求框架，怎么做？
ü okhttp源码
ü 网络请求缓存处理，okhttp如何处理网络缓存的
ü 从网络加载一个10M的图片，说下注意事项
ü TCP的3次握手和四次挥手
ü TCP与UDP的区别
ü TCP与UDP的应用
ü HTTP协议
ü HTTP1.0与2.0的区别
ü HTTP报文结构
ü HTTP与HTTPS的区别以及如何实现安全性
ü 如何验证证书的合法性?
ü https中哪里用了对称加密，哪里用了非对称加密，对加密算法（如RSA）等是否有了解?
ü client如何确定自己发送的消息被server收到?
ü 谈谈你对WebSocket的理解
ü WebSocket与socket的区别
ü 谈谈你对安卓签名的理解。
ü 请解释安卓为啥要加签名机制?
ü 视频加密传输
ü App 是如何沙箱化，为什么要这么做？
ü 权限管理系统（底层的权限是如何进行 grant 的）？
 
（三）数据库
 
ü sqlite升级，增加字段的语句
ü 数据库框架对比和源码分析
ü 数据库的优化
ü 数据库数据迁移问题
 
（四）算法
 
ü 排序算法有哪些？
ü 最快的排序算法是哪个？
ü 手写一个冒泡排序
ü 手写快速排序代码
ü 快速排序的过程、时间复杂度、空间复杂度
ü 手写堆排序
ü 堆排序过程、时间复杂度及空间复杂度
ü 写出你所知道的排序算法及时空复杂度，稳定性
https://www.cnblogs.com/zhaoshuai1215/p/3448154.html
ü 二叉树给出根节点和目标节点，找出从根节点到目标节点的路径
ü 给阿里2万多名员工按年龄排序应该选择哪个算法？
ü GC算法(各种算法的优缺点以及应用场景)
ü 蚁群算法与蒙特卡洛算法
ü 子串包含问题(KMP 算法)写代码实现
ü 一个无序，不重复数组，输出N个元素，使得N个元素的和相加为M，给出时间复杂度、空间复杂度。手写算法
ü 万亿级别的两个URL文件A和B，如何求出A和B的差集C(提示：Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优化)
ü 百度POI中如何试下查找最近的商家功能(提示：坐标镜像+R树)。
ü 两个不重复的数组集合中，求共同的元素。
ü 两个不重复的数组集合中，这两个集合都是海量数据，内存中放不下，怎么求共同的元素？
ü 一个文件中有100万个整数，由空格分开，在程序中判断用户输入的整数是否在此文件中。说出最优的方法
ü 一张Bitmap所占内存以及内存占用的计算
https://blog.csdn.net/tz_zs/article/details/72954107
ü 2000万个整数，找出第五十大的数字？
ü 烧一根不均匀的绳，从头烧到尾总共需要1个小时。现在有若干条材质相同的绳子，问如何用烧绳的方法来计时一个小时十五分钟呢？
ü 求1000以内的水仙花数以及40亿以内的水仙花数
ü 5枚硬币，2正3反如何划分为两堆然后通过翻转让两堆中正面向上的硬8币和反面向上的硬币个数相同
ü 时针走一圈，时针分针重合几次
ü N*N的方格纸,里面有多少个正方形
ü x个苹果，一天只能吃一个、两个、或者三个，问多少天可以吃完？
 
（五）插件化、模块化、组件化、热修复、增量更新、Gradle
 
ü 对热修复和插件化的理解
ü 插件化原理分析
ü 模块化实现（好处，原因）
ü 热修复,插件化
ü 项目组件化的理解
ü 描述清点击 Android Studio 的 build 按钮后发生了什么
 
（六）架构设计和设计模式
 
ü 谈谈你对Android设计模式的理解
https://www.cnblogs.com/android-blogs/p/5530239.html
ü MVC MVP MVVM原理和区别
https://blog.csdn.net/victoryzn/article/details/78392128
ü 你所知道的设计模式有哪些？
ü 项目中常用的设计模式
ü 手写生产者/消费者模式
http://www.importnew.com/27063.html
ü 写出观察者模式的代码
//观察者
interface  Observer{
    void  update(String msg);
}
static class  WxUser implements  Observer{
    public WxUser(String name) {
        this.name = name;
    }
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    private  String name;

    @Override
    public void update(String msg) {
        System.out.println(name+msg);
    }
}
//被观察者
interface  Observable{
    void attach(Observer observer);
    void detach(Observer observer);
    void notfiy(String msg);
}
static class VxSubcr implements  Observable
{
    private ArrayList<Observer> list =new ArrayList<>();
    @Override
    public void attach(Observer observer) {
        list.add(observer);
    }

    @Override
    public void detach(Observer observer) {
        list.remove(observer);
    }
    @Override
    public void notfiy(String msg) {
        for (Observer observer :list){
            observer.update(msg);
        }
    }
}
public static void main(String[] args){

    WxUser user=new WxUser("zhangsan");
    WxUser user1=new WxUser("lisi");
    VxSubcr subcr=new VxSubcr();
    subcr.attach(user);
    subcr.attach(user1);
    subcr.notfiy("发布了消息");
}
ü 适配器模式，装饰者模式，外观模式的异同？
ü 用到的一些开源框架，介绍一个看过源码的，内部实现过程。
ü 谈谈对RxJava的理解
ü RxJava的功能与原理实现
ü RxJava的作用，与平时使用的异步操作来比的优缺点
ü 说说EventBus作用，实现方式，代替EventBus的方式
ü 从0设计一款App整体架构，如何去做？
ü 说一款你认为当前比较火的应用并设计(比如：直播APP，P2P金融，小视频等)
ü 谈谈对java状态机理解
ü Fragment如果在Adapter中使用应该如何解耦？
ü Binder机制及底层实现
ü 对于应用更新这块是如何做的？(解答：灰度，强制更新，分区域更新)？
ü 实现一个Json解析器(可以通过正则提高速度)
ü 统计启动时长,标准
 
（七）性能优化
 
ü 如何对Android 应用进行性能分析以及优化?
ü ddms 和 traceView
ü 性能优化如何分析systrace？
ü 用IDE如何分析内存泄漏？
ü Java多线程引发的性能问题，怎么解决？
ü 启动页白屏及黑屏解决？
ü 启动太慢怎么解决？
ü 怎么保证应用启动不卡顿？
ü App启动崩溃异常捕捉
ü 自定义View注意事项
ü 现在下载速度很慢,试从网络协议的角度分析原因,并优化(提示：网络的5层都可以涉及)。
ü Https请求慢的解决办法（提示：DNS，携带数据，直接访问IP）
ü 如何保持应用的稳定性
ü RecyclerView和ListView的性能对比
ü ListView的优化
ü RecycleView优化
ü View渲染
ü Bitmap如何处理大图，如一张30M的大图，如何预防OOM
ü java中的四种引用的区别以及使用场景
ü 强引用置为null，会不会被回收？
 毫无意义，仅是改变了引用，并起不到实际意义，很有可能会被编译器优化掉
是否gc一个对象，取决于根节点是否可达。
（八）NDK、jni、Binder、AIDL、进程通信有关
 
ü 请介绍一下NDK
ü 什么是NDK库?
ü jni用过吗？
ü 如何在jni中注册native函数，有几种注册方式?
ü Java如何调用c、c++语言？
ü jni如何调用java层代码？
ü 进程间通信的方式？
ü Binder机制
ü 简述IPC？
ü 什么是AIDL？
ü AIDL解决了什么问题？
ü AIDL如何使用？
ü Android 上的 Inter-Process-Communication 跨进程通信时如何工作的？
ü 多进程场景遇见过么？
ü Android进程分类？
ü 进程和 Application 的生命周期？
ü 进程调度
ü 谈谈对进程共享和线程安全的认识
ü 谈谈对多进程开发的理解以及多进程应用场景
ü 什么是协程？
 
（九）framework层、ROM定制、Ubuntu、Linux之类的问题
 
ü java虚拟机的特性
ü 谈谈对jvm的理解
ü JVM内存区域，开线程影响哪块内存
ü 对Dalvik、ART虚拟机有什么了解？
ü Art和Dalvik对比
ü 虚拟机原理，如何自己设计一个虚拟机(内存管理，类加载，双亲委派)
ü 谈谈你对双亲委派模型理解
ü JVM内存模型，内存区域
ü 类加载机制
ü 谈谈对ClassLoader(类加载器)的理解
ü 谈谈对动态加载（OSGI）的理解
ü 内存对象的循环引用及避免
ü 内存回收机制、GC回收策略、GC原理时机以及GC对象
ü 垃圾回收机制与调用System.gc()区别
ü Ubuntu编译安卓系统
ü 系统启动流程是什么？（提示：Zygote进程 –> SystemServer进程 –> 各种系统服务 –> 应用进程）
ü 大体说清一个应用程序安装到手机上时发生了什么
ü 简述Activity启动全部过程
ü App启动流程，从点击桌面开始
ü 逻辑地址与物理地址，为什么使用逻辑地址？
ü Android为每个应用程序分配的内存大小是多少？
ü Android中进程内存的分配，能不能自己分配定额内存？
ü 进程保活的方式
ü 如何保证一个后台服务不被杀死？（相同问题：如何保证service在后台不被kill？）比较省电的方式是什么？
ü App中唤醒其他进程的实现方式
 
 
五、非技术性问题&HR问题汇总
 
这里整理的是一些与技术没有直接关系的面试题，但是能够考察你的综合水平，所以不要以为不是技术问题，就不看，往往有时候就是这样一些细节的题目被忽视，而错过了一次次面试机会。
 
（一）非技术问题
 
ü 介绍你做过的哪些项目
ü 都使用过哪些框架、平台？
ü 都使用过哪些自定义控件？
ü 研究比较深入的领域有哪些？
ü 对业内信息的关注渠道有哪些？
ü 最近都读哪些书？
ü 有没有什么开源项目？
ü 自己最擅长的技术点，最感兴趣的技术领域和技术点
ü 项目中用了哪些开源库，如何避免因为引入开源库而导致的安全性和稳定性问题
ü 实习过程中做了什么，有什么产出？
 
（二）HR提出的面试问题
 
ü 您在前一家公司的离职原因是什么？
ü 讲一件你印象最深的一件事情
ü 介绍一个你影响最深的项目
ü 介绍你最热爱最擅长的专业领域
ü 公司实习最大的收获是什么？
ü 与上级意见不一致时，你将怎么办？
ü 自己的优点和缺点是什么？并举例说明？
ü 你的学习方法是什么样的？实习过程中如何学习？实习项目中遇到的最大困难是什么以及如何解决的？
ü 说一件最能证明你能力的事情
ü 针对你你申请的这个职位，你认为你还欠缺什么
ü 如果通过这次面试我们单位录用了你，但工作一段时间却发现你根本不适合这个职位，你怎么办？
ü 项目中遇到最大的困难是什么？如何解决的？
ü 你的职业规划以及个人目标、未来发展路线及求职定位
ü 如果你在这次面试中没有被录用，你怎么打算？
ü 评价下自己，评价下自己的技术水平，个人代码量如何？
ü 通过哪些渠道了解的招聘信息，其他同学都投了哪些公司？
ü 业余都有哪些爱好？
ü 你做过的哪件事最令自己感到骄傲？
ü 假如你晚上要去送一个出国的同学去机场，可单位临时有事非你办不可，你怎么办？
ü 就你申请的这个职位，你认为你还欠缺什么？
ü 当前的offer状况；如果BATH都给了offer该如何选？
ü 你对一份工作更看重哪些方面？平台，技术，氛围，城市，还是money？
ü 理想薪资范围；杭州岗和北京岗选哪个？
ü 理想中的工作环境是什么？
ü 谈谈你对跳槽的看法
ü 说说你对行业、技术发展趋势的看法
ü 实习过程中周围同事/同学有哪些值得学习的地方？
ü 家人对你的工作期望及自己的工作期望
ü 如果你的工作出现失误，给本公司造成经济损失，你认为该怎么办？
ü 若上司在公开会议上误会你了，该如何解决？
ü 是否可以实习，可以实习多久？
ü 在五年的时间内，你的职业规划
ü 你看中公司的什么？或者公司的那些方面最吸引你？
 
 
 
