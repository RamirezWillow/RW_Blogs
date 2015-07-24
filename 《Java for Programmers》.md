> 面向对象分析与设计（Object-Oriented Alaysis and Dessign.OOAD）  
统一建模语言（Unified Modeling Language.UML）  
程序编程接口（Application Programming Interface.API）  
集成开发环境（Integrated Development Environment.IDE）  
虚拟机（Virtual Machine.VM）  
即时（Just-In-Time.JIT）  
创建执行步骤：edit（编辑）——compile（编译）——load（加载）——verify（验证）——execute（执行）  
统一资源定位标示符（URI，Uniform Resource Identifier）  
统一资源定位器（URL，Uniform Resource Locators）  

---


###收集：
1. System.out.printf显示多行  
System.out.printf("%s\n%s\n","A","B");  
输出：  
A  
B  
2. 在一条声明语句中声明同一种类型的多个变量，变量名称之间用逗号分开（即变量名的逗号分隔列表），  
例：  
int a,    //first number to add  
     b,    //second number to add  
     sum;    //sum of a and b  
3. 美式计数法（分组分隔符）  
例：  
double s = 164132165.84631;  
            System. out.printf("s = %,.3f" ,s);  
输出：  
s = 164,132,165.846  
4. &和|、&&和||用法一样，只是前者不执行短路求值，对于运算符右操作数有所需要的辅助效果（side effect）——修改变量的值，则逻辑与和逻辑或非常有用【联系：好2】  
5. Math类的几个方法:  
> |方法|描述|
|---|---|
|asb(x)|x的绝对值|
|ceil(x)|将x四舍五入为不小于x的最小整数|
|cos(x)|x的三角余弦值（x为弧度）|
|exp(x)|指数方法e^x|
|floor(x)|将x四舍五入为不大于x的最大整数|
|log(x)|x的自然对数（自然对数的底数为e）|
|max(x,y)|x与y的较大值|
|min(x,y)|x与y的较小值|
|pow(x,y)|x的y次幂|
|sin(x)|x的三角正弦值（x为弧度）|
|spot(x)|x的平方根|
|tan(x)|x的三角正切值（x为弧度）|  
|PI|π保留15位小数的近似值|
|E|自然对数e保留15位小数的近似值|  


6. 将main声明为静态的，使JVM不用创建该类的实例就能够使用main的方法
7. 都用方法的方式：  
①使用方法名的本身，调用同一个类中的一个方法。  
②使用包含对象的引用的变量，后接一个点号和方法名称  
③使用类名称和一个点号来调用类的静态方法  
8. 静态方法只能直接调用一个类型的其他静态方法（即使用方法名称本身），并且只能直接操作同一个类型的静态变量。为了访问类的非静态成员，静态方法必须使用该类的对象的引用
9. 实参提升（argument promotion）——将实参值（在可能的情况下）转换成方法在其对应参数中希望接收的类型，其适用于包含两个或多个基本类型值的表达式，也可以适用于作为作为实参传递的方法的基本类型值  
> | 类型 | 有效的提升 |
| ----- | ----------- |
|double|无|  
|float|double|
|long|float/doule|
|int|long/float/double|
|char|int/long/float/double|
|short|int/long/float/double| 
|byte|short/int/long/float/double|
|boolean|无|  


10. Java不允许将int值与枚举常量作比较
11. 基本的作用于规则如下：  
①参数声明的作用域是声明所在的方法体  
②局部变量声明的作用域从声明点开始，到声明所在的语句块结束为此  
③for语句首部初始化部分出现的局部变量声明的作用域，是for语句体和首部中的其他表达式  
④类的犯法或字段的作用域，为整个类体。这就使类的非晶态方法可以使用类的字段和其他昂发  
12. 方法重载：常用于创几个名称相同的方法，它们执行相同或者相似的任务，但使用不同类型或不同个数实参。  
例：Math方法abs，min和max中的每一个都有四个重载的版本  
①一个版本带两个double参数  
②一个版本带两个float参数  
③一个版本带两个int参数  
④一个版本带两个long参数  
13. 强化for语句【for(int number:array){sum+=number;}】：  
a.简化了迭代遍历数组的代码，其只能获取不能修改。  
b.只要不要求访问当前数组的索引值，就可以用强化for语句代替计数器控制for语句  
14. ArrayList<T>类中的几个方法  
**方法描述:**
add讲一个元素添加到ArrayList的末尾clear删除ArrayList中的全部元素contain如果ArrayList里面包含某个特定元素，则返回true，否则返回falseget删除指定索引处的那个元素indexOf返回ArrayList中的指定元素第一次出现的索引remove被重载的方法，删除第一次出现的指定值或者指定索引处的某个元素size返回保存在ArrayList中的元素个数trimToSize将ArrayList的容量裁剪成当前的元素个数  
15. 每个enum声明定义一个enum类具有的限制：  
①enum类型隐含final，因为它声明的是变量，不能修改  
②enum常量隐含为静态的  
③如果试图用new运算符创建enum类型的常量，会导致编译错误  
16. 将超类和子类引用赋予超类和子类类型的4种途径  
①将超类引用赋予超类变量  
②将子类引用赋予子类变量  
③将子类引用赋予超类变量是安全因为子类对象“是”超类对象。但是，超类对象只能用来引用超类成员。如果代码通过超类变量引用了只有子类才有的成员，则编译器会报告错误  
④将超类引用赋予子类变量，是一种编译错误。为了避免这一错误，必须显式地将超类引用强制转换成子类类型。执行时，如果引用所指的对象不是子类对象，则会发生异常，应当使用instanceof运算符来保证只对子类对象进行这种强制转换  
17. 异常处理：专门用于应付同步错误，这种错误是在语句执行时发生的。这类错误的常见例子包括：数组下标越界，算数溢出（即值位于科表示的范围之后），除零，无效的方法参数，线程中断以及不成功的内存分配（由于内存不够）。异常处理并不是用于处理与异步事件（例如磁盘I/O完成，网络信息到达，鼠标单击和键击）相关的错误，这类事件是与程序的控制流平行的或者独立的  
18. Throwable类的继承层次（部分）  

19. 带资源的try语句一般格式：  
try(ClassName theObject = new ClassName()){  
	//use theObject here  
}  
catch(Exception e){  
	//catch exception that occur while suing the resourse  
}   
20.类间关联的类框图  

解释：ATM类的一个对象执行Withdrawal类的0个或1个对象  
注：  
①关联是有方向的，Executes是关联名称  
②靠近类WithDrawal的单词currentTransaction是一个角色名称（role name），它表明Withdrawal对象在与ATM的关系中所扮演的角色  
