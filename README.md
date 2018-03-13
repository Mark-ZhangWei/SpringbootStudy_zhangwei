# SpringbootStudy_zhangwei
First project to study spring boot
DROP TABLE IF EXISTS `question`;
CREATE TABLE `question` (
  `qid` int(11) NOT NULL AUTO_INCREMENT,
  `typeid` int(11) DEFAULT NULL,
  `qstem` text NOT NULL,
  `qchoose` varchar(500) DEFAULT NULL,
  `qresult` varchar(255) NOT NULL,
  `qanalysis` varchar(255) DEFAULT NULL,
  `qremark` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`qid`)
) ENGINE=InnoDB AUTO_INCREMENT=325 DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of question
-- ----------------------------
INSERT INTO `question` VALUES ('96', '6', ' 指出下列程序运行的结果 \npublic class Example{ \n　　String str=new String(\"good\"); \n　　char[]ch={\'a\',\'b\',\'c\'}; \n　　public static void main(String args[]){ \n　　　　Example ex=new Example(); \n　　　　ex.change(ex.str,ex.ch); \n　　　  System.out.print(ex.str+\" and \"); \n　　　　for(int i=0;i<ex.ch.length;i++){\n System.out.print(ex.ch[i]);\n} \n　　} \n　　public void change(String str,char ch[]){ \n　　　　str=\"test ok\"; \n　　　　ch[0]=\'g\'; \n　　} \n}\n', 'A. good and abc,B. good and gbc,C. test ok and abc,D. test ok and gbc', 'D', '', null);
INSERT INTO `question` VALUES ('97', '6', '下列说法错误的是？', 'A. 尽管现行的Java语言版本不允许类的多继承，但是我们仍然可以在extends关键字后面放置一个列表,B. 在实现多态后，利用父类引用（声明时类型）调用父类子类均声明了的变量和方法，均调用在子类中声明的版本,C. Java中代码重用中的has a关系通过定义类属性方式实现，is a通过类继承来实现,D. this关键字代表当前对象，即this引用的是当前创建的类实例对象的句柄', 'B', '利用声明时类型调用父类和子类同时声明的属性时，调用方法是子类（运行时类型）声明的，而变量则是调用父类（声明时类型）声明的', null);
INSERT INTO `question` VALUES ('98', '6', '以下哪个是有关封装优点的正确描述？', 'A. 只需要一个public方法,B. 从任何方法中没有异常抛出,C. 可以不需要改变接口来改变实现，以达到外部使用代码无需变动,D. 可以不需要改变实现来改变接口，已达到外部使用代码无需变动', 'C', '封装把实现细节隐藏起来了，因此封装可以实现对类内部的改变不会影响到其他代码', null);
INSERT INTO `question` VALUES ('99', '6', '以下说法错误的是？', 'A. Java中接口不能被private或Protected修饰符修饰,B. Java中一个类可以实现多个接口，但是只能继承一个父类,C. 接口中定义的成员变量，即使不说明，默认均是public\\static\\final的,D. final\\static\\native关键字不能修饰接口，', 'D', '内部接口可以用static修饰', null);
INSERT INTO `question` VALUES ('100', '6', '给出以下代码，请问以下哪个描述是正确的？Public XXXX extends something1,something2', 'A. 如果XXXX是一个接口，something1和something2取消掉，则代码段合法,B. 如果XXXX是一个类，something1和something2均是接口，则代码段合法,C. 如果XXXX、something1和something2均是接口，则代码段合法,D. 因为Java语言不支持多继承机制，所以代码段不合法', 'C', '', null);
INSERT INTO `question` VALUES ('101', '6', '请问以下哪个程序代码体现了对象之间的is a关系？', 'A. public interface Color {\n\n}\n\npublic class Shape {\n private Color color;\n},B. public interface Component {\n\n}\n\npublic class Cpmtaomer implements Component {\n private Component[] children;\n},C. public class Species{ \n}\npublic class Animal{ \n private Species species;\n},D. public class Animal{ \n public interface Species{ \n }\n private Species species;\n}', 'B', '', null);
INSERT INTO `question` VALUES ('102', '6', '给出以下代码，改程序的执行结果是？\ninterface Base {\n int k = 0;\n}\npublic class Example implements Base {\n\n public static void main(String[] args) {\n  int i;\n  Example exm = new Example();\n  i = exm.k;\n  i = Example.k;\n  i = Base.k;\n  System.out.println(i);\n }\n}', 'A. 无内容输出,B. 代码编译失败,C. 代码运行时输出异常信息,D. 打印输出0', 'D', '变量K为接口中定义的一个静态常量，可以使用类名调用，也可以使用实例名调用', null);
INSERT INTO `question` VALUES ('103', '6', '给出下面代码，请问该程序的运行结果是什么？\ninterface A{\n int x=0;\n A(){\n  x=5;\n }\n A(int s){\n  x=s;\n }\n \n}', 'A. 编译不通过，因为接口中的构造器必须用public修饰,B. 编译不通过，因为接口中不能超过一个以上的构造器,C. 编译不通过，因为接口中不能存在构造器,D. 编译不通过，因为接口名必须超过1个字符', 'C', '', null);
INSERT INTO `question` VALUES ('104', '6', '以下代码的执行结果是：\npublic class Example {\n String s = \"Outer\";\n public static void main(String[] args) {\n  S2 s2 = new S2();\n  s2.display();\n }\n}\n\nclass S1 {\n String s = \"S1\";\n void display() {\n  System.out.println(s);\n }\n}\n\nclass S2 extends S1 {\n String s = \"S2\";\n}', 'A. S1,B. S2,C. null,D. Outer', 'A', '本题中，由于子类S2中未定义display方法，因此在子类S2实例上调用的display方法是继承自父类的S1中的，由于display方法只能对同类上的成员变量s进行访问，因此打印输出S1', null);
INSERT INTO `question` VALUES ('105', '6', '关于构造器说法错误的是', 'A. 构造器不属于类成员方法，因此构造器不能被继承,B. 只有构造器才能拥有和类名相同的方法名,C. 一个类可以拥有多个重载的构造器,D. 在子类中调用父类的非默认构造器，必须使用super（...）语句，而且该语句必须位于子类构造器的第一行', 'B', '普通类成员方法也可以和类同名，但是会造成隐患，不建议这么命名', null);
INSERT INTO `question` VALUES ('106', '6', '以下哪个针对默认无参构造器描述是正确的？', 'A. 均是public构造器,B. 均无访问修饰符,C. 均与所属类访问修饰符一致,D. 由编译器决定', 'C', '', null);
INSERT INTO `question` VALUES ('107', '6', '当一个类的所有构造器均为私有的，以下哪个描述是正确的？', 'A. 不能被其他类实例化,B. 不能被其他类继承,C. 既不能被其他类实例化，也不能被其他类继承,D. 该类必须被final修饰', 'C', '当一个类的所有构造器均为私有，这意味着其他类无法通过new语句实例化该类，并且该类不能被继承，如果子类可以继承该类，在实例化子类时，必须首先调用该类的构造器，但由于构造器是私有的，不能调用，因此使得子类无法实例化。', null);
INSERT INTO `question` VALUES ('108', '6', '以下哪些修饰符可以用于构造器？', 'A. final,B. static,C. synchronized,D. 以上选项均不行', 'D', '', null);
INSERT INTO `question` VALUES ('110', '6', '11) 已知如下代码： 1: class Example{\n2: String str;\n3: public Example(){\n4: str= \"example\";\n5: }\n6: public Example(String s){\n7: str=s;\n8: }\n9:} }\n10: class Demo extends Example{\n11: }\n12: public class Test{\n13:public void f () {\n14:Example ex = new Example(\"Good\");\n15:Demo d = new Demo(\"Good\");\n16:} }\n哪句语句会导致错误？\n', 'A. line6,B. line10,C. line14,D. line15', 'D', '构造方法不能被继承，因此Demo类不存在带有一个字符串参数的构造方法', null);
INSERT INTO `question` VALUES ('111', '6', '关于重载和覆盖，以下说法错误的是', 'A. 重载方法的返回值、访问修饰符以及抛出的异常都不是重载方法判断的决定因素,B. 一个静态方法既可以被重载为一个静态方法，也可以被重载为一个非静态方法,C. 一个静态方法既可以被覆盖为一个静态方法，也可以被覆盖为一个非静态方法,D. 覆盖的方法返回值必须和源方法返回值类型保持赋值兼容，访问权限不能小于源方法，只能抛出源方法异常或源方法异常的子类', 'C', '静态方法只能覆盖为静态方法', null);
INSERT INTO `question` VALUES ('112', '6', '现有基类中的一个方法：void method(){},请问以下哪些是子类中覆盖该方法的正确形式？', 'A. void method(){},B. int method(){return 0;},C. void method(int i),D. private void method()', 'A', '', null);
INSERT INTO `question` VALUES ('113', '6', '现有如下代码：\nclass Super {\n public float getNum() {\n  return 3.0f;\n }\n}\nclass Sub extends Super {\n // 空白处\n}\n请问以下哪个语句放置在注释的空白处会引起编译错误？', 'A. public float getNum(){return 4.0f;},B. public void getNum(){},C. public void getNum(double d){},D. public double getNum(float d){return 4.0;}', 'B', '', null);
INSERT INTO `question` VALUES ('114', '6', '以下代码的执行结果是什么？\npublic class Example {\n int i = 100;\n\n public void print() {\n  System.out.println(50);\n }\n\n public static void main(String[] args) {\n  Example a = new A();\n  System.out.println(a.i);\n  a.print();\n }\n}\n\nclass A extends Example {\n int i = 200;\n\n public void print() {\n  System.out.println(300);\n }\n}', 'A. 100\n300,B. 200\n300,C. 100\n50,D. 200\n50', 'A', '多态环境下利用父类引用调用属性，调用变量使用的是父类声明的，调用方法则因为动态绑定使用的是子类声明的', null);
INSERT INTO `question` VALUES ('115', '6', '在下面代码中，在插入代码处插入什么语句可以实现在A中的amethod()方法中直接调用类C的test()方法，而不需要创建一个类C的实例？\nclass C{\n public void test(){ \n  System.out.println(\"C\");\n }\n}\nclass B extends C{\n public void test(){ \n  System.out.println(\"B\");\n }\n}\nclass A extends B{\n public void test(){ \n  System.out.println(\"A\");\n }\n public void amethod(){\n  //插入代码处\n }\n}\n', 'A. test(),B. super.test(),C. super.super.test(),D. 不能实现该要求', 'D', 'super只能访问直接父类被覆盖的方法，不能跨级使用', null);
INSERT INTO `question` VALUES ('116', '6', '现有以下代码：\nclass Base {\n\n}\n\nclass Sub extends Base {\n public String getFields() {\n  String name = \"Sub\";\n  return name;\n }\n}\n\nclass DoSub {\n public static void main(String[] args) {\n  Base b = new Sub();\n  // 插入语句处\n }\n}\n在插入语句处插入那条代码能够输出Sub？', 'A. System.out.println(b.getFields());,B. System.out.println(b.name);,C. System.out.println((Base)b.getFields());,D. System.out.println(((Sub)h).getFields());', 'D', '', null);
INSERT INTO `question` VALUES ('117', '6', '欲构造ArrayList类继承了List接口，下列哪个方法是正确的', 'A. ArrayList myList=new Object(),B.  List myList=new ArrayList(),C. ArrayList myList=new List(),D. List myList=new List()', 'D', '', null);
INSERT INTO `question` VALUES ('118', '6', '以下关于abstract的说法，正确的是', 'A. abstract只能修饰类,B.  abstract只能修饰方法,C. abstract类中必须有abstract方法,D. abstarct方法所在的类必须用abstract修饰', 'D', '', null);
INSERT INTO `question` VALUES ('119', '6', '关于类继承的说法，正确的是', 'A. Java 类允许多继承,B. Java接口允许多继承,C. 接口和类都允许多继承,D. 接口和类都不允许多继承', 'B', '', null);
INSERT INTO `question` VALUES ('120', '6', '关于接口的说法，正确的是', 'A. 接口中的方法只能在接口的实现类中实现,B. 接口中可定义变量成员,C. 接口中不能定义常量,D. 以上都不对', 'A', '接口中的方法都是抽象方法', null);
INSERT INTO `question` VALUES ('121', '6', '如果类中的成员变量只可以被同一包访问，则使用如下哪个约束符?', 'A.  private,B. public,C. protected,D. no modifier', 'D', '', null);
INSERT INTO `question` VALUES ('122', '6', '以下哪个约束符可用于定义成员常量', 'A. static,B. final,C. abstract,D. const', 'B', '', null);
INSERT INTO `question` VALUES ('123', '6', '给出如下代码:\nclass Test{\n　　private int m;\n　　public static void fun() {\n　　　　// some code...\n　　}\n}\n如何使成员变量m 被函数fun()直接访问?\n', 'A. 将private int m 改为protected int m,B. 将private int m 改为 public int m,C. 将private int m 改为 static int m,D. 将private int m 改为 int m', 'B', '静态方法中只能访问临时变量或类的static成员', null);
INSERT INTO `question` VALUES ('124', '6', '下列代码能否正常运行，如果能够正常运行，输出结果是什么\npublic class TestClass { \n public static void main(String[] args) {\n  int num1=5;\n  int num2=5;  \n  class InnerClass{\n   public int add(){\n    return num1+num2;\n   }\n  };  \n  InnerClass in=new InnerClass();\n System.out.println(in.add());  \n }\n}', 'A. 输出10,B. 输出0,C. 运行时输出异常信息,D. 编译不能通过', 'D', '内部内中访问外部类中的非成员属性，要求该属性为final', null);
INSERT INTO `question` VALUES ('125', '6', '以下代码的执行结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  Base b = new Base();\n  Subclass1 S1 = new Subclass1();\n  Subclass2 s2 = new Subclass2();\n  s1 = (Subclass1) s2;\n }\n}\n\nclass Base {\n}\n\nclass Subclass1 extends Base {\n}\n\nclass Subclass2 extends Base {\n}', 'A. 代码编译成功，运行期间没有异常抛出,B. 代码编译失败，赋值语句s1 = （Subclass1）s2非法,C. 代码编译成功，但运行时ClassCastException对象造型异常被抛出,D. 代码编译失败，因为一个基类不能被多个子类继承', 'B', '', null);
INSERT INTO `question` VALUES ('126', '6', '以下代码的执行结果是：\npublic class Example {\n static int i = 1, j = 2;\n static {\n  display(i);\n  i = i + j;\n }\n\n static void display(int n) {\n  System.out.println(n);\n }\n\n public static void main(String[] args) {\n  display(i);\n }\n}', 'A. 1\n2,B. 0\n1,C. 1\n3,D. 1\n1', 'C', '', null);
INSERT INTO `question` VALUES ('127', '6', '对于内部类，以下说法错误的是', 'A. 匿名内部类可以实现接口或继承其他类，但不能同时即实现接口又继承类,B. 匿名内部类不能有任何明确的构造器,C. 内部类可以定义在外部类类体中，也可以定义在外部类的方法体中，和外部类不同，内部类均能使用访问修饰符，并能使用static修饰,D. 在Java中，对内部类的嵌套层次没有限制', 'C', '定义在方法体中的内部类不能使用访问控制符和static修饰', null);
INSERT INTO `question` VALUES ('128', '6', '对于以下代码，请问插入哪个语句可以访问到内部类InsideOne?\npublic class Example {\n public static void main(String[] args) {\n  EnclosingOne eo=new EnclosingOne();\n  //插入语句处\n }\n}\n\nclass EnclosingOne{ \n public class InsideOne{  \n }\n}', 'A. InsideOne ei=new eo.InsideOne();,B. InsideOne ei=EnclosingOne.new InsideOne();,C. InsideOne ei=new EnclosingOne.InsideOne();,D. EnclosingOne.InsideOne ei=eo.new InsideOne();', 'D', '', null);
INSERT INTO `question` VALUES ('129', '7', '以下哪些是关于完全封装的正确描述？', 'A. 所有的变量都是私有的,B. 所有的方法都是私有的,C. 只有通过提供的方法才能访问类属性,D. 通过方法和变量名均可访问属性', 'A、C', '', null);
INSERT INTO `question` VALUES ('130', '7', '请选择所有的正确答案', 'A. 在接口中定义的方法默认为private方法,B. 在接口中定义的变量默认为public、static、final的,C. 一个接口可以继承多个接口,D. 关键字implements代表接口的继承关系', 'B、C', '', null);
INSERT INTO `question` VALUES ('131', '7', '以下哪些描述是正确的？', 'A. native关键字表明修饰的方法是由其他非Java语言编写的,B. 能够出现在Java源文件中import语句前的只有注释语句,C. 接口中定义的方法默认是public和abstract的，不能被private或protected修饰,D. 构造器只能被public或protected修饰', 'A、C', '', null);
INSERT INTO `question` VALUES ('132', '7', '以下哪些关于构造器的描述是正确的？', 'A. 子类可以继承父类的构造器,B. 如果没有编写构造器，编译器会自动为类提供一个无参的默认构造器,C. 构造器都没有返回值,D. 构造器可以抛出异常', 'B、C、D', '', null);
INSERT INTO `question` VALUES ('133', '7', '给出下面的代码段:\npublic class Base{\nint w, x, y ,z;\npublic Base(int a,int b)\n{\nx=a; y=b;\n}\npublic Base(int a, int b, int c, int d)\n{\n// assignment x=a, y=b\nw=d;\nz=c;\n}\n}\n在代码说明// assignment x=a, y=b处写入如下哪几个代码是正确的？（ ）\n', 'A. Base(a,b);,B. x=a, y=b;,C. x=a; y=b;,D. this(a,b)', 'C、D', '', null);
INSERT INTO `question` VALUES ('134', '7', '以下关于方法覆盖描述正确的有', 'A. 覆盖的方法和被覆盖的方法必须具有相同的方法名、参数列表和返回类型,B. 覆盖的方法的访问范围不能比被覆盖的方法访问范围小,C. 覆盖的方法不能抛出被覆盖方法不能抛出的异常,D. 被覆盖的方法不能被private修饰符修饰', 'B、C、D', '覆盖方法的返回值类型可以不一致，但要保证类型是和被重载方法返回值赋值兼容', null);
INSERT INTO `question` VALUES ('135', '7', '现有一下代码：protected void method(int x){...}，以下哪些有关覆盖该方法的描述是正确的？', 'A. 覆盖的方法必须采用int型作为唯一个一个参数,B. 覆盖的方法必须返回类型为void,C. 覆盖的方法可以被private修饰符修饰,D. 覆盖的方法可以返回任何类型的值', 'A、B', '', null);
INSERT INTO `question` VALUES ('136', '7', '现有以下代码：\npublic class MethodOver{ \n public void setVar(int a,int b,float c){  \n }\n}\n以下哪些是满足setVar方法的正确重载形式？', 'A. private void setVar(int a,float c,int b){},B. protected void setVar(int a,int b,float d){},C. public int setVar(int a,float c,int b){return a;},D. public int setVar(int a,float c){return a;}', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('137', '7', '现有以下代码，请问该程序的运行结果是什么？\nclass A {\n protected int method(){\n  return 0;\n } \n}\nclass B extends A{\n int method(){\n  return 0;\n }\n}', 'A. 编译失败，因为覆盖方法的访问范围不能比被覆盖的方法更窄,B. 编译失败，因为类A中的method()方法声明为protected,因此对其子类都是不可见的,C. 编译失败，如果将第7行加上public修饰符，可编译通过,D. 编译失败，如果将第7行加上pritected修饰符，可编译通过', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('138', '7', '现有以下代码：\ninterface W {\n}\n\nclass Z implements W {\n}\n\nclass X extends Z {\n}\n\nclass Y extends Z {\n}\n下列哪些代码段是正确的？\n', 'A. X x=new X();\nY y=new Y();\nZ z=new Z();\ny=(Y)x;,B. X x=new X();\nY y=new Y();\nZ z=new Z();\nx=(X)y;,C. X x=new X();\nY y=new Y();\nZ z=new Z();\nZ=(Z)x;,D. X x=new X();\nY y=new Y();\nZ z=new Z();\nW w=(W)x;', 'C、D', '', null);
INSERT INTO `question` VALUES ('139', '7', '有关匿名内部类描述正确的有', 'A. 匿名内部类没有显式构造器,B. 匿名内部类可以实现接口,C. 匿名内部类可以继承非final类,D. 匿名内部类可以同时实现接口和继承非final类', 'A、B、C', '', null);
INSERT INTO `question` VALUES ('140', '7', '以下哪些类型的变量可以被一个内部类访问？', 'A. 所有static变量,B. 所有final变量,C. 所有的实例成员变量,D. 只有final静态变量', 'A、B、C', '', null);
INSERT INTO `question` VALUES ('141', '7', '以下关于内部类的描述哪些是正确的？', 'A. 定义在内部类中的变量不能被static修饰符修饰，除非内部类本身是静态的,B. 定义在类中非方法中的内部类，可以访问外部类的所有变量，而不管变量的访问控制声明,C. 一个内部类实际上是外部类的子类,D. 内部类可以被private修饰符修饰', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('142', '6', '下列说法错误的是？', 'A. 尽管现行的Java语言版本不允许类的多继承，但是我们仍然可以在extends关键字后面放置一个列表,B. 在实现多态后，利用父类引用（声明时类型）调用父类子类均声明了的变量和方法，均调用在子类中声明的版本,C. Java中代码重用中的has a关系通过定义类属性方式实现，is a通过类继承来实现,D. this关键字代表当前对象，即this引用的是当前创建的类实例对象的句柄', 'B', '', null);
INSERT INTO `question` VALUES ('143', '6', '以下哪个语句实现了声明一个二维整数数组？', 'A. int[]5[5] a = new int[][];,B. int a = new int[5,5];,C. int []a[] = new int[5][5];,D. int[][] a = new [5]int[5];', 'C', 'Java语言中声明数组时，方括号与变量的位置关系无特定次序', null);
INSERT INTO `question` VALUES ('144', '6', '以下代码运行输出的结果是什么？\npublic class Example {\n\n public static void main(String[] args) {\n  char[] c = new char[100];\n  System.out.println(c[50]);\n }\n}', 'A. 打印输出50,B. 打印输出49,C. 打印输出\\u0000,D. 打印输出null', 'C', '数组对象通过new语句实例化后，数组中的元素根据数据类型会自动被系统初始化，即被赋予默认数值，字符型值是一个无符号整数型，初始值为0，形式为\'\\u0000\'', null);
INSERT INTO `question` VALUES ('145', '6', '以下哪个语句用于获取数组中的元素个数？', 'A. intArray.size();,B. intArray.size();,C. intArray.length;,D. intArray.length();', 'C', '注意和字符串获取长度的方式区分，字符串提供length()方法，而数组则是length属性', null);
INSERT INTO `question` VALUES ('146', '6', '下列代码的执行结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  int index = 1;\n  int[] foo = new int[3];\n  int bar = foo[index];\n  int baz = bar + index;\n  System.out.println(baz);\n }\n}', 'A. 打印输出0,B. 打印输出1,C. 打印输出2,D. 运行期间有异常抛出', 'B', '', null);
INSERT INTO `question` VALUES ('147', '6', '给出下面代码： \npublic class Example{ \n　　static int arr[] = new int[10];\n　　public static void main(String a[]) \n　　{ \n　　　System.out.println(arr[1]); \n　　} \n} \n那个语句是正确的？\n', 'A. 编译时将产生错误,B. 编译时正确，运行时将产生错误,C. 输出0,D. 输出null', 'C', '', null);
INSERT INTO `question` VALUES ('148', '6', '为将数组myArray的长度由3改为6，现采取以下代码：\nint[] myArray = new int[3];\nmyArray = new int[6];\n代码执行后，以下叙述哪项是正确的？', 'A. 数组myArray的长度已由3改为6，其中前3个元素的值不变，后3个元素的值为空,B. 数组myArray的长度已经由3变为6，其中前三个元素的值不变，后3个元素需要经过初始化才能使用,C. 数组myArray的长度没有变化,D. 数组myArray的长度已由3改为6，原来3个元素的值全部丢失', 'D', '', null);
INSERT INTO `question` VALUES ('149', '6', '以下代码执行的结果是：\npublic class Example {\n public static void main(String[] args) {\n  int[] x = { 1, 2, 3 };\n  x[1] = (x[1] > 1) ? x[2] : 0;\n  System.out.println(x[1]);\n }\n}', 'A. 输出1,B. 输出2,C. 输出3,D. 输出4', 'C', '', null);
INSERT INTO `question` VALUES ('150', '6', '以下那种初始化数组的方式是错误的？', 'A. String[] names = {\"zhang\",\"wang\",\"li\"};,B. String names[] = new String[3];\nnames[2] = \"li\";\nnames[0] = \"zhang\";\nnames[1] = \"wang\";,C. String[3] names = {\"zhang\",\"wang\",\"li\"};,D. 以上写法都正确', 'C', '', null);
INSERT INTO `question` VALUES ('151', '7', '以下哪些是声明一个字符串数组的正确形式？', 'A. String[] s;,B. String []S;,C. Sting [s],D. String s[]', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('152', '7', '以下哪些语句正确？', 'A. double snow[] = new double[31];,B. double snow[31] = new array[31];,C. double snow[31] = new array;,D. double[] snow = new double[31];', 'A、D', '', null);
INSERT INTO `question` VALUES ('153', '7', '以下哪些是声明一个数组的正确形式？', 'A. int i[][];,B. int i[5][5];,C. int[] i[],D. int[][] a;', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('154', '7', '以下哪些是初始化数组的正确形式？', 'A. char c[] = {\'a\',\'b\'};,B. int []x[] = {{1,2,3},{1,2,3}};,C. int x[3] = {1,2,3};,D. int []x = {0,0,0};', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('155', '7', '执行下列代码后,哪个结论是正确的 String[] s=new String[10];', 'A. s[10] 为 \"\",B. s[9] 为 null,C. s[0] 为 未定义,D. s.length 为10', 'B、D', '', null);
INSERT INTO `question` VALUES ('156', '6', '以下哪个是finalize()方法的正确形式？', 'A. protected void finalize() throws Throwable,B. final finalize(),C. public final finalize(),D. private boolean finalize()', 'A', '', null);
INSERT INTO `question` VALUES ('157', '6', '如果finalize（）方法抛出一个运行时异常，以下哪个描述正确？', 'A. 正在运行的应用程序系统崩溃,B. 此异常被忽略，并且该异常对象被垃圾回收器回收,C. 此异常被忽略，但是该异常对象未被垃圾回收期回收,D. 此异常导致JVM崩溃', 'B', 'finalize()方法只是用于清除对象，而不是实际的销毁对象，因此对该方法的调用不会引起系统崩溃，该方法抛出的异常也会作为废弃对象被垃圾回收期回收', null);
INSERT INTO `question` VALUES ('158', '6', '如何释放掉一个对象占据的内存空间？', 'A. 调用free()方法,B. 调用System.gc()方法,C. 赋值给该对象的引用为null,D. 程序员无法明确强制垃圾回收器运行', 'D', '', null);
INSERT INTO `question` VALUES ('159', '6', '给出以下代码：\n1.public class Example {\n2. public static void main(String[] args) {\n3.  String s = \"abcd\";\n4.  Integer x = new Integer(3);\n5.  String s2 = s + 4;\n6.  s2 = null;\n7.  s = null;\n8. }\n9.}\n改程序运行到第几行变量S2引用的对象符合垃圾回收器回收条件？', 'A. 第7行,B. 不存在,C. 第6行,D. 直到main线程结束，S2应用的对象才可能被回收', 'C', '', null);
INSERT INTO `question` VALUES ('160', '6', '以下代码运行到关键点处，有多少对象符合垃圾回收的条件？\npublic class Example {\n public static void main(String[] args) {\n  String name;\n  String newName = \"Nick\";\n  newName = \"Jason\";\n  name = \"Frieda\";\n  String newestName = name;\n  name = null;\n  // 关键点\n }\n}', 'A. 0个,B. 1个,C. 2个,D. 3个', 'B', '', null);
INSERT INTO `question` VALUES ('161', '7', '以下哪些是有关垃圾回收器的正确描述？', 'A. 程序员可以在制定时间调用垃圾回收器释放内存,B. 垃圾回收器可以保证Java程序不会产生内存溢出,C. 程序员可以制定垃圾回收器回收对象,D. 对象的finalize()方法在对象被垃圾回收器回收之前获得调用', 'C、D', '通过通配符*号引入的两个不同包中存在同名的类，当代码中不加包名直接使用时，会产生编译错误，使用时需要提供完整包路径', null);
INSERT INTO `question` VALUES ('162', '7', '拥有下列哪些引用类型的对象在虚拟机内存足够的情况下不会被垃圾回收机制回收？', 'A. 强引用,B. 软引用,C. 弱引用,D. 虚引用', 'A、B', '', null);
INSERT INTO `question` VALUES ('163', '6', 'Java语言中异常的分类是哪项？', 'A. 运行时异常和异常,B. 受检异常和非受检异常,C. 错误和异常,D. 错误和运行时异常', 'C', '', null);
INSERT INTO `question` VALUES ('164', '6', '所有异常的父类是哪项？', 'A. Throwable,B. Error,C. RuntimeException,D. Exception', 'A', '', null);
INSERT INTO `question` VALUES ('165', '6', '下列属于非受检异常（运行时异常）的是哪项？', 'A. SQLException,B. IOException,C. NullPointerException,D. OutOfMemoryError', 'C', '', null);
INSERT INTO `question` VALUES ('166', '6', '假设有自定义异常类ServiceException,那么抛出该异常的语句正确的是哪项？', 'A. raise ServiceException,B. throw new ServiceException(),C. throw ServiceException,D. throws ServiceException', 'B', '', null);
INSERT INTO `question` VALUES ('167', '6', '在方法声明中，说明该方法可能会抛出的异常列表时使用哪个关键字？', 'A. throw ,B. catch,C. finally,D. throws', 'D', '', null);
INSERT INTO `question` VALUES ('168', '6', '现有代码：\npublic class Example {\n public static void main(String[] args) {\n  try {\n   System.out.print(Integer.parseInt(\"forty\"));   \n  } catch (RuntimeException e) {\n   System.out.println(\"Runtime\");\n  }catch (NumberFormatException e) {\n   System.out.println(\"Number\");\n  }\n }\n}\n执行结果是什么？', 'A. 输出Number,B. 输出Runtime,C. 输出40,D. 编译失败', 'D', 'NumberFormatException是RuntimeException的子类，因此两个catch块位置应该交换才能正确处理异常', null);
INSERT INTO `question` VALUES ('169', '6', '现有代码如下：\npublic class Example {\n\n void topGo() {\n  try {\n   middleGo();\n  } catch (Exception e) {\n   System.out.println(\"catch\");\n  }\n }\n\n void middleGo() throws Exception {\n  go();\n  System.out.println(\"late middle\");\n }\n\n void go() throws Exception {\n  throw new Exception();\n }\n\n public static void main(String[] args) {\n  Example example = new Example();\n  example.topGo();\n }\n}\n该代码的执行结果是？', 'A. 输出late middle,B. 输出catch,C. 输出late middle catch,D. 输出catch late middle', 'B', '', null);
INSERT INTO `question` VALUES ('170', '6', '如下代码执行后的输出结果是？\npublic class Example {\n public static void main(String[] args) {\n  try {\n   throw new Exception();\n  } catch (Exception e) {\n   try {\n    throw new Exception();\n   } catch (Exception e2) {\n    System.out.println(\"inner\");\n   }\n   System.out.println(\"middle\");\n  }\n  System.out.println(\"out\");\n }\n}', 'A. inner outer,B. middle outer,C. inner middle outer,D. 编译失败', 'C', '', null);
INSERT INTO `question` VALUES ('171', '6', '现有如下代码：\npublic class Example extends Utils{\n public static void main(String[] args) {\n  try {\n   System.out.println(new Example().getInt(\"42\"));\n  } catch (NumberFormatException e) {\n   System.out.println(\"NFExc\");\n  }\n } \n int getInt(String arg) throws NumberFormatException{\n  return Integer.parseInt(arg);\n }\n}\n\nclass Utils {\n int getInt(String arg) {\n  return 42;\n }\n}\n该代码执行的结果是？', 'A. NFExc,B. 42,C. 42NFExc,D. 编译失败', 'B', 'Utils中的getInt方法没有抛出异常，而子类Example中的getInt抛出了运行时异常，这是符合方法覆盖的抛出异常特性规范的，因为运行时异常并不会强制要求方法调用代码捕获处理', null);
INSERT INTO `question` VALUES ('172', '6', '现有如下代码：\npublic class Example extends Utils{\n public static void main(String[] args) {\n  try {\n   System.out.println(new Example().getInt(\"42\"));\n  } catch (NumberFormatException e) {\n   System.out.println(\"NFExc\");\n  }\n } \n int getInt(String arg) throws Exception{\n  return Integer.parseInt(arg);\n }\n}\n\nclass Utils {\n int getInt(String arg) {\n  return 42;\n }\n}\n该代码执行的结果是？', 'A. NFExc,B. 42,C. 42NFExc,D. 编译失败', 'D', '子类抛出的异常不符合方法覆盖的异常列表要求，因此编译失败（见上题）', null);
INSERT INTO `question` VALUES ('173', '6', '现有如下代码：\npublic class Example {\n public static void main(String[] args) {// a\n  new Example().topGo();\n }\n\n void topGo() {// b\n  middleGo();\n }\n\n void middleGo() {// c\n  go();\n  System.out.println(\"late middle\");\n }\n\n void go() {// d\n  throw new Exception();\n }\n}\n为了使代码能够编译通过，需要在哪个地方加入声明throws Exception?', 'A. d,B. c和d,C. b、c和d,D. a、b、c和d', 'D', '', null);
INSERT INTO `question` VALUES ('174', '6', '下面代码的执行结果是？\nclass Example extends Utils {\n public static void main(String[] args) {\n  try {\n   System.out.print(new Example().getlnt(\"42\"));\n  } catch (Exception e) {\n   System.out.println(\"Exc\");\n  }\n }\n\n int getlnt(String arg) throws Exception {\n  return Integer.parseInt(arg);\n }\n}\n\nclass Utils {\n int getlnt() {\n  return 42;\n }\n}', 'A. NFExc,B. 42,C. 42NFExc,D. 编译失败', 'B', '本题没有实现方法覆盖', null);
INSERT INTO `question` VALUES ('175', '6', '关于异常处理，说法错误的是？', 'A. try…catch…finally结构中，必须有try语句块，catch语句块和finally语句块不是必须的，但至少要两者取其一,B. 在异常处理中，若try中的代码可能产生多种异常则可以对应多个catch语句，若catch中的参数类型有父类子类关系，此时应该将子类放在后面，父类放在前面,C. 一个方法可以抛出多个异常，方法的返回值也能够是异常,D. Throwable是所有异常的超类', 'B', '若catch中的参数类型有父类子类关系，此时应该将子类放在前面，父类放在后面', null);
INSERT INTO `question` VALUES ('176', '6', '以下关于Error和Exception类的描述正确的是？', 'A. Error类和Exception类都是Throwable类的子类,B. Error类是一个final类，而Exception类是一个非final类,C. Exception类是一个final类，而Error类是一个非final类,D. Error类和Exception类都实现了Throwable接口', 'A', '', null);
INSERT INTO `question` VALUES ('177', '6', '请问以下哪个是声明一个方法抛出异常的正确形式？', 'A. void m() throws IOException{},B. void m() throw IOException,C. void m(){} throws IOException,D. void m(void) throw IOException{}', 'A', '', null);
INSERT INTO `question` VALUES ('178', '6', '请问以下哪些关于try…catch…finally结构中的finally语句的描述是正确的？', 'A. 只有当一个catch语句获得执行后，finally语句才获得执行,B. 只有当catch语句未获得执行时，finally语句才获得执行,C. 如果有finally语句，return语句将在finally语句执行完毕后才会返回,D. 只有当异常抛出时，finally语句才获得执行', 'C', '', null);
INSERT INTO `question` VALUES ('179', '6', '请问以下代码的直接执行结果是？\nclass Example{\n public static void main(String[] args) {\n  try {\n   System.out.println(args[0]);\n   System.out.println(\"I\'m nomal\");\n   if (true)\n    return;\n  } catch (Exception ex) {\n   System.out.println(\"I\'m exception\");\n   if (true)\n    return;\n  } finally {\n   System.out.println(\"I\'m finally.\");\n  }\n\n  System.out.println(\"Out of try.\");\n }\n｝', 'A. I\'m exception\nI\'m finally.\n,B. 代码不能编译通过，因为最后一条语句位于return后，不可到达,C. 代码编译通过，但运行时输出异常信息,D. I\'m nomal\nI\'m finally.', 'A', '', null);
INSERT INTO `question` VALUES ('180', '6', '关于以下代码，说法正确的是？\nclass Example{\n public static void main(String[] args) throws IOException {\n  if (args[0] == \"hello\") {\n   throw new IOException();\n  }\n }\n}', 'A. 代码编译成功,B. 代码编译失败，因为main()方法是入口方法，不能抛出异常,C. 代码编译失败，因为IOException异常是系统异常，不能由应用程序抛出,D. 代码编译失败，因为字符串应该用equals方法判定一致性', 'A', '', null);
INSERT INTO `question` VALUES ('181', '6', '关于以下代码，说法正确的是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  System.out.println(\"Before Try\");\n  try {\n  } catch (java.io.IOException e) {\n   System.out.println(\"Inside Catch\");\n  }\n  System.out.println(\"At the End\");\n }\n}', 'A. 代码编译失败，因为无异常抛出,B. 代码编译失败，因为未导入IOException异常类,C. 输出Before Try\nAt the End,D. 输出Inside Catch\nAt the End', 'A', '', null);
INSERT INTO `question` VALUES ('182', '6', '关于以下代码，说法正确的是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  System.out.println(\"Before Try\");\n  try {\n  } catch (Throwable e) {\n   System.out.println(\"Inside Catch\");\n  }\n  System.out.println(\"At the End\");\n }\n}', 'A. 代码编译失败，因为无异常抛出,B. 代码编译失败，因为未导入IOException异常类,C. 输出Before Try\nAt the End,D. 输出Inside Catch\nAt the End', 'C', '', null);
INSERT INTO `question` VALUES ('183', '6', '给出以下代码：\nclass Example {\n public static void main(String[] args) throws IOException {\n  try {\n   methodA();   \n  } catch (IOException e) {\n   System.out.println(\"caught IOException\");\n  }catch (Exception e) {\n   System.out.println(\"caught Exception\");\n  }\n }\n}\n如果methodA()方法抛出一个IOException异常，则该程序的运行结果是什么？', 'A. 无内容输出,B. 代码编译失败,C. 输出caught IOException,D. 输出caught Exception', 'C', '', null);
INSERT INTO `question` VALUES ('184', '6', '下列代码的运行结果是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  try {\n   return;\n  } finally{\n   \n   System.out.println(\"Finally\");\n  }\n }\n}', 'A. 无内容输出,B. 输出Finally,C. 代码编译失败,D. 输出异常信息', 'B', '', null);
INSERT INTO `question` VALUES ('185', '6', '给出以下代码，执行结果是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  aMethod();\n }\n \n static void aMethod(){\n  try {\n   System.out.println(\"Try\");\n   return;\n  } catch (Exception e) {\n   System.out.println(\"Catch\");\n  }finally{\n   System.out.println(\"Finally\");\n  }\n }\n}', 'A. 代码编译成功，但运行期间抛出异常,B. 代码便以失败，因为return语句错误,C. 输出Try和Finally,D. 输出Try', 'C', '', null);
INSERT INTO `question` VALUES ('186', '6', '以下代码中，如果test()方法抛出一个NullPointException异常时，打印输出什么内容？\nclass Example {\n public static void main(String[] args) throws IOException {\n  try {\n   test();\n   System.out.println(\"Message1\");\n  } catch (ArrayIndexOutOfBoundsException e) {\n   System.out.println(\"Message2\");\n  }finally{\n   System.out.println(\"Message3\");\n  }\n }\n}', 'A. 打印输出Message1,B. 打印输出Message2,C. 打印输出Message3,D. 以上都不对', 'C', '', null);
INSERT INTO `question` VALUES ('187', '6', '以下代码执行结果是什么？\nclass Example {\n public static String output = \"\";\n public static void foo(int i) {\n  try {\n   if (i == 1) {\n    throw new Exception();\n   }\n   output += \"1\";\n  } catch (Exception e) {\n   output += \"2\";\n   return;\n  } finally {\n   output += \"3\";\n  }\n  output += \"4\";\n }\n\n public static void main(String[] args) throws IOException {\n  foo(0);\n  foo(1);\n  System.out.println(output);\n }\n}', 'A. 无内容输出,B. 代码编译失败,C. 输出13423,D. 输出14323', 'C', '', null);
INSERT INTO `question` VALUES ('188', '6', '以下代码执行结果是？\npublic abstract class Example extends Base {\n public abstract void method();\n}\n\nclass Base {\n public Base() throws IOException {\n  throw new IOException();\n }\n}', 'A. 代码编译失败，因为非抽象类不能被扩展为抽象类,B. 代码编译失败，因为必须提供一个可以抛出或可以不抛出IOException异常的构造器,C. 代码编译失败，以in为必须提供一个可以抛出IOException异常或其子类的构造器,D. 代码编译成功', 'C', '', null);
INSERT INTO `question` VALUES ('189', '6', '关于以下代码正确的说法是：\n1.public class Example {\n2. int x = 0;\n3.\n4. public Example(int inVal) throws Exception {\n5.  if (inVal != this.x) {\n6.   throw new Exception(\"Invalid input\");\n7.  }\n8. }\n9.\n10. public static void main(String[] args) {\n11.  Example t = new Example(4);\n12. }\n13.}', 'A. 代码在第1行编译错误,B. 代码在第4行编译错误,C. 代码在第6行编译错误,D. 代码在第11行编译错误', 'D', '', null);
INSERT INTO `question` VALUES ('190', '7', '关于try…catch…finally结构，描述正确的是些？', 'A. 可以有多个catch,B. 只能有一个catch,C. 可以没有catch,D. finally必须有', 'A、C', '', null);
INSERT INTO `question` VALUES ('191', '7', '当fragile()方法抛出一个IllegalArgumentException异常时，下列代码的运行结果是什么？\npublic static void main(String[] args) throws IOException {\n  try {\n   fragile();\n  } catch (NullPointerException e) {\n   System.out.println(\"NullPointerException thrown\");\n  } catch (Exception e) {\n   System.out.println(\"Exception thrown\");\n  } finally {\n   System.out.println(\"Done with exceptions\");\n  }\n  System.out.println(\"myMethod is done\");\n }\n｝', 'A. 输出NullPointerException thrown,B. 输出Exception thrown,C. 输出Done with Exception,D. 输出myMethod is done', 'B、C、D', '', null);
INSERT INTO `question` VALUES ('192', '7', '现有如下代码：\npublic class Example { \n public static void main(String[] args) {\n  try {\n   int x=Integer.parseInt(\"42a\");\n   //插入代码处\n   System.out.println(\"oops\");\n  }\n }\n}\n在插入代码处插入哪些语句可以在运行后输出oops？', 'A.  } catch (IllegalArgumentException e) {,B. } catch (IllegalStateException c) {,C.  } catch (NumbelFormatException n) {,D. } catch (ClassCastException c) {', 'A、C', '', null);
INSERT INTO `question` VALUES ('193', '7', '下列代码的执行结果是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  int i = 1, j = 1;\n  try {\n   i++;\n   j--;\n   if (i == j) {\n    j++;\n   }\n  } catch (ArithmeticException e) {\n   System.out.println(0);\n  } catch (ArrayIndexOutOfBoundsException e) {\n   System.out.println(1);\n  } catch (Exception e) {\n   System.out.println(2);\n  } finally {\n   System.out.println(3);\n  }\n  System.out.println(4);\n }\n}', 'A. 输出1,B. 输出2,C. 输出3,D. 输出4', 'C、D', '', null);
INSERT INTO `question` VALUES ('194', '7', '下列代码的执行结果是？\nclass Example {\n public static void main(String[] args) throws IOException {\n  int i = 1, j = 1;\n  try {\n   i++;\n   j--;\n   if (i/j > 1) {\n    j++;\n   }\n  } catch (ArithmeticException e) {\n   System.out.println(0);\n  } catch (ArrayIndexOutOfBoundsException e) {\n   System.out.println(1);\n  } catch (Exception e) {\n   System.out.println(2);\n  } finally {\n   System.out.println(3);\n  }\n  System.out.println(4);\n }\n}', 'A. 输出0,B. 输出2,C. 输出3,D. 输出4', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('195', '7', '现有如下代码：\npublic class Example { \n public static void main(String[] args) {\n  try {\n   System.out.println(\"before\");\n   doRisyThing();\n   System.out.println(\"after\");\n  } catch (Exception e) {\n   System.out.println(\"catch\");\n  }\n  System.out.println(\"done\");\n }\n \n public static void doRisyThing() throws Exception{\n  //this code returns unless it throws an Exception\n }\n}\n该代码可能的执行结果有哪些？', 'A. before catch,B. before after done,C. before catch done,D. before after catch', 'B、C', '', null);
INSERT INTO `question` VALUES ('196', '7', '以下有关java.lang.Exception异常类的正确描述有？', 'A. 该类是一个公共类,B. 该类是Throwable类的子类,C. 该类实现了Throwable接口,D. 该类可以序列化', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('197', '7', '给出以下代码：\n1. public void aMethod(){  \n2.  \n3.  if(Condition){\n4.   \n5.  }\n6.  \n7. }\n当if条件表达式为true时，插入哪些语句可以抛出MyException异常？', 'A. 在第4行插入throws new MyException();,B. 在第4行插入throw new MyException();,C. 在第6行插入throw new MyException();,D. 在第1行插入throws MyException', 'B、D', '', null);
INSERT INTO `question` VALUES ('198', '7', '以下哪些是catch语句能够捕获处理的异常？', 'A. Throwable,B. Error,C. Exception,D. String', 'A、B、C', 'Error也是可以被catch捕获的', null);
INSERT INTO `question` VALUES ('199', '7', '以下哪些描述是正确的？', 'A. try语句块后必须至少存在一个catch语句块,B. try语句块后可以存在不限数量的finally语句块,C. try语句块后必须至少存在一个catch语句块或finally语句块,D. 如果catch和finally语句块同时存在，则catch语句块必须位于finally语句块前', 'C、D', '', null);
INSERT INTO `question` VALUES ('200', '6', '下列代码的执行结果是？\nclass Example {\n\n private void method1() throws Exception {\n  throw new RuntimeException();\n }\n\n public void method2() {\n  try {\n   method1();\n  } catch (RuntimeException e) {\n   System.out.println(\"Caught Runtime Exception\");\n  } catch (Exception e) {\n   System.out.println(\"Caught Exception\");\n  }\n }\n\n public static void main(String[] args) throws IOException {\n  Example a = new Example();\n  a.method2();\n }\n}', 'A. 代码编译失败,B. 输出Caught Runtime Exception,C. 输出Caught Exception,D. 输出Caught Runtime Exception和Caught Exception', 'B', '', null);
INSERT INTO `question` VALUES ('201', '7', '以下代码的输出结果是什么？选择所有的正确答案。\nclass Example {\n public static void main(String[] args) throws IOException {\n  for (int i = 0; i < 10; i++) {\n\n   try {\n    try {\n     if (i % 3 == 0)\n      throw new Exception(\"E0\");\n     System.out.println(i);\n    } catch (Exception inner) {\n     i *= 2;\n     if (i % 3 == 0)\n      throw new Exception(\"E1\");\n    } finally {\n     ++i;\n    }\n   } catch (Exception outer) {\n    i += 3;\n   } finally {\n    --i;\n   }\n  }\n }\n}', 'A. 4,B. 5,C. 6,D. 7', 'A、B', '', null);
INSERT INTO `question` VALUES ('202', '6', '下列说法错误的是？', 'A. Object类是所有Java类的顶层类，即类继承树的根。,B. 如果一个类没有使用extends关键字扩展任何类，则编译器自动将创建的类视为Object类的子类,C. Object类中提供了equals()方法来判定本对象和其他对象中的内容是否一致,D. Object中提供的clone默认为浅克隆', 'C', 'equals方法默认和==一致', null);
INSERT INTO `question` VALUES ('203', '6', '定义在Object类上的hashCode()方法的返回值类型是什么？', 'A. char,B. long,C. int,D. float', 'C', '', null);
INSERT INTO `question` VALUES ('204', '6', '关于集合中对象的equals()和hashCode()规定说法错误的是？', 'A. 如果两个对象相同，那么他们的hashCode值需要一致,B. 如果两个对象的hashCode值一致，他们的equals方法不一定返回true,C. equals方法默认和==判定一致,D. Java中hashCode就是对象的内存地址', 'D', 'Java中hashCode不是内存地址，但是可以一定程度上代表地址特诊', null);
INSERT INTO `question` VALUES ('205', '6', '以下代码执行结果是什么？\nclass Person {\n static void sayHello() {\n  System.out.println(\"HelloWorld!\");\n }\n}\n\npublic class Example {\n public static void main(String[] args) {\n  ((Person) null).sayHello();\n }\n}', 'A. 编译失败,B. 编译成功，运行时产生NullPointerException,C. 输出HelloWorld!,D. 输出空白字符串', 'C', 'null能够被造型撑任何类型，而sayHello方法是静态方法，不依赖实例调用', null);
INSERT INTO `question` VALUES ('206', '6', '以下代码的执行结果是？\nclass RectObject {\n public int x;\n public int y;\n\n public RectObject(int x, int y) {\n  this.x = x;\n  this.y = y;\n }\n\n\n @Override\n public boolean equals(Object obj) {\n  if (this == obj)\n   return true;\n  if (obj == null)\n   return false;\n  if (getClass() != obj.getClass())\n   return false;\n  final RectObject other = (RectObject) obj;\n  if (x != other.x) {\n   return false;\n  }\n  if (y != other.y) {\n   return false;\n  }\n  return true;\n }\n}\n\npublic class Example {\n public static void main(String[] args) {\n  HashSet<RectObject> set = new HashSet<RectObject>();\n  RectObject r1 = new RectObject(3, 3);\n  RectObject r2 = new RectObject(5, 5);\n  RectObject r3 = new RectObject(3, 3);\n  set.add(r1);\n  set.add(r2);\n  set.add(r3);\n  set.add(r1);\n  System.out.println(\"size:\" + set.size());\n }\n}', 'A. size:1,B. size:2,C. size:3,D. size:4', 'C', '首先判断r1对象和r2对象的hashCode，因为Object中的hashCode方法返回的是对象本地内存地址的换算结果，不同的实例对象的hashCode是不相同的，同样因为r3和r1的hashCode也是不相等的，但是r1==r1的，所以最后set集合中只有r1,r2,r3这三个对象，所以大小是3', null);
INSERT INTO `question` VALUES ('207', '6', '以下代码执行结果是？\nclass RectObject {\n public int x;\n public int y;\n\n public RectObject(int x, int y) {\n  this.x = x;\n  this.y = y;\n }\n\n\n @Override\n public boolean equals(Object obj) {\n  return false;\n }\n}\n\npublic class Example {\n public static void main(String[] args) {\n  HashSet<RectObject> set = new HashSet<RectObject>();\n  RectObject r1 = new RectObject(3, 3);\n  RectObject r2 = new RectObject(5, 5);\n  RectObject r3 = new RectObject(3, 3);\n  set.add(r1);\n  set.add(r2);\n  set.add(r3);\n  set.add(r1);\n  System.out.println(\"size:\" + set.size());\n }\n}', 'A. size:1,B. size:2,C. size:3,D. size:4', 'C', '首先是判断hashCode是否相等，不相等的话，直接跳过，相等的话，然后再来比较这两个对象是否相等或者这两个对象的equals方法，因为是进行的或操作，所以只要有一个成立即可，那这里我们就可以解释了，其实上面的那个集合的大小是3,因为最后的一个r1没有放进去，以为r1==r1返回true的，所以没有放进去了。所以集合的大小是3，如果我们将hashCode方法设置成始终返回false的话，这个集合就是4了。', null);
INSERT INTO `question` VALUES ('208', '6', '以下代码执行结果是？\nclass RectObject {\n public int x;\n public int y;\n\n public RectObject(int x, int y) {\n  this.x = x;\n  this.y = y;\n }\n\n @Override\n public int hashCode() {\n  // TODO Auto-generated method stub\n  return (int)System.nanoTime();\n }\n\n @Override\n public boolean equals(Object obj) {\n  return false;\n }\n}\n\npublic class Example {\n public static void main(String[] args) {\n  HashSet<RectObject> set = new HashSet<RectObject>();\n  RectObject r1 = new RectObject(3, 3);\n  RectObject r2 = new RectObject(5, 5);\n  RectObject r3 = new RectObject(3, 3);\n  set.add(r1);\n  set.add(r2);\n  set.add(r3);\n  set.add(r1);\n  System.out.println(\"size:\" + set.size());\n }\n}', 'A. size:1,B. size:2,C. size:3,D. size:4', 'D', '见上题', null);
INSERT INTO `question` VALUES ('209', '6', '下列关于Math类说法错误的是', 'A. java.lang.Math类是final类，因此不能被其他类继承,B. java.lang.Math类的构造器是私有的，即声明为private，不能实例化一个Math类的对象,C. java.lang.Math类上定义的所有常量和方法均是public和static的，因此可以直接通过类名调用,D. min()和max()方法的参数之一，如果是NaN值，则方法将返回另一个参数值', 'D', 'min()和max()方法的参数之一，如果是NaN值，则方法的返回值就为NaN', null);
INSERT INTO `question` VALUES ('210', '6', '以下哪个方法是Math类中定义的？', 'A. absolute(),B. log(),C. cosine(),D. sine()', 'B', '在Math类中对应的正确方法应为abs()\\cos()\\sin()', null);
INSERT INTO `question` VALUES ('211', '6', '定义在Math类上的round(double d)方法的返回值类型是什么？', 'A. char,B. int,C. long,D. double', 'C', 'round方法用于获取一个四舍五入的整数', null);
INSERT INTO `question` VALUES ('212', '6', '以下哪个方法用于计算平方根？', 'A. squareRoot(),B. sqrt(),C. root(),D. sqr()', 'B', '', null);
INSERT INTO `question` VALUES ('213', '6', '调用Math.random()方法最有可能输出以下哪些结果？', 'A. -0.12和0.56E3,B. 0.12和1.1E1,C. -23.45和0.0,D. 0.356和0.03', 'D', 'random()方法返回值的取值范围在0.0..1.0之间', null);
INSERT INTO `question` VALUES ('214', '6', '以下代码的输出结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  System.out.println(Math.round(Float.MAX_VALUE));\n }\n}', 'A. 输出Integer.MAX_VALUE,B. 输出一个最接近Float.MAX_VALUE的整数,C. 编译失败,D. 运行时输出异常信息', 'A', 'Math.round(Float.MAX_VALUE)的返回值为Integer.MAX_VALUE，Math.round(Double.MAX_VALUE)的返回值为Long.MAX_VALUE（真实计算结果超过返回值范围）', null);
INSERT INTO `question` VALUES ('215', '6', '以下代码的运行结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  System.out.println(Math.min(0.0, -0.0));\n }\n}', 'A. 代码编译失败,B. 输出0.0,C. 输出-0.0,D. 代码编译成功，但运行时输出异常信息', 'C', '浮点数的取值范围内存在正负0.0', null);
INSERT INTO `question` VALUES ('216', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  System.out.println(Math.min(0.0, -0.0));\n }\n}', 'A. 输出4,B. 输出5,C. 输出6 ,D. 输出9', 'D', '比2.3大的最接近整数是3，因此ceil(2.3f)=3.0，因为2.7的四舍五入的值为3.0，所以round(2.7)=3.0，最终打印输出等于9', null);
INSERT INTO `question` VALUES ('217', '6', '以下代码的运行结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  double d1 = -0.5;\n  System.out.println(\"Ceil d1=\" + Math.ceil(d1));\n  System.out.println(\"Floor d1=\" + Math.floor(d1));\n }\n}\n', 'A. 输出Ceil d1=-0.0 Floor d1=-1.0,B. 输出Ceil d1=0.0 Floor d1=-1.0,C. 输出Ceil d1=-0.0 Floor d1=-0.0,D. 输出Ceil d1=0.0 Floor d1=0.0', 'A', '', null);
INSERT INTO `question` VALUES ('218', '6', '给出以下代码，为了结果输出-12.0，方法method(d)应为以下哪个方法？\npublic class Example {\n public static void main(String[] args) {\n  double d = -11.1;\n  double d1 = method(d);\n  System.out.println(d1);\n }\n}', 'A. floor(),B. ceil(),C. round(),D. abs()', 'A', '', null);
INSERT INTO `question` VALUES ('219', '6', '给出以下代码，请问在程序的第6行插入那条语句，改程序可依次打印输出11、10、9？\n1.public class Example {\n2. public static void main(String[] args) {\n3.  double x[] = { 10.2, 9.1, 8.7 };\n4.  int i[] = new int[3];\n5.  for (int a = 0; a < x.length; a++) {\n6.\n7.   System.out.println(i[a]);\n8.  }\n9. }\n10.}', 'A. i[1] = ((int)Math.min(x[a]));,B. i[1] = ((int)Math.max(x[a]));,C. i[1] = ((int)Math.ceil(x[a]));,D. i[1] = ((int)Math.floor(x[a]));', 'C', '', null);
INSERT INTO `question` VALUES ('220', '6', '以下代码执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  System.out.println(Math.min(Float.NaN, Float.POSITIVE_INFINITY));\n }\n}', 'A. 输出NaN,B. 打印输出Infinity,C. 运行时异常，因为NaN不是有效的参数,D. 运行时异常，因为Infinity不是有效的参数', 'A', 'min()和max()方法的参数之一，如果是NaN值，则方法的返回值就为NaN', null);
INSERT INTO `question` VALUES ('221', '6', '以下代码的执行结果是？\npublic class Example{\n  public static void main(String s[]){\n   String str=”123”;\nString str_=new String(“123”);\nString  _str=”123”;\n   System.out.println(str==_str);\nSystem.out.println(str==str_);\n} \n}\n', 'A. 输出true true,B. 输出false false,C. 输出true false,D. 输出false true', 'C', '字符串创建的时候可以使用常量池', null);
INSERT INTO `question` VALUES ('222', '6', 'public class Example {\n public static void main(String[] args) {\n  Integer i = 100;\n  Integer j = 100;\n  System.out.println(i == j);\n  i = 300;\n  j = 300;\n  System.out.println(i == j);\n }\n}', 'A. 输出true true,B. 输出false false,C. 输出true false,D. 输出false true', 'C', '128以内的数进行自动包装时使用池操作', null);
INSERT INTO `question` VALUES ('223', '6', '以下哪个不是基本类型的包装类？', 'A. Char,B. Integer,C. Boolean,D. float', 'A', '', null);
INSERT INTO `question` VALUES ('224', '6', '以下说法正确的是？', 'A. Void类是Class类的子类,B. Float类是Double类的子类,C. Double类是Wrapper类的子类,D. Integer类是Number类的子类', 'D', '', null);
INSERT INTO `question` VALUES ('225', '6', '定义在Integer类上的哪些方法用于将一个Integer对象转换为一个基本数据int类型？', 'A. valueOf（）,B. intValue（）,C. getInt（）,D. getInteger（）', 'B', '', null);
INSERT INTO `question` VALUES ('226', '6', '一下代码的执行结果是什么？\npublic class Example {\n public static void main(String[] args) {\n  String val = null;\n  int x = Integer.parseInt(val);\n  System.out.println(x);\n }\n}', 'A. 输出0,B. 输出null,C. 输出NumberFormatException异常,D. 无内容输出', 'C', '', null);
INSERT INTO `question` VALUES ('227', '6', '由于Java中存在字符串对象池，因此采用下面方法创建的两个字符串变量，他们指向的是同一个字符串对象：String str1=\"asddsg\";String str2=\"asddsg\"', 'A. 调用字符串上定义的改变字符串内容的方法，返回值都是一个新字符串，而原有字符串内容不变,B. 调用replace（char oldChar,char newChar）方法时，当参数oldChar和newChar一致时，返回一个和源对象内容一致的新字符串,C. String的equals方法用于判定两个字符串内容是否一致,D. 调用toUpperCase()和toLowerCase()方法，当为进行大小写转换时，返回源字符串对象', 'B', '调用replace（char oldChar,char newChar）方法时，当参数oldChar和newChar一致时，返回源字符串对象', null);
INSERT INTO `question` VALUES ('228', '6', '以下说法错误的是？', 'A. String中的append方法用于在源字符串后追加内容,B. StringBuffer中的append方法用于在源字符串后追加内容,C. StringBuffer是一个缓冲区，器内容可变,D. String中的concat方法用于字符串串联', 'A', 'String中没有append方法', null);
INSERT INTO `question` VALUES ('229', '6', '以下哪些有关通过子类来扩展String类功能的描述是正确的？', 'A. 无法子类化，因为String类是一个final类,B. 可以子类化，通过覆盖String类中的方法实现功能扩展,C. 无法子类化，因为String类是一个抽象类,D. 可以子类化，但是只能覆盖Object类中声明的方法，因为String类中定义的其他方法否是final的', 'A', '', null);
INSERT INTO `question` VALUES ('230', '6', '嗲用以下哪个方法会导致字符串被改变？', 'A. concat(),B. toUpperCase(),C. replace(),D. 没有改变字符串的方法可以调用', 'D', '', null);
INSERT INTO `question` VALUES ('231', '6', '如何获取一个String类实例S包含的字符个数？', 'A. s.size,B. s.length,C. s.size(),D. s.length()', 'D', '', null);
INSERT INTO `question` VALUES ('232', '6', '以下代码执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  System.out.println(\"string\".endsWith(\"\"));\n }\n}', 'A. 输出true,B. 输出false,C. 编译失败,D. 运行时输出异常信息', 'A', '', null);
INSERT INTO `question` VALUES ('233', '6', '有String s = \"Metallica\";请问以下哪个语句可以打印输出ica？', 'A. System.out.println(s.substring(7));,B. System.out.println(s.substring(6));,C. System.out.println(s.substring(6，8));,D. System.out.println(s.substring(7，9));', 'B', '', null);
INSERT INTO `question` VALUES ('234', '7', '以下那些关于String类的描述是正确的？', 'A. 该类是一个final类,B. 该类是一个public类,C. 该类可以序列化,D. 该类有一个一StringBuffer实例作为参数的构造器', 'A、B、C、D', '', null);
INSERT INTO `question` VALUES ('235', '7', '以下哪些是String类中定义的方法？', 'A. length（）,B. toUpper(),C. toString(),D. equals()', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('236', '7', '以下哪些关于封装类的描述是正确的？', 'A. 封装类都是public类,B. 封装类均可序列化,C. 封装类均是final类,D. 封装类都是java.lang.Number类的子类', 'A、B、C', '', null);
INSERT INTO `question` VALUES ('237', '7', '请问以下哪些方法是定义在Object类上的，请选择所有正确答案', 'A. toString(),B. equals(Object o),C. println(),D. wait()', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('238', '7', '请问以下哪些描述是正确的？请选择所有正确答案', 'A. Class类是Object类的超类,B. Object类是一个final类,C. Class类可用于装载其他类,D. ClassLoader类可用于装载其他类', 'C、D', '', null);
INSERT INTO `question` VALUES ('239', '7', '以下哪些方法是定义在Math类上用于三角计算的方法？', 'A. sin(),B. cos(),C. tan(),D. aSin()', 'A、B、C', '', null);
INSERT INTO `question` VALUES ('240', '7', '给出以下代码，请问以下哪些定义在Math类上的方法可以使表达式结果为true?\nMethod(-4.4) == -4', 'A. round(),B. trunc(),C. floor(),D. ceil()', 'A、D', '', null);
INSERT INTO `question` VALUES ('241', '7', '以下哪些方法是Math类中定义的？', 'A. random(),B. Random(),C. toDegrees(),D. square()', 'A、C', '', null);
INSERT INTO `question` VALUES ('242', '7', '以下哪些是定义在Math类中的有效方法？', 'A. arcTan(double a),B. atan(double a),C. sqrt(double a),D. min(int a,int b)', 'B、C、D', '', null);
INSERT INTO `question` VALUES ('243', '6', '下列哪个属于集合接口？', 'A. Tree,B. Stack,C. Array,D. Map', 'D', '', null);
INSERT INTO `question` VALUES ('244', '6', '以下哪个是枚举接口？', 'A. Runnable,B. Throwable,C. Enumeration,D. List', 'C', '', null);
INSERT INTO `question` VALUES ('245', '6', '以下哪个集合接口支持通过字符串主键检索对象？', 'A. Map,B. Set,C. List,D. Collection', 'A', '', null);
INSERT INTO `question` VALUES ('246', '6', '以下哪个集合接口支持元素排序？', 'A. Collection,B. Set,C. List,D. Map', 'C', '', null);
INSERT INTO `question` VALUES ('247', '6', '通过语句new Vector(5,10);创建一个Vector实例，向该Vector实例添加第6个元素6会产生什么结果？', 'A. 一个IndexOutOfBounds异常抛出,B. Vector实例增加容量至10,C. Vector实例容量增加至15,D. Vector实例容量未增加，因为当添加第5个元素时，容量已增加过', 'C', '', null);
INSERT INTO `question` VALUES ('248', '6', '以下哪些语句用于创建一个Map实例？', 'A. Map m = new Map();,B. Map m = new Map(init capacity,increment capacity);,C. Map m = new Map(new Collection());,D. 无法实例化', 'D', 'Map是接口', null);
INSERT INTO `question` VALUES ('249', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  String s1 = \"abc\";\n  String s2 = \"def\";\n  Stack<String> stack = new Stack<String>();\n  stack.push(s1);\n  stack.push(s2);\n  try {\n   String s3 = stack.pop() + stack.peek();\n   System.out.println(s3);\n  } catch (Exception e) {\n   // TODO: handle exception\n  }\n }\n}', 'A. abcdef,B. defabc,C. abcabc,D. defdef', 'B', '', null);
INSERT INTO `question` VALUES ('250', '6', '以下代码执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  String s1 = \"abc\";\n  String s2 = \"def\";\n  Stack<String> stack = new Stack<String>();\n  stack.push(s1);\n  stack.push(s2);\n  try {\n   String s3 = stack.pop() + stack.peek();\n   System.out.println(s3);\n  } catch (Exception e) {\n   // TODO: handle exception\n  }\n }\n}', 'A. abcdefabcdef,B. defabcdefabc,C. fedcbafedcba,D. abcdef', 'D', '', null);
INSERT INTO `question` VALUES ('251', '6', '以下代码执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  TreeMap<String, String> map = new TreeMap<String, String>();\n  map.put(\"one\", \"1\");\n  map.put(\"two\", \"2\");\n  map.put(\"three\", \"3\");\n  displayMap(map);\n }\n\n static void displayMap(TreeMap map) {\n  Collection<String> c = map.entrySet();\n  Iterator<String> i = c.iterator();\n  while (i.hasNext()) {\n   Object o = i.next();\n   System.out.print(o.toString());\n  }\n }\n}', 'A. onetwothree,B. 123,C. one=1three=2two=2,D. onethreetwo', 'C', '', null);
INSERT INTO `question` VALUES ('252', '6', '集合中Set接口的特点是', 'A. 不允许重复元素，元素有顺序,B. 允许重复元素，元素无顺序,C. 允许重复元素，元素有顺序,D. 不允许重复元素，元素无顺序', 'D', '', null);
INSERT INTO `question` VALUES ('253', '6', '实现了Set接口的类是哪项？', 'A. ArrayList,B. HashTable,C. HashSet,D. Collection', 'C', '', null);
INSERT INTO `question` VALUES ('254', '6', '表示键值对概念的接口是哪项？', 'A. Set,B. List,C. Collection,D. Map', 'D', '', null);
INSERT INTO `question` VALUES ('255', '6', 'List接口的特点是哪项？', 'A. 不允许重复元素，元素有顺序,B. 允许重复元素，元素无顺序,C. 允许重复元素，元素有顺序,D. 不允许重复元素，元素无顺序', 'C', '', null);
INSERT INTO `question` VALUES ('256', '6', '创建一个只能存放String的泛型ArrayList的语句是哪项', 'A. ArrayList<int> al = new ArrayList<int>();,B. ArrayList<String> al = new ArrayList<String>();,C. ArrayList al = new ArrayList<String>();,D. ArrayList<String> al = new List<String>();', 'B', '', null);
INSERT INTO `question` VALUES ('257', '6', '下列代码执行后的输出是哪项？\npublic class Example {\n public static void main(String[] args) {\n  List<String> al = new ArrayList<String>();\n  al.add(\"1\");\n  al.add(\"2\");\n  al.add(\"2\");\n  al.add(\"3\");\n  System.out.println(al);\n }\n}', 'A. [1,2,3],B. [1,2,3,3],C. [1,2,2,3],D. [2,1,3,2]', 'C', '', null);
INSERT INTO `question` VALUES ('258', '6', '以下代码中“插入代码处”插入什么内容将导致程序输出“abc”?', 'A. for(Iterator o : list.iterator();o.hasNext();),B. for(Iterator o : list),C. for(String 0: list.iterator()),D. for(String o : list)', 'D', '', null);
INSERT INTO `question` VALUES ('259', '6', '以下代码的执行结果是？\npublic class Example {\n\n public static void main(String[] args) {\n  TreeSet<String> t = new TreeSet<String>();\n  if (t.add(\"one\"))\n   if (t.add(\"two\"))\n    if (t.add(\"three\"))\n     t.add(\"four\");\n  for (String s : t) {\n   System.out.print(s);\n  }\n }\n}', 'A. one,B. onethreetwo,C. onetwothreefour,D. fouronethreetwo', 'D', 'TreeSet中默认按自然排序排列', null);
INSERT INTO `question` VALUES ('260', '6', '现有如下类型：\na - java.util.Hashtable\nb - java.util.List\nc - java.util.ArrayList\nd - java.util.SortedSet\n和定义：\n1-使用本接口，允许用户控制集合中每个元素的插入位置\n2-使用本集合，确保用户可以按照递增或元素的自然顺序遍历集合\n3-本具体类型允许空元素及基于索引的访问\n4-本集合是同步的\n哪一组匹配是对的？', 'A. 2描述d，3描述b,B. 1描述b，3描述c,C. 3描述a，4描述b,D. 4描述a，2描述c', 'B', '', null);
INSERT INTO `question` VALUES ('261', '6', '现有：\npublic class Example {\n\n public static void main(String[] args) {\n  TreeSet<String> s = new TreeSet<String>();\n  s.add(\"one\");\n  s.add(\"two\");\n  // 插入代码处\n  for (String s2 : sorted) {\n   System.out.print(s2 + \" \");\n  }\n }\n}\n和四个代码片段：\ns1:SortedSet sorted = s.tailSet(s.first());\ns2:SortedSet<String> sorted = s.tailSet(s.first());\ns3:SortedSet sorted = (SortedSet)s.tailSet(s.first());\ns4:SortedSet sorted = (SortSet<String>)s.tailSet(s.first());\n分别插入到插入代码处，哪项可以编译？\n', 'A. S2,B. S2和S3,C. S2和S4,D. S2、S3和S4', 'A', '', null);
INSERT INTO `question` VALUES ('262', '6', '现有：\npublic class Example {\n\n public static void main(String[] args) {\n  //插入代码处\n  c.put(\"X\", 123);\n }\n}\n下列哪些插入到插入代码处能够正常编译？', 'A. Map c = new SortedMap();,B. HashMap c = new HashMap();,C. SortedMap c = new TreeMap();,D. Map c = new LinkedHashMap();', 'B', '', null);
INSERT INTO `question` VALUES ('263', '7', '现有：\nlist是一个合法的集合引用\ngetCollection（）返回一个合法集合的引用，以下语句哪些是合法的？', 'A. for(Object o : list),B. for(Object o : getCollection()),C. for(Object o : list.iterator()),D. for(Iterator I;list.iterator();i.hasNext())', 'B、C、D', '', null);
INSERT INTO `question` VALUES ('264', '7', '哪些集合是同步的？', 'A. TreeSet,B. Hashtable,C. Vector,D. LinkedList', 'B、C', '', null);
INSERT INTO `question` VALUES ('265', '7', '下列哪些项是泛型的优点？', 'A. 不用向下强制类型转换,B. 代码容易编写,C. 类型安全,D. 运行速度快', 'A、C', '', null);
INSERT INTO `question` VALUES ('266', '7', '以下哪些是Collection接口的子接口？', 'A. Dictionary,B. List,C. Map,D. Set', 'B、D', '', null);
INSERT INTO `question` VALUES ('267', '7', '以下哪些有关Vector类的描述是正确的？', 'A. 该类是个public类,B. 该类是个final类,C. 该类实现了List接口,D. 该类可以序列化', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('268', '7', '以下哪些集合接口支持重复元素存在？', 'A. Collection,B. List,C. Map,D. Set', 'A、B', '', null);
INSERT INTO `question` VALUES ('269', '6', '以下哪些类提供了创建一个目录的方法？', 'A. File,B. DataOutput,C. Directory,D. FileDescriptor', 'A', '', null);
INSERT INTO `question` VALUES ('270', '6', '以下说法正确的是', 'A. RandomAccessFile类是File类的子类,B. FileWriter类提供有操作基本数据类型的方法,C. RandomAccessFile类提供有删除磁盘文件的方法,D. File类提供有删除磁盘文件的方法', 'D', '', null);
INSERT INTO `question` VALUES ('271', '6', '以下哪个类的构造器需要mode参数r或rw？', 'A. DataInputStream,B. InputStream,C. RandomAccessFile,D. File', 'C', '', null);
INSERT INTO `question` VALUES ('272', '6', '以下哪个关于Serializable的描述是正确的？', 'A. Serializable是Java语言中的一个关键字,B. Serializable是一个可以被实现的接口,C. Serializable是一个可以被继承的类,D. 以上均不对', 'B', '', null);
INSERT INTO `question` VALUES ('273', '6', '从InputStream对象中如何创建一个Reader对象？', 'A. 使用InputStream类中定义的createReader()方法,B. 吃用Reader类中的createReader()方法,C. 构造一个InputStreamReader实例，将InputStream对象作为InputStreamReader类构造器的参数传入,D. 构造一个OutputStreamReader实例，将InputStream对象作为OutputStreamReader类构造器 的参数传入', 'C', '', null);
INSERT INTO `question` VALUES ('274', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  File f = new File(\"c:\\\\large.txt\");\n }\n}', 'A. large.txt文件在本地硬盘上被创建,B. 在Unix系统上运行失败，因为路径分割符不正确,C. large.txt文件在本地硬盘上没有被创建,D. 如果large.txt文件已经存在，则一个异常被抛出', 'C', '', null);
INSERT INTO `question` VALUES ('275', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) {\n  RandomAccessFile raf = new RandomAccessFile(\"test.java\", \"rw\");\n  raf.seek(raf.length());\n }\n}', 'A. 代码编译失败,B. 运行期IOException异常抛出,C. 文件指针定位在最后一个字符前,D. 文件指针定位在最后一个字符后', 'A', '没有处理IO异常，如果处理了IO异常，文件又确实存在，则D成立', null);
INSERT INTO `question` VALUES ('276', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) throws IOException {\n  PrintStream pr = new PrintStream(new FileOutputStream(\"outfile\"));\n  System.out = pr;\n  System.out.println(\"OK!\");\n }\n}', 'A. 代码编译失败，以你为System.out是一个常量，不能赋值,B. 代码编译成功，但因为System.out是一个常量，导致运行期异常抛出,C. 控制台输出OK！,D. outfile文件中输出OK！', 'A', '', null);
INSERT INTO `question` VALUES ('277', '6', '给出以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) throws IOException {\n  StringReader strinin = new StringReader(\"test\");\n  LineNumberReader in = new LineNumberReader(strinin);\n  PrintWriter out = new PrintWriter(System.out);\n  out.println(in.readLine());\n  out.flush();\n }\n}', 'A. test,B. 1.test,C. 1：test,D. 1 test', 'A', '', null);
INSERT INTO `question` VALUES ('278', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) throws IOException {\n  RandomAccessFile file = new RandomAccessFile(\"test.txt\", \"rw\");\n  file.writeBoolean(true);\n  file.writeInt(123456);\n  file.writeInt(7890);\n  file.writeLong(10000000);\n  file.writeInt(777);\n  file.writeFloat(0.0001f);\n  file.seek(5);\n  System.out.println(file.readInt());\n  file.close();\n }\n}', 'A. 123456,B. 7890,C. 10000000,D. 777', 'B', '本例中共写入字节数为1（boolean）+4（int）+8（long）+4（int）+8(float)=29,seel（）方法用于从文件起始位置跳过制定数量的字节数，seek(5)是跳过了5个字节，所以从第6个字节开始读取，即从写入的第二个int型值（7890）开始读取，故打印输出为7890', null);
INSERT INTO `question` VALUES ('279', '6', '以下代码的执行结果是？\npublic class Example {\n public static void main(String[] args) throws IOException {\n  try {\n   String strString = \"test\";\n   char buffer[] = new char[strString.length()];\n   strString.getChars(0, strString.length(), buffer, 0);\n   FileWriter f = new FileWriter(\"MyFile1.txt\");\n   FileWriter f1 = f;\n   f1.close();\n   for (int i = 0; i < buffer.length; i++) {\n    f.write(buffer[i] + \"\");\n   }\n   f.close();\n   FileWriter f2 = new FileWriter(\"MyFile2.txt\");\n   f2.write(buffer);\n   f2.close();\n\n  } catch (IOException e) {\n   System.out.println(e.getMessage());\n  }\n }\n}', 'A. 运行期无异常抛出,B. 执行f1.close()抛出IOException异常,C. f.write(buffer[i]+\"\")抛出IOException异常,D. 执行new FileWriter(\"MyFile1.txt\")抛出IOException', 'C', '', null);
INSERT INTO `question` VALUES ('280', '6', '以下哪项是Java语言中定义的字节流？', 'A. OutputStream,B. Reader,C. Writer,D. InputStream', 'A', '', null);
INSERT INTO `question` VALUES ('281', '6', '在输入流的read方法返回哪个值的时候表示读取结束？', 'A. 0,B. 1,C. -1,D. null', 'C', '', null);
INSERT INTO `question` VALUES ('282', '6', '为了从文本文件中逐行读取内容，应该使用哪个处理流对象？', 'A. BufferedReader,B. BufferedWriter,C. BufferedInputStream,D. BufferedOutputStream', 'A', '', null);
INSERT INTO `question` VALUES ('283', '6', '为了实现自定义对象的序列化，该自定义对象必须实现哪个接口？', 'A. Volatile,B. Serializable,C. Runnable,D. Transient', 'B', '', null);
INSERT INTO `question` VALUES ('284', '6', '以下程序执行结果是？\npublic class Example {\n public static void main(String[] args) throws IOException {\n  String s = \"x,yy,123\";\n  Scanner sc = new Scanner(s);\n  while (sc.hasNext()) {\n   System.out.println(sc.next() + \" \");\n  }\n }\n}', 'A. x yy,B. x,yy,123,C. x yy 123,D. x,yy', 'B', '', null);
INSERT INTO `question` VALUES ('285', '6', '现有：\nf是一个File类实例的合法引用\nfr是一个FileReader类实例的合法引用\nbr是一个BufferedReader类实例的合法引用\n如下代码：\nString line = null;\n//插入代码处\nSystem.out.println(line);\n｝\n哪一行代码插入到插入代码处将循环一次输出文本文件的一行？', 'A. while((line = f.read())!=null){,B. while((line = fr.read())!=null){,C. while((line = br.read())!=null){,D. while((line = br.readLine())!=null){', 'D', '', null);
INSERT INTO `question` VALUES ('286', '6', '现有int x = reader.read()，下列哪一项正确？', 'A. reader不是FileReader或者BufferedReader类型,B. reader可以使FileReader或者BufferedReader,C. reader可以使FileReader类型，但不能使BufferedReader类型,D. reader可以使BufferedReader类型，但不能使FileReader类型', 'B', '', null);
INSERT INTO `question` VALUES ('287', '6', '现有：\nString s = \"write a line to a file\";\nw.print(s + \"\\n\");\n哪一个是对的？', 'A. w既可以是PrintWriter类型，也可以是BufferedWriter类型,B. w既不可以是PrintWriter类型，也不可以是BufferedWriter类型,C. w可以是PrintWriter类型，但不可以是BufferedWriter类型,D. w既可以是BufferedWriter类型，也可以是PrintWriter类型', 'C', '', null);
INSERT INTO `question` VALUES ('288', '6', '有如下代码：\npublic class Example implements Serializable {\n Collar c = new Collar();\n}\n\nclass Collar implements Serializable {\n CollarPart cp1 = new CollarPart();\n CollarPart cp2 = new CollarPart();\n}\n\nclass CollarPart implements Serializable {\n}\n如果Example实例被序列化，则多少对象将被序列化？', 'A. 1,B. 2,C. 3,D. 4', 'D', '', null);
INSERT INTO `question` VALUES ('289', '7', '以下关于File类的描述哪些是正确的？', 'A. File类可以用于访问当前工作路径中的文件,B. 当一个File类实例被构建时，对应的目录或文件在本地文件系统中被创建,C. File类可以用于访问本地文件系统中的目录或文件,D. 当一个File类实例被垃圾回收器回收后，对应的目录或文件也被删除', 'A、C', '', null);
INSERT INTO `question` VALUES ('290', '7', '以下哪些语句是构建RandomAccessFile实例的正确形式？', 'A. RandomAccessFile(\"file\",\"r\");,B. RandomAccessFile(\"r\",\"file\");,C. RandomAccessFile(\'r\',\"file\");,D. RandomAccessFile(\"file\",\"rw\");', 'A、D', '', null);
INSERT INTO `question` VALUES ('291', '7', '请问以下哪些修饰符用于修饰类属性时，该属性不能被序列化？', 'A. private,B. static,C. transient,D. protected', 'B、C', '', null);
INSERT INTO `question` VALUES ('292', '7', '以下哪些是FileOutputSteram类的正确构造形式？', 'A. FileOutputStream(FileDescriptor fd),B. FileOutputStream(String n,boolean a),C. FileOutputStream(boolean a),D. FileOutputStream(File f)', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('293', '7', '以下哪些是定义在java.io包中的抽象类？', 'A. InputStream,B. PrintStream,C. Reader,D. FileInputStream', 'A、C', '', null);
INSERT INTO `question` VALUES ('294', '7', '以下哪些描述是正确的？', 'A. InputStream和OutputStream类是基于字节流的,B. ObjectInputStream类和ObjectOutputStream类不支持序列化的对象,C. Reader和Writer是基于字符流的,D. Reader类和Writer类是支持对象序列化的首选', 'A、C', '', null);
INSERT INTO `question` VALUES ('295', '7', '以下哪些描述是正确的？', 'A. Writer类可以使用不同的字符编码向输出流写入字符,B. Writer类可以向输出流写入Unicode字符,C. Writer类提供向输出流写入任意Java基本数据类型的方法,D. Writer类提供向输出流写入引用数据类型的方法', 'A、B', '', null);
INSERT INTO `question` VALUES ('296', '6', 'super.getClass()方法调用,下面程序的输出结果是什么?\npublic class Example extends Date {\n\n public static void main(String[] args) {\n  new Example().test();\n }\n\n public void test() {\n  System.out.println(super.getClass().getName());\n }\n}', 'A. Date,B. Object,C. Example,D. 运行时抛出异常', 'C', '由于getClass()在Object类中,定义了final,子类不能覆盖这个方法,所以在test方法中调用的getClass().getName()方法,其实就是在调用从父类继承的getClass()方法,等效于调用super.getClass().getName()方法,所以super.getClass().getName()方法返回的也应该是Example\n如果想得到父类的名称,应该用以下的代码:getClass().getSuperClass().getName();', null);
INSERT INTO `question` VALUES ('297', '7', '以下哪些方法在Class类中定义？', 'A. getConstructors(),B. getPrivateMethods(),C. getDeclaredFields(),D. getImports()', 'A、C', '', null);
INSERT INTO `question` VALUES ('298', '7', '以下哪些说法正确？', 'A. 动态代理类与静态代理类一样，必须由开发人员编写源代码，并编译成.class文件,B. 代理类与被代理类具有同样的接口,C. java.lang.Exception类实现了java.io.Serializable接口，因此Exception对象可以被序列化后在网络上传输,D. java.lang.reflect包中的Proxy类提供了创建动态代理类的方法', 'B、C、D', '', null);
INSERT INTO `question` VALUES ('299', '7', '以下哪些属于动态代理类的特点？', 'A. 动态代理类是public、final和非抽象类型的,B. 动态代理类实现了getProxyClass()或newProxyInstance()方法中参数interfaces 指定的所有接口,C. 动态代理类可以继承用户自定义的任意类,D. 动态代理类都具有一个public 类型的构造方法，该构造方法有一个\nInvocationHandler 类型的参数', 'A、B、D', '', null);
INSERT INTO `question` VALUES ('300', '6', '以下哪个是Runnable接口中定义的方法？', 'A. start(),B. run(),C. stop(),D. yield()', 'B', '', null);
INSERT INTO `question` VALUES ('301', '6', '以下哪个描述是正确的？', 'A. 多线程是Java语言独有的,B. 多线程需要多CPU,C. 多线程要求一个计算机拥有单独一个CPU,D. Java语言支持多线程', 'D', '', null);
INSERT INTO `question` VALUES ('302', '6', '当线程在IO处堵塞时，以下哪些描述正确？', 'A. 线程进入准备状态,B. 线程进入消亡状态,C. 没有其他线程可以完成IO操作,D. 线程进入等待状态', 'D', '', null);
INSERT INTO `question` VALUES ('303', '6', '以下哪个方法可以启动一个线程', 'A. start(),B. init（）,C. run(),D. main()', 'A', '', null);
INSERT INTO `question` VALUES ('304', '6', '请问以下哪个描述是正确的？', 'A. 只有线程具有锁,B. 类的对象都具有锁,C. 基本数据类型具有锁,D. 只有Runnable对象具有锁', 'B', '', null);
INSERT INTO `question` VALUES ('305', '6', '以下哪些描述是正确的？', 'A. 调用sleep()方法使线程进入就绪状态,B. 调用sleep()方法使线程进入等待状态,C. 调用start()方式使线程立即获得执行,D. 调用wait()方法是线程进入就绪状态', 'B', '', null);
INSERT INTO `question` VALUES ('306', '6', '当一个处于阻塞状态的线程解除阻塞后，它将回到那个状态？', 'A. 运行状态,B. 结束状态,C. 新建状态,D. 就绪状态', 'D', '', null);
INSERT INTO `question` VALUES ('307', '6', '线程的默认优先级是哪项？', 'A. 0,B. 1,C. 5,D. 10', 'C', '', null);
INSERT INTO `question` VALUES ('308', '6', '以下代码的执行结果是？\npublic class Example implements Runnable {\n public static void main(String args[]) {\n  Example ex = new Example();\n  Thread t = new Thread(ex);\n  t.start();\n }\n\n void run() {\n  System.out.print(\"pong\");\n }\n}', 'A. 输出pong,B. 运行时输出异常信息,C. 运行后无任何输出,D. 编译失败', 'D', 'run()方法应该是public的', null);
INSERT INTO `question` VALUES ('309', '6', '为了保证方法的线程安全，声明方法的时候必须使用哪个修饰符？', 'A. new,B. transient,C. void,D. synchronized', 'D', '', null);
INSERT INTO `question` VALUES ('310', '6', '现有：t是一个合法的Thread对象的引用，并且t的合法run()方法如下：\n\n public void run() {\n  System.out.print(\"go\");\n }\n执行：\nt.start();\nt.start();\nt.run();\n后结果是什么？', 'A. go go,B. go go go,C. go之后跟着一个异常,D. go go之后跟着一个异常', 'C', '线程重复启动了', null);
INSERT INTO `question` VALUES ('311', '6', '现有代码：\npublic class Example implements Runnable {\n public static void main(String args[]) {\n  new Thread(new Example()).start();\n  try {\n   int x = Integer.parseInt(args[0]);\n   Thread.sleep(x);\n  } catch (Exception e) {\n   // TODO: handle exception\n  }\n }\n\n public void run() {\n  throw new RuntimeException(\"Exception\");\n }\n}\n运行命令 java Example 1000后结果是什么？', 'A. main,B. 编译失败,C. RuntimeException：exception\nmain,D. 无输出', 'C', '', null);
INSERT INTO `question` VALUES ('312', '6', '请问wait()方法定义在以下哪个类上？', 'A. Applet,B. Runnable,C. Thread,D. Object', 'D', '', null);
INSERT INTO `question` VALUES ('313', '6', '请问wait()方法在以下哪个代码中被调用？', 'A. 一个while()循环体中,B. run方法中,C. 同步化代码块中,D. 代码的任何地方', 'C', '', null);
INSERT INTO `question` VALUES ('314', '6', '下列代码的执行结果是？\npublic class Example{\n public static void main(String args[]) {\n\n  Thread t = new Thread() {\n   public void run() {\n    pong();\n   }\n  };\n  t.run();\n  System.out.print(\"ping\");\n }\n\n static void pong() {\n  System.out.print(\"pong\");\n }\n}', 'A. pingpong,B. pongping,C. pingpong和pongping都有可能,D. 都不输出', 'B', 'start()用来启动一个线程，当调用start方法后，系统才会开启一个新的线程，进而调用run()方法来执行任务，而单独的调用run()就跟调用普通方法是一样的，已经失去线程的特性了。因此在启动一个线程的时候一定要使用start()而不是run()。', null);
INSERT INTO `question` VALUES ('315', '6', '以下哪个关于Runnable的描述是正确的？', 'A. Runnable是Java语言的一个关键字，用于修饰类，来表明该类是一个独立线程,B. Runnable是一个接口，实现该接口的类对象可以提供给Thread类构造器作为创建线程的依据,C. Runnable是一个类，继承该类的子类可以作为独立的线程存在,D. 以上皆不对', 'B', '', null);
INSERT INTO `question` VALUES ('316', '6', '以下代码的执行结果是？\npublic class Example implements Runnable {\n\n public static void main(String[] args) {\n  Thread t = new Thread(new Example());\n  t.start();\n }\n\n public void run(int limit) {\n  for (int x = 0; x < limit; x++) {\n   System.out.println(x);\n  }\n }\n}', 'A. 输出从0至limit,B. 无内容输出，因为没有明确调用run()方法,C. 代码编译失败，因为没有正确实现Runnable接口,D. 代码编译失败，如果声明为抽象类，可以使代码编译成功', 'C', '', null);
INSERT INTO `question` VALUES ('317', '6', '以下代码的执行结果是？\npublic class Example implements Runnable {\n\n public static void main(String[] args) {\n  Example ex1 = new Example();\n  Example ex2 = new Example();\n  Example ex3 = new Example();\n  \n  ex1.run();\n  ex2.run();\n  ex3.run();\n }\n\n public void run() {\n  while (true) {\n   System.out.println(Thread.currentThread().getName());\n   try {\n    Thread.sleep(100);\n   } catch (InterruptedException e) {\n    // TODO Auto-generated catch block\n    e.printStackTrace();\n   }\n  }\n }\n}', 'A. 代码编译失败，因为ex2.run()无法获得执行,B. 代码编译成功，存在3个可运行的线程,C. 代码编译成功，仅存在1个可运行的线程,D. 代码编译成功，循环交替输出不同的线程名', 'C', '没有使用start()方法启动线程，而是直接调用的run方法', null);
INSERT INTO `question` VALUES ('318', '7', '请问以下哪些是有关线程状态转换的正确描述？', 'A. 从就绪状态转换到运行状态,B. 从运行状态转换到就绪状态,C. 从运行状态转换到等待状态,D. 从等待状态转换到就绪状态', 'A、B、C、D', '', null);
INSERT INTO `question` VALUES ('319', '7', '如何定义一个类作为线程使用', 'A. 继承Thread类,B. 实现Throwable接口,C. 实现Multithread接口,D. 实现Runnable接口', 'A、D', '', null);
INSERT INTO `question` VALUES ('320', '7', '请问以下哪些描述是正确的？', 'A. wait()方法和notify()方法是Thread类声明的,B. wait()方法和notify()方法是在Object类中定义的,C. 只有同步化的类支持wait()方法和notify（）方法,D. 在JDK1.2中废除了wait()方法和notify()方法', 'A、B', '', null);
INSERT INTO `question` VALUES ('321', '7', '以下那些是线程停止执行的原因？', 'A. 较高优先级的线程开始执行,B. 在线程中调用了某个对象的wait()方法,C. 线程的yield()方法被调用,D. 线程的sleep()方法被调用', 'A、B、C、D', '', null);
INSERT INTO `question` VALUES ('322', '7', '以下哪些方法可以用于将一个正在执行的线程停止执行？', 'A. wait(),B. notify(),C. yield(),D. suspend()', 'A、C、D', '', null);
INSERT INTO `question` VALUES ('323', '6', '在服务器www.chinaosfti.com上提供了基于TCP的时间服务应用，该应用使用port为6666。创建连接到此服务器的语句是?', 'A. Socket s = new Socket(\"www.chinaosfti.com\", 6666);,B. Socket s = new Socket(\"www.chinaosfti.com:6666\");,C. Socket s =Socket.accept(\"www.chinaosfti.com\", 6666);,D. Socket s =Socket.accept(\"www.chinaosfti.com:6666\");', 'A', '', null);
INSERT INTO `question` VALUES ('324', '7', 'Java UDP编程主要用到的两个类型是', 'A. UDPSocket,B. DatagramSocket,C. UDPPacket,D. DatagramPacket', 'B、D', '', null);

-- ----------------------------
-- Table structure for `questiontype`
-- ----------------------------
DROP TABLE IF EXISTS `questiontype`;
CREATE TABLE `questiontype` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `questionTypeCode` varchar(500) DEFAULT NULL,
  `questionTypeName` varchar(500) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=11 DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of questiontype
-- ----------------------------
INSERT INTO `questiontype` VALUES ('6', 'DANXUANTI', '单选题');
INSERT INTO `questiontype` VALUES ('7', 'DUOXUANTI', '多选题');
INSERT INTO `questiontype` VALUES ('8', 'TIANKONGTI', '填空题');
INSERT INTO `questiontype` VALUES ('9', 'PANDUANTI', '判断题');
INSERT INTO `questiontype` VALUES ('10', 'JIEDATI', '解答题');

-- ----------------------------
-- Table structure for `tauth`
-- ----------------------------
DROP TABLE IF EXISTS `tauth`;
CREATE TABLE `tauth` (
  `CID` varchar(36) NOT NULL,
  `CDESC` varchar(200) DEFAULT NULL,
  `CNAME` varchar(100) NOT NULL,
  `CSEQ` decimal(22,0) DEFAULT NULL,
  `CURL` varchar(200) DEFAULT NULL,
  `CPID` varchar(36) DEFAULT NULL,
  PRIMARY KEY (`CID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of tauth
-- ----------------------------
INSERT INTO `tauth` VALUES ('0', '', '首页', '1', null, null);
INSERT INTO `tauth` VALUES ('cdadd', null, '菜单添加', '4', '/admin/menu/add.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cdaddym', null, '添加菜单页面', '3', '/admin/menu/menuAdd.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cdcx', null, '菜单查询', '2', '/admin/menu/treegrid.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cddelete', null, '菜单删除', '7', '/admin/menu/remove.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cdedit', null, '菜单编辑', '6', '/admin/menu/edit.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cdeditym', null, '编辑菜单页面', '5', '/admin/menu/menuEdit.do', 'cdgl');
INSERT INTO `tauth` VALUES ('cdgl', null, '菜单管理', '4', null, 'xtgl');
INSERT INTO `tauth` VALUES ('cdglym', null, '菜单管理页面', '1', '/admin/menu/menu.do', 'cdgl');
INSERT INTO `tauth` VALUES ('jsadd', null, '角色添加', '4', '/admin/role/add.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jsaddym', null, '添加角色页面', '3', '/admin/role/roleAdd.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jscx', null, '角色查询', '2', '/admin/role/datagrid.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jsdelete', null, '角色删除', '7', '/admin/role/remove.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jsedit', null, '角色编辑', '6', '/admin/role/edit.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jseditym', null, '编辑角色页面', '5', '/admin/role/roleEdit.do', 'jsgl');
INSERT INTO `tauth` VALUES ('jsgl', null, '角色管理', '2', null, 'xtgl');
INSERT INTO `tauth` VALUES ('jsglym', null, '角色管理页面', '1', '/admin/role/role.do', 'jsgl');
INSERT INTO `tauth` VALUES ('qxadd', null, '权限添加', '4', '/admin/auth/add.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxaddym', null, '添加权限页面', '3', '/admin/auth/authAdd.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxcx', null, '权限查询', '2', '/admin/auth/treegrid.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxdelete', null, '权限删除', '7', '/admin/auth/remove.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxedit', null, '权限编辑', '6', '/admin/auth/edit.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxeditym', null, '编辑权限页面', '5', '/admin/auth/authEdit.do', 'qxgl');
INSERT INTO `tauth` VALUES ('qxgl', null, '权限管理', '3', null, 'xtgl');
INSERT INTO `tauth` VALUES ('qxglym', null, '权限管理页面', '1', '/admin/auth/auth.do', 'qxgl');
INSERT INTO `tauth` VALUES ('xtgl', null, '系统管理', '1', null, '0');
INSERT INTO `tauth` VALUES ('yhadd', null, '用户添加', '4', '/admin/user/add.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhaddym', null, '添加用户页面', '3', '/admin/user/userAdd.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhcx', null, '用户查询', '2', '/admin/user/datagrid.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhedit', null, '用户修改', '6', '/admin/user/edit.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yheditym', null, '修改用户页面', '5', '/admin/user/userEdit.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhgl', null, '用户管理', '1', null, 'xtgl');
INSERT INTO `tauth` VALUES ('yhglym', '', '用户管理页面', '1', '/admin/user/user.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhsc', null, '用户删除', '7', '/admin/user/remove.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhxgjs', '批量修改用户角色', '修改角色', '9', '/admin/role/roleEdit.do', 'yhgl');
INSERT INTO `tauth` VALUES ('yhxgjsym', '批量修改用户角色', '修改角色页面', '8', '/admin/user/userRoleEdit.do', 'yhgl');

-- ----------------------------
-- Table structure for `tmenu`
-- ----------------------------
DROP TABLE IF EXISTS `tmenu`;
CREATE TABLE `tmenu` (
  `CID` varchar(36) NOT NULL,
  `CICONCLS` varchar(100) DEFAULT NULL,
  `CNAME` varchar(100) NOT NULL,
  `CSEQ` decimal(22,0) DEFAULT NULL,
  `CURL` varchar(200) DEFAULT NULL,
  `CPID` varchar(36) DEFAULT NULL,
  PRIMARY KEY (`CID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of tmenu
-- ----------------------------
INSERT INTO `tmenu` VALUES ('0', null, '首页', '1', null, null);
INSERT INTO `tmenu` VALUES ('bjgl', null, '班级管理', '1', '/education/clazz/clazz.do', 'jwgl');
INSERT INTO `tmenu` VALUES ('cdgl', null, '菜单管理', '4', '/admin/menu/menu.do', 'xtgl');
INSERT INTO `tmenu` VALUES ('cjcx', null, '成绩查询', '1', '/score/score/scoreHistory.do', 'cjfx');
INSERT INTO `tmenu` VALUES ('cjfx', null, '成绩分析', '5', null, '0');
INSERT INTO `tmenu` VALUES ('fbsj', null, '发布试卷', '2', '/settings/test/test.do', 'sjgl');
INSERT INTO `tmenu` VALUES ('fstj', null, '分数统计', '3', '/score/score/scoreSpread.do', 'cjfx');
INSERT INTO `tmenu` VALUES ('jsgl', null, '角色管理', '2', '/admin/role/role.do', 'xtgl');
INSERT INTO `tmenu` VALUES ('jwgl', null, '教务管理', '2', null, '0');
INSERT INTO `tmenu` VALUES ('ksgl', null, '考试管理', '6', null, '0');
INSERT INTO `tmenu` VALUES ('ksxx', null, '考生信息', '1', '/education/student/notNeedAuth_studentInfo.do', 'ksgl');
INSERT INTO `tmenu` VALUES ('pzsj', null, '配置试卷', '1', '/questionManage/questionConfig/questionConfig.do', 'sjgl');
INSERT INTO `tmenu` VALUES ('qsfx', null, '趋势分析', '2', '/score/score/scoreTrend.do', 'cjfx');
INSERT INTO `tmenu` VALUES ('qxgl', null, '权限管理', '3', '/admin/auth/auth.do', 'xtgl');
INSERT INTO `tmenu` VALUES ('sjcx', null, '试卷查询', '2', '/score/score/notNeedAuth_score.do', 'ksgl');
INSERT INTO `tmenu` VALUES ('sjgl', null, '试卷管理', '4', null, '0');
INSERT INTO `tmenu` VALUES ('sjk', null, '数据库', '7', null, '0');
INSERT INTO `tmenu` VALUES ('sjkjk', null, '数据库监控', '1', '/druid/index.html', 'sjk');
INSERT INTO `tmenu` VALUES ('stgl', null, '试题管理', '3', '', '0');
INSERT INTO `tmenu` VALUES ('sttk', null, '试题题库', '2', '/question/question/question.do', 'stgl');
INSERT INTO `tmenu` VALUES ('tklx', null, '题库类型', '1', '/question/questionType/questionType.do', 'stgl');
INSERT INTO `tmenu` VALUES ('xtgl', null, '系统管理', '1', null, '0');
INSERT INTO `tmenu` VALUES ('xygl', null, '学员管理', '2', '/education/student/student.do', 'jwgl');
INSERT INTO `tmenu` VALUES ('yhgl', null, '用户管理', '1', '/admin/user/user.do', 'xtgl');

-- ----------------------------
-- Table structure for `trole`
-- ----------------------------
DROP TABLE IF EXISTS `trole`;
CREATE TABLE `trole` (
  `CID` varchar(36) NOT NULL,
  `CDESC` varchar(200) DEFAULT NULL,
  `CNAME` varchar(100) NOT NULL,
  PRIMARY KEY (`CID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of trole
-- ----------------------------
INSERT INTO `trole` VALUES ('001', '所有权限', '管理员');
INSERT INTO `trole` VALUES ('002', '来宾账户', 'Guest');

-- ----------------------------
-- Table structure for `troletauth`
-- ----------------------------
DROP TABLE IF EXISTS `troletauth`;
CREATE TABLE `troletauth` (
  `CAUTHID` varchar(36) DEFAULT NULL,
  `CROLEID` varchar(36) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of troletauth
-- ----------------------------
INSERT INTO `troletauth` VALUES ('0', '001');
INSERT INTO `troletauth` VALUES ('xtgl', '001');
INSERT INTO `troletauth` VALUES ('yhgl', '001');
INSERT INTO `troletauth` VALUES ('yhglym', '001');
INSERT INTO `troletauth` VALUES ('yhcx', '001');
INSERT INTO `troletauth` VALUES ('yhaddym', '001');
INSERT INTO `troletauth` VALUES ('yhadd', '001');
INSERT INTO `troletauth` VALUES ('yheditym', '001');
INSERT INTO `troletauth` VALUES ('yhedit', '001');
INSERT INTO `troletauth` VALUES ('yhsc', '001');
INSERT INTO `troletauth` VALUES ('yhxgjsym', '001');
INSERT INTO `troletauth` VALUES ('yhxgjs', '001');
INSERT INTO `troletauth` VALUES ('jsgl', '001');
INSERT INTO `troletauth` VALUES ('jsglym', '001');
INSERT INTO `troletauth` VALUES ('jscx', '001');
INSERT INTO `troletauth` VALUES ('jsaddym', '001');
INSERT INTO `troletauth` VALUES ('jsadd', '001');
INSERT INTO `troletauth` VALUES ('jseditym', '001');
INSERT INTO `troletauth` VALUES ('jsedit', '001');
INSERT INTO `troletauth` VALUES ('jsdelete', '001');
INSERT INTO `troletauth` VALUES ('qxgl', '001');
INSERT INTO `troletauth` VALUES ('qxglym', '001');
INSERT INTO `troletauth` VALUES ('qxcx', '001');
INSERT INTO `troletauth` VALUES ('qxaddym', '001');
INSERT INTO `troletauth` VALUES ('qxadd', '001');
INSERT INTO `troletauth` VALUES ('qxeditym', '001');
INSERT INTO `troletauth` VALUES ('qxedit', '001');
INSERT INTO `troletauth` VALUES ('qxdelete', '001');
INSERT INTO `troletauth` VALUES ('cdgl', '001');
INSERT INTO `troletauth` VALUES ('cdglym', '001');
INSERT INTO `troletauth` VALUES ('cdcx', '001');
INSERT INTO `troletauth` VALUES ('cdaddym', '001');
INSERT INTO `troletauth` VALUES ('cdadd', '001');
INSERT INTO `troletauth` VALUES ('cdeditym', '001');
INSERT INTO `troletauth` VALUES ('cdedit', '001');
INSERT INTO `troletauth` VALUES ('cddelete', '001');
INSERT INTO `troletauth` VALUES ('yhglym', '002');
INSERT INTO `troletauth` VALUES ('yhcx', '002');

-- ----------------------------
-- Table structure for `tuser`
-- ----------------------------
DROP TABLE IF EXISTS `tuser`;
CREATE TABLE `tuser` (
  `cid` varchar(36) NOT NULL,
  `cname` varchar(100) DEFAULT NULL,
  `cpwd` varchar(128) DEFAULT NULL,
  `createid` varchar(36) DEFAULT NULL,
  `createtime` datetime DEFAULT NULL,
  `modifyid` varchar(36) DEFAULT NULL,
  `modifytime` datetime DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of tuser
-- ----------------------------
INSERT INTO `tuser` VALUES ('admin', '管理员', '21232f297a57a5a743894a0e4a801fc3', '', null, 'admin/管理员', '2017-10-12 09:07:14');

-- ----------------------------
-- Table structure for `tusertrole`
-- ----------------------------
DROP TABLE IF EXISTS `tusertrole`;
CREATE TABLE `tusertrole` (
  `CROLEID` varchar(36) DEFAULT NULL,
  `CUSERID` varchar(36) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

-- ----------------------------
-- Records of tusertrole
-- ----------------------------
INSERT INTO `tusertrole` VALUES ('001', 'admin');
INSERT INTO `tusertrole` VALUES ('002', 'user');
INSERT INTO `tusertrole` VALUES ('001', 'zhangwei');
INSERT INTO `tusertrole` VALUES ('002', 'guest');
INSERT INTO `tusertrole` VALUES ('001', '11');
INSERT INTO `tusertrole` VALUES ('002', 'test');
INSERT INTO `tusertrole` VALUES ('002', 'test');
INSERT INTO `tusertrole` VALUES ('002', 'tt');
