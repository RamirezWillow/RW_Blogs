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
4. &和|和&&，||用法一样，只是前者不执行短路求值，对于运算符右操作数有所需要的辅助效果（side effect）——修改变量的值，则逻辑与和逻辑或非常有用【联系：好2】  
5. Math类的几个方法  
方法描述：   
asb(x)x的绝对值ceil(x)将x四舍五入为不小于x的最小整数cos(x)x的三角余弦值（x为弧度）exp(x)指数方法e^xfloor(x)  
将x四舍五入为不大于x的最大整数  
log(x)x的自然对数（自然对数的底数为e）max(x,y)x与y的较大值min(x,y)x与y的较小值pow(x,y)x的y次幂sin(x)  
x的三角正弦值（x为弧度）  
spot(x)x的平方根  
tan(x)  
x的三角正切值（x为弧度）  
PIπ保留15位小数的近似值E自然对数e保留15位小数的近似值  
6. 将main声明为静态的，使JVM不用创建该类的实例就能够使用main的方法
7. 都用方法的方式：  
①使用方法名的本身，调用同一个类中的一个方法。  
②使用包含对象的引用的变量，后接一个点号和方法名称  
③使用类名称和一个点号来调用类的静态方法  
8. 静态方法只能直接调用一个类型的其他静态方法（即使用方法名称本身），并且只能直接操作同一个类型的静态变量。为了访问类的非静态成员，静态方法必须使用该类的对象的引用
9. 实参提升（argument promotion）——将实参值（在可能的情况下）转换成方法在其对应参数中希望接收的类型，其适用于包含两个或多个基本类型值的表达式，也可以适用于作为作为实参传递的方法的基本类型值
类型有效的提升double无   floatdoublelongfloat/douleintlong/float/doublecharint/long/float/doubleshort  
int/long/float/double  
byteshort/int/long/float/doubleboolean  
10. Java不允许将int值与枚举常量作比较
