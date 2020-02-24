# C++从入门到精通 C++11/14/17
`-网易云课堂`
## Content
- 一、基本语言
	- 01 语言特性、工程构成、可移植性
	- 02 命名空间简介、基本输入输出精解
	- 03 auto、头文件防卫、引用、常量
	- 04 范围for、new内存动态分配、nullptr
	- 05结构、权限修饰符、类简介
	- 06 函数新特性、内联函数、const详解
	- 07 string类型介绍
	- 08 vector类型介绍
	- 09 迭代器精彩演绎、失效分析及弥补、实战
	- 10 类型转换：static_cast、reinterpret_cast等
- 二、类
	- 01 成员函数、对象拷贝、私有成员
	- 02 构造函数详解、explicit、初始化列表
	- 03 inline、const、mutable、this、static
	- 04 类内初始化、默认构造函数、=default;
	- 05 拷贝构造函数
	- 06 重载运算符、拷贝赋值运算符、析构函数
	- 07 派生类、调用顺序、访问等级、函数遮蔽
	- 08 基类指针、虚纯虚函数、多态性、虚析构
	- 09 友元函数、友元类、友元成员函数
	- 10 RTTI、dynamic_cast、typeid、虚函数表
	- 11 基类与派生类关系的详细🔎再探讨
	- 12 左值、右值，左值引用、右值引用、move
	- 13 临时对象深入探讨、解析，提高性能手段
	- 14 对象移动、移动构造函数、移动赋值运算符
	- 15 继承的构造函数、多重继承、虚继承
	- 16 类型转换构造函数、运算符，类成员指针
- 三、模版与泛型
	- 01 模版概念，函数模版定义、调用
	- 02 类模版概念，类模版定义、使用
	- 03 用typename场合、默认模版参数、趣味写法分析
	- 04 成员函数模版，显式实例化、声明
	- 05 using定义模版别名，显式制定模版参数
	- 06 模版全特化、偏特化(局部特化)
	- 07 可变参模版
	- 08 可变参模版续、模版参数
- 四、智能指针
	- 01 直接内存管理(new/delete)、创建新工程观察内存泄漏
	- 02 new、delete探秘，智能指针概述、shared_ptr基础
	- 03 shared_ptr常用操作、计数、自定义删除器等
	- 04 weak_ptr概述、weak_ptr常用操作、尺寸
	- 05 shared_ptr使用场景、陷阱、性能分析、使用建议
	- 06 unique_ptr概述、常用操作
	- 07 返回unique_ptr、删除器、尺寸、智能指针总结
- 五、并发与多线程
	- 01 并发基本概念及实现，进程、线程基本概念
	- 02 线程启动、结束，创建线程多法、join，detach
	- 03 线程传参详解，detach()大坑，成员函数做线程函数
	- 04 创建多个线程、数据共享问题分析、案例代码
	- 05 互斥量概念、用法、死锁演示及解决详解
	- 06 unique_lock详解
	- 07 单例设计模式共享数据分析、解决，call_once
	- 08 condition_variable、wait、notify_one、notify_all
	- 09 async、future、packaged_task、promise
	- 10 future其他成员函数、shared_future、atomic
	- 11 std::atomic续谈、std::async深入谈
	- 12 windows临界区、其他各种mutex互斥量
	- 13 补充知识、线程池浅谈、数量谈、总结
- 六、内存高级话题
	- 01 new、delete的进一步认识
	- 02 new细节探秘、重载类内operator new、delete
	- 03 内存池概念、代码实现和详细分析
	- 04 嵌入式指针概念及范例、内存池改进版
	- 05 重载全局new、delete，定位new及重载等
- 七、STL标准模版库大局观
	- 01 STL总述、发展史、组成、数据结构谈
	- 02 容器分类、array、vector容器精解
	- 03 容器的说明和简单应用例续
	- 04 分配器概述、使用，工作原理
	- 05 迭代器的概念和分类
	- 06 算法概述、内部处理、使用范例
	- 07 函数对象回顾、系统函数对象及范例
	- 08 适配器概念、分类、范例及总结
- 八、未归类知识点
	- 01 函数调用运算符、function类模版
	- 02 万能引用universal reference
	- 03 理解模版类型推断、查看类型推断结果
	- 04 引用折叠，转发、完美转发，forward
	- 05 理解auto类型推断，auto应用场合
	- 06 详解decltype含义，decltype主要用途
	- 07 可调用对象、std::function、std::bind
	- 08 lambda表达式，for_each、find_if简介
	- 09 lambda表达式捕获模式的陷阱分析和展示
	- 10 可变参数函数、initializer_list、省略号形参
	- 11 萃取(traits)技术概念、范例等
***
# 一、基本语言

## 01 语言特性、工程构成、可移植性

- Ｃ语言 <==> C++

- 面向过程式的程序设计 <==> 基于对象/面向对象的程序设计

- 结构体 <==> 类

- 结构变量 <==> 对象



`cstdio` 是将stdio.h的内容用C++头文件的形式表示出来。

cstdio是标准C++(STL)，且cstdio中的函数都是定义在一个名称空间std里面的，如果要调用这个名字空间的函数，必须得加std::或者在文件中声明using namespace std。



## 02 命名空间简介、基本输入输出精解
> 1 命名空间概念简介
> 2 基本输入输出cin、cout精解


#### 命名空间概念简介

**命名空间**：是为了防止名字冲突而引入的一种机制。系统中可以定义多个命名空间，在不同命名空间内定义的函数，即便同名，也互不影响。



**命名空间的定义**



```c
namespace 命名空间名
{
	...
}	//命名空间的定义可以不连续，可以写在一个解决方案的多个.cpp文件内
```



**如何访问命名空间中的对象**



```c
命名空间名::实体名

using namespace 命名空间名;
```

`::`叫做**作用域运算符**



#### 基本输入输出cin、cout精解



**`iostream`库(输入输出流)**



```c
#include <iostream>

std::cout << "我又入坑了";
```

1. `std::命名空间`，std是标准库命名空间

2. `cout`(console output)，控制台输出，“标准输出”对象

3. `<<`：**流插入运算符**。“输出”运算符，在这里被重载，不是位运算的左移



```c
std::cout << x << "的平方是" << x*x << "\n";
std::cout << x << "的平方是" << x*x << std::endl;
```

`std::endl`是一个模版函数名，相当于函数指针，一般都位于`std::cout`语句的末尾

作用：

1. 输出换行符`\n`

2. 强制刷新输出缓冲区



```c
std:cout << "请输入两个数字：" << std::endl;
int value1, value 2;
std::cin >> value1 >> value2
std::cout << value1 << "和" << value2 << "的和是：" << value1+value2 << std::endl;
```

1. `cin`(console input)，“标准输入”对象，可用来替代scanf

2. `>>`：**流提取运算符**。“输入”运算符

3. 返回其左侧运算对象作为其计算结果



## 03 auto、头文件防卫、引用、常量
> 1 局部变量及初始化
> 2 auto
> 3 头文件防卫式声明
> 4 引用
> 5 常量
#### 局部变量及初始化

###### 随时用到随时定义



```c
//C++中定义时初始化
int i { 0 };	//等同于int i = 0;
int a[] {1, 2, 3};
```

#### auto：变量的自动类型推断

auto可以在变量声明的时候根据变量初始值的类型自动为此变量选择匹配的类型(声明时要初始化)；auto自动类型推断发生在编译期间，不会造成程序效率降低。



```c
auto value = true;	//自动推断成bool
auto b { 3.5f };	//自动推断为浮点型
```

#### 头文件防卫式声明



```c
//head1.h
#ifndef __HEAD1__H__
#define __HEAD1__H__

//语句

#endif
```

避免在同一个文件内包含多次同一个头文件，因为在第二次`#include`时，该标识符(常用文件名大写，如：`__HEAD1__H__`)已被定义，`#ifndef`判定False，则不会执行下面语句。

#### 引用



```c
int value { 10 };
int &refval = value;
```

为变量起了另外一个名字，一般用&符号标识。

#### 常量

`const`关键字和`constexpr`关键字



```c
const int var = 7;
constexpr int var2 = 8;	//const和constexpr(C++11新标准)声明了该变量不改变
```

## 04 范围for、new内存动态分配、nullptr

> 1 范围for语句
> 2 动态内存分配问题
> 3 nullptr

#### 范围for语句

```c
int v[] { 1, 2, 3, 4 };
for (auto x : v)
{
	std::cout << x << std::endl;
}	//每次将v拷贝到x中
for (auto &x : v)
{
	std::cout << x << std::endl;
}	//用引用的功能剩去了拷贝，提高了系统效率
```

#### 动态内存分配问题

在上一系列C语言的讲解中，把内存分为了程序区、静态存储区、动态存储区三个区域；C++中，我们把内存进一步分为五个区域：

1. **栈**：一般函数内的局部变量都会放在这里，由编译器自动分配和释放；

2. **堆**：程序员malloc/new分配，用free/delete来释放。忘记释放后，系统会回收；

3. **全局/静态存储区**：放全局变量和静态变量static。程序结束时系统释放；

4. **常量存储区**

5. **程序代码区**



**堆和栈不同的用途和区别**

1. 栈 空间是有限的，分配速度快；

2. 堆 只要不超出实际拥有的物理内存，也在操作系统允许能够分配的内存大小之内都可以分配，分配速度比栈慢



在C语言中，用`malloc`和`free`从堆中分配和释放内存用。`malloc`和`free`是函数；`new`和`delete`是关键字。



`malloc`**(memory allocation)：动态内存分配**

**一般形式**：



```c
void *malloc(int NumBytes);	//NumBytes：要分配的字节数。
// 分配成功则返回指向被分配内存的指针，分配失败则返回NULL。
```

`free`的**一般形式**：



```c
void free(void *FirstByte);	//将之前malloc分配的内存空间还给程序(操作系统)
```

###### 演示的是该函数被定义时的函数声明

**如何使用**`malloc`**和**`free`



```c
int *p = NULL;
p = (int *)malloc(sizeof(int));	//malloc函数返回值是void *万能指针，需要强制类型转换为整型和p相同
if (p != NULL)
{
	*p = 5;
	free(p);	//free的参数是一个指针
}

char *point = NULL;
point = (char *)malloc(100 * sizeof(char));
if (point != NULL)
{
	strcpy_s(point, 100, "hello world");	//strcpy_s有三个参数，第二个参数为占用的字节数
	cout << point << endl;
	free(point);
}
```

**回顾**



```c
char a = 'a';	//char字符型，只能存单个字符
char a[] = "Hi";	//字符数组，用字符串的方式初始化
char *p = "Hi";		//"Hi"是一个字符数组，数组名代表首地址，将首地址给一个字符指针
```

`new`和`delete`：是**运算符**(标识符)。C++中使用new/delete分配和释放内存。

`new`的**一般使用格式**：

1. 指针变量名 = new 类型标识符;

2. 指针变量名 = new 类型标识符(初始值);

3. 指针变量名 = new 类型标识符[内存单元个数];



```c
int *a = new int;
if (a != NULL)
{
	...
	delete a;
}

int *pa = new int[10];
if (pa != NULL)
{
	...
	delete[] pa;
}
```
#### nullptr：C++11引入的关键字

`nullptr`代表的也是空指针。使用nullptr可以避免在整数和指针之间混淆。



```c
//NULL在文档中是这样定义的
#define NULL 0
//而nullptr并不是整形常量0
cout << typeid(NULL).name() << endl;
cout << typeid(nullptr.name() << endl;
//用typeid打印出两个的类型名时
//NULL => int
//nullptr => std::nullptr_t
```

## 05 结构、权限修饰符、类简介

> 1 结构回顾
> 2 public和private权限修饰符
> 3 类简介
> 4 类的组织


#### public和private权限修饰符

> public、private、protected



`public`：用这个修饰符修饰 结构/类中的成员变量/成员函数，就可以被外界访问，好比是该类的外部接口一样。

`private`：用这个修饰符修饰 结构/类中的成员变量/成员函数，只有被内部定义的成员函数才能使用。



```c
struct 结构体名{
public:
	成员;
private:
	成员;
};
```

#### 类简介`class`

在C++️类和结构及其相似，区别有两点：

1. C++结构内部的成员变量和成员函数默认的访问级别都是public；而类内部的成员变量和成员函数默认的访问级别都是private

2. C++结构体继承默认的是public，而C++类的继承默认的是private



#### 类的组织(书写✍️规范)

类的定义代码放在一个.h头文件中，头文件名可以跟类名相同；

类的具体实现代码放在一个.cpp文件中。

## 06 函数特性、内联函数、const详解

> 1 函数回顾与后置返回类型
> 2 内联函数
> 3 函数杂合用法总结
> 4 const char *、char const *、char * const三者的区别
> 5 函数形参中带const



#### 函数回顾与后置返回类型

1. 函数定义中，形参如果在函数体内用不到的话，则可以不给形参变量名字，只给其类型

2. 函数声明时，可以只有形参类型，没有形参名

3. 常见的把返回值类型放在函数名字之前，叫前置返回类型

4. C++11中，提出了后置返回类型，就是将返回值类型放在函数名的后面



```c
auto name(int value) -> void
{
	return;
}
```

#### 内联函数

> 在函数定义前添加`inline`关键字



1. 内联函数适用于函数体很小，调用又很频繁的函数

2. inline影响编译器，在编译阶段对inline这种函数进行处理，系统尝试将调用该函数的动作替换为函数本体。通过这种方式来提升性能

3. inline只是开发者对编译器的一个建议，编译器可以尝试去做，同样也可以不做，取决于编译器的诊断功能

4. **内联函数的定义要放在头文件中**(普通函数是将函数声明放在.h文件中，函数定义放在一个单独的.cpp文件中)



#### 函数杂合用法总结

1. 函数返回类型void，表示函数不返回任何类型。但是我们可以通过调用一个返回类型是void的函数，让它作为另一个返回类型是void的函数的返回值

2. 没有形参可以保存形参列表为️`()`，或者在形参列表里写入void`(void)`

3. 普通函数，定义只能定义一次(放在.cpp文件中)，声明可以声明多次。一般函数定义.cpp文件会#include自己的函数声明文件.h

4. **`void func(int &ta, int &tb)``，在C++中，更习惯用引用类型的形参来取代指针类型的形参**，目的是达到避免值传递拷贝降低效率的目的



#### const char *、char const *、char * const三者的区别

- const char *和char const *是等价的，`const char *p`中p指向的目标不能通过p来修改

- `char * const p`在定义时需要初始化，指针p一旦指向一个目标后，就不能指向其他目标了，~~p++~~



#### 函数形参中带const

1. 在形参前➕`const`可以避免无意修改形参值引起实参值被改变

2. 实参类型可以更灵活



## 07 string类型介绍

> 1 前言
> 2 string类型简介
> 3 定义和初始化string对象
> 4 string对象上的操作



#### string类型简介

C++标准库中的类型，代表一个☝️可变长字符串，当作类类型



```c
#include <string>
```

#### 定义和初始化string对象



```c
string s1;	//默认空串，里面没有字符
string s2 = "It's so terrible";
string s3("It's so terrible");
int num = 6;
string s4(num, 'a');	//连续num个'a' -> "aaaaaa"
```

#### string对象上的操作



```c
using namespace std;	//std命名空间下

string s1;	
s1.empty();	//string当作类，对象的调用方法就是 类.对象
s1.size();
s1.length();
s1[n];	//和字符数组类似
...
```

- `empty()`：判断是否为空，返回布尔值

- `size()`/`length()`：返回字节/字符数量，代表该字符串的长度

- `s[n]`：返回s中的第n个字符

- `s1+s2+" "`：字符串的连接，返回连接后的结果，得到一个新的string对象(strcat)

- `s1 = s2`：字符串对象赋值，用s2里面的内容取代原来s1的内容(strcpy)

- `s1 == s2`：判断两个字符串是否相等(strcmp)

- `s1 != s2`：判断两个字符串是否不等

- `s.c_str`：返回一个字符串s中的内容指针。这个函数的引入是为了与C语言兼容



```c
string s1 = "abc";
const char *p  = s1.c_str();	//返回的指针改动
char str[100];
strcpy_s(str, sizeof(str), p);	//abc
```

- 范围for针对string的使用：能够遍历一个序列中的每一个元素



```c
string s1 = "HeiHei";
for (auto c : s1)
{
	cout << c << endl;
}
for (auto &c : s1)
{
	//引用类型可以修改string的值
	//toupper把小写字母改变成大写字母
	c = toupper(c);
}
```
## 08 vector类型介绍

> 1 vector类型简介
> 2 定义和初始化vector对象
> 3 vector对象上的操作

#### vector类型简介

标准库：**集合或者动态数组**。可以把若干对象放在里面。

vector也被称作**容器**。



```c
#include <vector>
using namespace std
vector<int> contain;

struct student {
	int num;
};
vector<student> stulist;
```

`<int>`类模版，vector本身就是类模版，`<int>`实际上就是类模版实例化的过程。

###### vector内部不能装引用类型。

#### 定义和初始化vector对象



```c
//1.空vector
vector<string> mystr;
//2.元素拷贝
vector<string> mystr2(mystr);
vector<string> mystr2 = mystr;
//3.C++11标准中，列表初始化
vector<string> mystr3 = {"aaa", "bbb", "ccc"};
//4.创建指定数量的元素。有元素数量概念的东西，一般会用圆括号
vector<string> mystr4(5, "hehe");	//创建5个元素，每个都是hehe
```

#### vector对象⬆️的操作

- `empty()`判断是否为️，返回布尔值

- `push_back()`**常用方法，用于向vector末尾增加一个元素**

- `insert( , )`：插入新值，第一个参数为插入位置，第二个为插入的元素(位置用迭代器来表示)

- `erase()`：删除该位置上的值(位置用迭代器来表示)

- `size()`返回元素个数

- `clear()`移除所有元素，将容器清空

- `v[n]`返回v的第n个元素

- `=`赋值

- `==` `!=`相等、不等，元素数量和对应位置的元素值都比较

- *范围for的应用*



```c
vector<int> vecvalue{1, 2, 3, 4, 5};
for (auto &vecitem : vecvalue)
{
	vecitem * 2;
}
```
*范围for结论：在for语句中(遍历一个容器等等类似操作中)，不能改动vector容器的容量，增加/删除都不可以。*

## 09 迭代器精彩演绎，失效分析及弥补、实战

> 1 迭代器简介
> 2 容器的迭代器类型
> 3 迭代器begin()/end()操作，反向迭代器rbegin()/rend()操作
> 4 迭代器运算符
> 5 const_iterator迭代器
> 6 迭代器失效
> 7 范例演示

#### 迭代器简介

迭代器是一种**遍历容器内元素的数据类型**，理解的时候就理解为迭代器用来指向容器中的某个元素。`[]`下标的方式，迭代器更**常用**。通过迭代器，我们可以读取容器中的元素值，读string中的每个字符，还可以修改某个迭代器所指向的元素值。

#### 容器的迭代器类型



```c
//std是一个命名空间	string、vector是类
vector<int> iv = {100, 200 ,300};
vector<int>::iterator iter;	//定义迭代器
```
为了方便理解，我们把`vector<int>::iterator`理解为一个类型，使用该类型定义的变量，就是一个迭代器。

#### 迭代器begin()/end()操作，反向迭代器rbegin()/rend()操作

> begin()/end()、rbegin()/rend()都用来返回迭代类型



```c
//如果容器中有元素，则begin返回的迭代器，指向的是容器中的第一个元素也就是iv[0]
vector<int>::iterator iter;
iter = iv.begin();
iter = iv.end();	//end返回的迭代器指向的并不是末端元素，而是末端元素的后面，是一个不存在的元素
```

如果容器为️，那么begin和end指向相同。

##### 传统迭代器遍历使用方法



```c
vector<int> iv = {100, 200 ,300};
for (vector<int>::iterator iter = iv.begin(); iter != iv.end(); iter++)
{
	cout << *iter << endl;
}
```

##### 反向迭代器(逆向迭代器)



```c
vector<int>::reverse_iterator iter_reverse;
for (vector<int>::reverse_iterator iter_reverse = iv.rbegin(); iter_reverse != iv.rend(); iter_reverse++)
{
	cout << *iter_reverse << endl;
}
```

#### 迭代器运算符

- `*iter`：返回迭代器iter所指向元素的引用。必须保证这个迭代器指向的是有效的容器元素

- `++iter` `iter++`：让迭代器指向容器中下一个元素

- `--iter` `iter--`：指向容器上一个元素



```c
struct student
{
	int num;
};
student stu1;
stu1.num = 2018100043;

vector<student> sv;
sv.push_back(stu1);
vector<student>::iterator iter = sv.begin();
cout << (*iter).num << endl;
//cout << iter->num << endl;
```

#### const_iterator迭代器

const_iterator迭代器，表示迭代器指向的元素值不能改变，但是可以不断指向下一个元素。只能从容器中读元素。



```c
vector<int>::const_iterator iter;
```

##### cbegin和cend操作

> C++11引入的函数，返回的都是常量迭代器



```c
for (auto iter = sv.cbegin(), iter != sv.cend(), iter++)
{
	cout << *iter << endl;
}
```
用`auto`替代`vector<int>::const_iterator`简化代码
#### 迭代器失效

在操作迭代器的过程中(使用了迭代器这种循环体♻️)，千万不要改变容器的容量，也就是不要增加或者删除容器中的元素。



```c
//解决在迭代器内插入数据的方法(避免使用)
vector<int> value {1, 2, 3, 4};
vector<int>::iterator beg = value.begin();
int icount = 0;
while (beg != value.end())
{
	beg = value.insert(beg, icount + 100);	//insert( , )第一个参数是位置
	icount++;
	if (icount > 10)
		break;
	beg++;
}
//逐个删去容器内的值
while (!value)
{
	beg = value.begin();
	value.erase(beg);	//erase删除该位置上的值
}
```
##### vector容器常用操作与内存释放
> 太长了，在上操练了一遍

```c
#include <string>
#include <vector>

using namespace std;
struct conf {
	char itemname[40];
	char itemcontent[100];
};

char* getinfo (vector<conf*>& conflist, const char* pitem)
{
	for (vector<conf*>::iterator iter = conflist.begin(); iter != conflist.end(); iter++)
	{
		if (_stricmp(pitem, (*iter)->itemname) == 0)	//_stricmp 类似于 strcmp返回值是0时两者相等
			return (*iter)->itercontent;	//前面讲的都是iter->what/(*iter).what，我认为这里的(*iter)->itercontent是因为容器里装的是结构体指针
	}
	return nullptr;
}

int main
{
conf* pconf1 = new conf;
strcpy_s(pconf1->itemname, sizeof(pconf1->itemname), "Servername");
strcpy_s(pconf1->itemcontent, sizeof(pconf1->itemcontent), "1区");

conf* pconf2 = new conf;
strcpy_s(pconf2->itemname, sizeof(pconf2->itemname), "ServerID");
strcpy_s(pconf2->itemcontent, sizeof(pconf2->itemcontent), "127.0.0.0");
vector<conf*> conflist;
conflist.push_back(pconf1);
conflist.push_back(pconf2);

char* p_tmp = getinfo(conflist, "ServerID")
cout << p_tmp << endl;

std::vector<conf*>::iterator pos;
for (pos = conflist.begin(); pos != conflist.end(); pos++)
{
	delete(*pos)	//*pos才是存入的结构指针
}
conflist.clear();

return 0;
}
```

## 10 类型转换：`static_cast`、`reinterpret_cast`等

> 1 隐式类型转换
> 2 显式类型转换

#### 显式类型转换

`static_cast`、`dynamic_cast`、`const_cast`、`reinterpret_cast`四个强制类型转换都被称为“命名的强制类型转换”。



**通用形式**❤️

`强制类型转换名<type>(express)`

**强制类型转换名**：上面这四种；

**type**：转换的目标类型；

**express**：被转换的值。



#### `static_cast`静态转换

“正常转换”，编译的时候就会进行类型转换的检查。代码中要保证转换的安全性和正确性。



- **相关类型转换**：比如整型和实型之间的转换



```c
float f = 3.43f;
int i = static_cast<int>(f);
```

- **子类转成父类类型**(继承关系)(后面会讲到)

- **`void*`和其他类型指针之间的转换**



#### `dynamic_cast`：主要应用于运行时类型识别和检查

*主要用来父类型和子类型之间转换(父类型指针指向子类型对象，然后用dynamic_cast把父指针类型往子指针类型转)*

#### `const_cast`：去除指针或者引用的const性质

只能去除**指针**和**引用**



```c
const int i = 90;
const int* pi = &i;
int* qi = const_cast<int*>(pi);
```
#### `reinterpret_cast`：重新解释，处理无关类型的转换
# 二、类
**Author:** XFFer_
## 01 成员函数、对象拷贝、私有成员
> 1 综述
> 2 类基础
> 3 成员函数
> 4 对象的拷贝
> 5 私有成员

#### 成员函数

```cpp
//Time.h
class Time {
	int hour;
	int minute;
	int second;
	void InitTime (int tmphour, int tmpminute, int tmpsecond);
};
//Time.cpp
#include "Time.h"
void Time::InitTime (int tmphour, int tmpminute, int tmpsecond)
{
	hour = tmphour;
	minute = tmpminute;
	second = tmpsecond;	//类内部定义成员函数可以之间引用成员变量
}
```
#### 对象的拷贝

```cpp
Time time_one;
Time time_two = time_one;
Time time_three (time_two);
Time time_four { time_three };
```
*默认情况下，这种类对象的拷贝，是每个成员变量逐个拷贝。如果在类中定义适当的“赋值运算符”就能够控制对象的这种拷贝行为。*
## 02 构造函数详解，explicit，初始化列表
> 1 构造函数
> 2 多个构造函数
> 3 函数默认参数
> 4 隐式转换和explicit
> 5 构造函数初始化列表

#### 构造函数
在类中，有一种**特殊的成员函数**，它的**名字和类名相同**，我们在创建类的对象时，这个特殊的成员函数就**会被系统自动调用**。这个成员函数，就叫“**构造函数**”；因为构造函数会被系统自动调用，所以我们可以简单的理解成：构造函数的目的就是初始化类对象的数据成员。

```cpp
//Time.h
class Time {
public:
	int Hour;
	int Minute;
	int Second;
	Time (int tmphour, int tmpminute, int tmpsecond);
};
//Time.cpp
Time::Time (int tmphour, int tmpminute, int tmpsecond)
{
	Hour = tmphour;
	Minute = tmpminute;
	Second = tmpsecond;
}
```
- 构造函数没有返回值
- 不可以手工调用构造函数
- 正常情况下，构造函数应该被声明为public
- 构造函数中如果有多个参数，则我们创建对象的时候也要带上这些参数

```cpp
//定义一个类对象
Time mytime = Time(3, 29, 23);
Time mytime(3, 29, 23);
Time mytime{3, 29, 23);
Time mytime = Time{3, 29, 23};
```
#### 多个构造函数
**提供多种初始化方法**，但是参数表类型或者个数要有明显不同。
通过对象拷贝得到的新对象并没有调用传统意义上的构造函数而是调用了拷贝构造函数。
#### 函数默认参数
- 函数的默认值只能放在**函数声明**中，除非该函数没有函数声明
- 在具有多个参数的函数中指定默认值时，默认参数都必须出现在不默认参数的右边
- 一旦某个参数指定了默认值，它右边的所有参数都必须制定默认值

#### 隐式转换和explicit
在构造函数声明前添加`explicit`可以强制性要求构造函数不能做隐式类型转换，只能用于初始化和显式类型转换。
#### 构造函数初始化列表
> 定义构造函数时

```cpp
Time::Time (int tmphour, int tmpminute, int tmpsecond)
	:Hour(tmphour), Minute(tmpminute), Second(tmpsecond)
{
	...;
}
```
## 03 inline、const、mutable、this、static
> 1 在类定义中实现成员函数inline
> 2 成员函数末尾的const
> 3 mutable
> 4 返回自身对象的引用，this
> 5 static成员

#### 在类定义中实现成员函数inline
直接在.h头文件中类的定义中实现的成员函数，会被当作inline内联函数来处理。
#### 成员函数末尾的const“常量成员函数”
在成员函数后增加一个const。不但要在成员函数声明中增加const，在函数定义时也要增加const。
**作用**：这个成员函数不会修改该对象里任何成员变量的值。

```cpp
void classname::funcname (int valuelist) const;
```
**结论**：const成员函数，不管是const对象和非const对象都可以调用常量成员函数；而普通成员函数，不能用const对象调用。
#### mutable
> 不稳定，易改变的意思。为了图片const的限制

用`mutable`修饰一个成员变量，一个成员变量一旦被mutable修饰了，就表示这个成员变量永远处于可以被修改状态。即便是在const结尾的成员函数中，也可以修改。
#### 返回自身对象引用this
**快捷键** 
`ctrl + F3 + fn`	查找文件中重名项

```cpp
//Time.h
class Time {
	int Hour;
	Time& add_hour (int tmphour);
};
//Time.cpp
Time& Time::add_hour (int tmphour)	//返回值是对象本身
{
	Hour += tmphour;	//this->Hour += tmphour;
	return *this;	//this就是指向对象本身的指针，*this就是对象本身
}
//project.cpp
#include "Time.h"
int main()
{
	Time mytime;
	mytime.add_hour(3);
}
```
在调用成员函数时，编译器负责把这个对象的地址(&mytime)传递给成员函数中一个隐藏的this形参。在系统角度看来，任何对类成员的直接访问都被看做是通过this做隐式调用的。
1. this指针只能在成员函数中使用，全局函数、静态函数都不能使用this指针
2. 在普通成员函数中，this是一个指向非const类型的const指针`(Time* const this)`指向不能变，值可以改变
3. 在const成员函数中，this是一个指向const类型的const指针`(const Time* const this)`指向和值都不可以改变

#### static成员
**属于整个类的成员变量，这种成员变量叫static成员变量(静态成员变量)**，同样也有**静态成员函数**。静态成员函数只能操作静态成员变量。
特点：不属于某个对象，属于整个类，一旦在某个对象中修改了这个成员变量的值，在其他对象中也会随之改变。
调用时`类名::成员变量名``类名::成员函数名`

```cpp
//Time.h
class Time {
	static int date;	//还没有分配内存，不能初始化
};
//Time.cpp
int Time::date;	//分配内存，不给初值默认为0，定义时不需要加static
```
## 04 类内初始化、默认构造函数、 =default
> 1 类相关非成员函数
> 2 类内初始化
> 3 const成员变量的初始化
> 4 默认构造函数
> 5 =default; ,=delete;

#### const成员变量的初始化
常量属性变量，需要在构造函数定义时使用初始化成员列表给出常量值。
#### 默认构造函数
没有参数的构造函数称为默认构造函数。当没有构造函数时，进行“默认初始化”，编译器会生成一个“合成默认构造函数”。
使用多个构造函数时，一旦定义了一个构造函数系统就不会生成“默认构造函数”。
#### `=default;`，`=delete;`
> C++11引入

```cpp
class Time {
public:
	Time() = default;	//编译器能够自动生成函数体(只能用于特殊的函数)
	Time() = delete;	//禁用某个函数
};
```

## 05 拷贝构造函数
如果一个类的构造函数的第一个参数是**所属的类类型的引用**。如果还有其他额外参数，那么这些额外的参数还**都有默认值**，则这个构造函数叫做**拷贝构造函数**。
 
```cpp
class Time {
public:
	Time (const Time& tmptime, int tmpvalue = 0);
};
Time::Time(const Time& tmptime, int tmpvalue){

}
```
拷贝构造函数不要使用`explicit`。
## 06 重载运算符、拷贝赋值运算符、析构函数
> 1 重载运算符
> 2 拷贝赋值运算符
> 3 析构函数
>> 函数重载
>> 构造函数的成员初始化
>> 析构函数的成员销毁
>> new对象和delete对象

#### 重载运算符
**总结：**
**重载运算符**本质上是一个函数。整个函数的正式名字：`operator运算符`。重载运算符有**返回类型**和**参数列表**。
#### 拷贝赋值运算符

```cpp
class Time {
public:
	Time& operator=(const Time& tmpin);
};
Time& Time::operator=(const Time& tmpin) {
	return *this;	//返回调用拷贝赋值运算符的对象本身
}
//调用举例
Time mytime1;
Time mytime2;
mytime2 = mytime1;	//实际上是mytime2这个对象调用了拷贝赋值运算符，返回的仍是mytime2，形参是mytime1
```
#### 析构函数：相对于构造函数
> 对象在销毁时，会自动调用析构函数

由`~类名`构成，返回值，不接受任何参数，不能被重载，一个类只能用唯一一个析构函数。

```cpp
~Time();
Time::~Time()
{
	...
}
```
*成员变量的初始化和销毁时机问题：初始化时先定义的变量先初始化，销毁时先定义的后销毁。*
## 07 派生类、调用顺序、访问等级、函数遮蔽
> 1 派生类概念
> 2 派生类对象定义时调用构造函数的顺序
> 3 public，protected，private
> 4 函数遮蔽

#### 派生类概念
类之间存在着一种层次关系**“继承”**，继承的概念是面向对象程序设计的核心思想之一

- **父类**(基类，超类)
- **子类**(派生类)

```cpp
class Men : public Human		//Men是Human的子类
```
**继承方式**(访问等级/访问权限)：`public`/`protected`/`private`
###### 一个子类可以继承多个父类
#### 派生类对象定义时调用构造函数的顺序
首先会调用父类的构造函数，再调用子类的构造函数。
#### `public`/`private`/`protected`
**三种访问权限**：
`public`：可以被任意实体所访问
`protected`：只允许本类**或者子类**的**成员函数**来访问
`private`：只允许本类的成员函数访问
**三种继承访问**：`public`、`protected`、`private`

基类中的访问权限|子类继承基类的继承方式|子类得到的访问权限
------|------|------
public|public|public
protected|public|protected
private|public|子类无权访问
||
public|protected|protected
protected|protected|protected
private|protected|子类无权访问
||
public|private|private
protected|private|private
private|private|子类无权访问

**总结**：
1. 子类public继承父类不改变父类的访问权限
2. protected继承将父类中public成员变成子类的protected成员
3. private继承是的父类所有成员在子类中的访问权限变为private
4. 父类中的private成员不受继承方式的额影响，子类永远无权访问
5. **对于父类来讲，尤其是父类的成员函数，如果不想让外面访问，就设置为private；如果想让自己的子类能够访问，就设置为protected；如果想公开，就设置为public。**

#### 函数遮蔽
如果父类和子类中都出现同名函数，那么父类中无论有几个同名函数子类中都无法访问到。有两种方法：
1. 在子类的成员函数中，用“父类::函数名”强制调用父类函数
2. 通过`using`(C++11新定义)让父类同名函数在子类中可见，实际上就是通过“重载”的方式

## 08 基类指针、虚纯虚函数、多态性、虚析构
> 1 基类指针、派生类指针
> 2 虚函数
>> override
>> final
>
> 3 多态性
> 4 纯虚函数
> 5 基类的析构函数一般写成虚函数(虚析构函数)

#### 基类指针、派生类指针

```cpp
Human *phuman = new Men;
```
**新玩法**：用父类指针`new`一个子类对象，但是这个父类指针不能调用子类成员函数
#### 虚函数
**Q:**有没有一个解决方案，使我们只定义一个对象指针，就能够调用父类、子类的同名函数？
**A:**。但是**它的类型必须是父类类型**，而且**该同名函数在父类声明之前要加`virtual`声明该函数为虚函数。**
***一旦一个函数在基类中被声明成了虚函数，那么在所有的派生类中这个函数都是虚函数。***

```cpp
Human *phuman = new Human;	//new基类，调用基类内的同名函数
phuman = new Men;	//子类，调用子类内的同名函数
phuman = new Wemen;
```
##### `override`
这个关键字用在“子类”中，虚函数专用，用来说明派生类中的虚函数覆盖了父类中的同名函数，加在函数声明末尾。

```cpp
class Men : public Human {
public:
	virtual void eat() override;
};
```
##### `final`
虚函数专用，用在父类中函数声明中后加`final`，那么就禁止一切覆盖该函数的操作。
**调用虚函数执行的是“动态绑定”**。动态：表示的是在程序运行时才能得知调用了哪个子类的虚函数。
#### 多态性
多态性是针对虚函数来说的，体现在具有继承关系的父类和子类之间，子类重新定义父类的成员函数，通过父类的指针，只有到了程序运行时期，找到动态绑定到父类上的对象，系统内部通过查虚函数表，找到入口地址，从而调用父类或者子类的成员函数，这就是运行时期的多态性。
#### 纯虚函数
**纯虚函数**是在**基类**中声明的虚函数，但是它在基类中没有定义，但是要求任何派生类都要定义该虚函数自己的实现方法。

**基类中实现纯虚函数的方法是** 在函数原型后加`= 0`。

一旦一个类有纯虚函数，那么就不能生成这个类的对象了，它的主要目的是**统一管理子类对象**。

#### 基类的析构函数一般写成虚函数(虚析构)
**Q**:用基类指针new子类的对象，在delete系统不会调用派生类的析构函数，导致内存泄漏。
**A**:在父类的析构函数前`virtual`写成虚析构

**结论**：如果类作为基类，就一定要写析构函数`~类名`，析构函数一定要是虚析构函数`virtual`。
## 09 友元函数、友元类、友元成员函数
> 1 友元函数
> 2 友元类
> 3 友元成员函数


#### 友元函数
在类中定义为`private`不能公开访问，如果让函数function成为类的友元函数，那么就能访问类的所有成员(成员变量/成员函数)(`private`/`public`/`protected`)。

```cpp
class Name {
friend void function(const Name& tmpin);	//该函数是友元函数
};
```
友元函数不属于类成员，不受public、private、protected管控。
#### 友元类

```cpp
class B {
public:
	void callA(int x, A& tmpin) {
		tmpin.a = x;
	}
};
class A {
private:
	int a;
	
	friend class B;	//B是A的友元类，B可以调用A中的所有成员
};
```
**每个类负责控制自己的友元类和友元函数**

1. 友元关系不能被继承
2. 友元关系是单向的
3. 友元关系是没有传递性的

#### 友元成员函数
只有`public`的函数才能成为其他类的友元成员函数
## 10 RTTI、dynamic_cast、typeid、虚函数表 
> 1 RTTI是什么
> 2 `dynamic_cast`运算符
> 3 typeid运算符
> 4 type_info类
> 5 RTTI与虚函数表

#### RTTI是什么
**RTTI**(Run Time Identification)：**运行时类型识别**
通过运行时类型识别，程序能够使用基类的指针或者引用来检查这些指针或者引用所指的对象的实际派生类型。

RTTI我们把这个称呼看成是一种系统提供的一种能力，或者一种功能。这种功能或者能力通过两个运算符来体现：
1. **`dynamic_cast`运算符**：能够将基类的指针或者引用安全的转换为派生类的指针或者引用
2. **`typeid`运算符**：返回指针或者引用所指对象的实际类型

**补充**：要让RTTI的两个运算符能够正常工作，基类中必须要有一个虚函数
**作用**：前面讲到，基类和派生类的同名函数可以通过虚函数和父类指针new子类对象来实现，但是子类中专有函数却不能通过该指针调用，RTTI就用来解决这个问题

#### `dynamic_cast`运算符

```cpp
Human* phuman = new Man;
Man* pman = dynamic_cast<Man*>(phuman);
```
**基类必须有一个虚函数**。

对于**引用**，如果用`dynamic_cast`转换失败，会返回一个`std::bad_cast`异常。C++中我们使用`try{}...catch(){}:`捕捉异常。

```cpp
Human* phuman = new Men;
Human& q = *phuman;
try
{
	Men& men_in = dynamic_cast<Men&>(q); 
	men_in.test();
}
catch(std::bad_cast)
{
	cout << "phuman实际不是一个Men类型" << endl;
}
```
#### `typeid`运算符
**typeid(类型)，也可能typeid(表达式)**
拿到对象类型信息；typeid就会返回一个常量对象的引用，这个常量对象是一个标准库类型type_info(类)。

```cpp
Human* phuman = new Men;
Human& q = *phuman;
cout << typeid(*phuman).name() << endl;	//typeid返回值是一个类，.name()是一个成员
cout << typeid(q).name() << endl;
```
#### type_info类
- `typeid().name()`返回名字
	- **`typeid`返回的是type_info这个类，可以用`const type_info &tp`接**

#### RTTI与虚函数表
C++中，如果类里含有虚函数。编译器就会对该类产生一个虚函数表。虚函数表里每一项都是一个指针。每个指针指向这个类里的各个虚函数的入口地址。虚函数表项里，第一个表项很特殊，它指向的是这个类所的type_info对象。
## 11 基类与派生类关系的详细再探讨
> 1 派生类对象模型简述 
> 2 派生类构造函数
> 3 既当父类又当子类
> 4 不想当基类的类
> 5 静态类型与动态类型
> 6 派生类向基类的隐式类型转换
> 7 父类子类之间的拷贝与赋值


#### 派生类对象模型简述
派生类对包含*含有派生类自己定义的成员变量、成员函数的子对象*和*所继承的基类的子对象*。
#### 派生类构造函数
派生类用基类的构造函数初始化基类部分，派生类的构造函数初始化派生类部分。
**Q**:假如基类构造函数需要传入参数，派生类该如何定义？
**A**:通过派生类的**构造函数初始化列表**。

```cpp
class A {
public:
	A(int i) : m_value_a(i) {}
	int m_value_a;
};
class B : public A {
public:
	B(int i, int j) : m_value_b(j), A(i) {}
	int m_value_b;
};
```
#### 既当父类又当子类
继承关系有传递性，构成一种继承链。
#### 不想当基类的类
`final`加在类名后，就不能做基类了。
`final`在前面讲到是不能被子类中的同名函数遮蔽。
#### 静态类型与动态类型
**静态类型**：变量声明时的类型。静态类型编译的时候是已知的。
**动态类型**：指的是这个指针或引用所代表的内存中的对象的类型，在运行时才能得知。
只有在基类指针或引用时才存在静态类型和动态类型不一致的情况。

**用派生类对象给一个基类对象赋值或初始化时，只会对派生类对象的基类部分操作。**
**复习**：

```cpp
class Human {
public:
	//重载拷贝运算符
	Human& operator=(const Human& tmphuman)
	{
		return *this;
	}
	//拷贝构造函数
	Human (Human& tmpin) {}
};
```
## 12 左值、右值、左值引用、右值引用、move
> 1 左值和右值
> 2 引用分类
> 3 左值引用
> 4 右值引用
>> 右值引用的引入目的
>
> 5 std::move函数
> 6 左值右值总结说明

#### 左值和右值
**左值**(左值表达式)：能用在赋值语句等号左侧的东西，能够代表一个地址。
**右值**(右值表达式)：非左值的值。
一个左值可能同时具有左值属性和右值属性。
#### 引用分类
三种形式的引用：
1. 左值引用(绑定到左值)`&`
2. const引用(常量引用)(也是左值引用，但是不能改变值的对象)
3. 右值引用(绑定到右值)`&&`

#### 左值引用
除const引用可以绑定到右值外，其他左值引用均不可以绑定到右值。
#### 右值引用

```cpp
int&& refrightvalue = 3;
```
**总结**：

- 返回左值引用的函数，连同赋值，下标，前置递增递减运算符(++i)，都是返回左值表达式的例子
- 返回非引用类型的函数，连同算数，关系，位以及后置递增运算符(i++)都生成右值

`++i`**是左值表达式的原因：**++i直接给变量i+1，然后返回i本身，这里i是变量。
`i++`**是右值表达式的原因：**i++先产生一个临时变量，记录下临时变量的值用作使用，在递增接着返回这个临时变量，临时变量是右值。
##### 右值引用的引入目的
- 提高系统运行效率。把拷贝对象变成移动对象来提高效率
- 移动对象。`&&`作为移动构造函数和移动赋值运算符的参数，`&`作为拷贝赋值运算符和拷贝赋值构造函数的参数

#### std::move函数
**把左值强制转换成右值**

```cpp
int i = 10;
int&& ri = std::move(i)
```

## 13 临时对象深入探讨、解析，提高性能手段
> 1 临时对象的概念
> 2 产生临时对象的情况和解决
>> 以传值的方式给函数传递参数
>> 类型转换生成的临时对象/隐式类型转换以保证函数调用成功
>> 函数返回对象的时候
#### 临时对象的概念
一些临时变量是因为代码书写问题产生的统一称临时变量为**临时对象**。
#### 产生临时对象的情况和解决
##### 以传值的方式给函数传递参数
*应当避免直接将对象实体传入函数，如果传入的是类对象，会多调用拷贝构造函数和析构函数，消耗系统资源。*
##### 类型转换生成的临时对象/隐式类型转换以保证函数调用成功
C++语言只会给const引用产生临时变量。

```cpp
class Cls {
public:
	int value1;
	int value2;
	
	Cls (int tmpin1 = 0, int tmpin2 = 0) : value1(tmpin1), value2(tmpin2);
};
Cls operator+ (Cls& cls_in1, Cls& cls_in2)
{
	return Cls(cls_in1.value1 + cls_in2.value1, cls_in1.value2 + cls_in2.value2);
}
```
*直接return避免构建局部对象，节省了构造函数和析构函数的使用提升效率。*

## 14 对象移动、移动构造函数、移动赋值运算符
> 1 对移动的概念
> 2 移动构造函数和移动赋值运算符概念
> 3 移动构造函数演示
> 4 移动赋值运算符演示
> 5 合成的移动操作
> 6 总结

#### 对移动的概念
> C++11定义的新概念，将临时对象有用的部分保留下来，无用的部分清除掉

#### 移动构造函数和移动赋值运算符概念
###### 首先回顾一下，拷贝赋值运算符在定义时返回值类型和参数表都是根据具体情况而变的，唯一不变的是函数名必须是`operator符号`
**移动构造函数**：`类名::类名(const 类名&& tmp)`
***右值引用的引入用作移动构造函数的参数***，移动构造函数除**右值引用**外其他函数参数都必须**带有初值**(拷贝构造函数也是这样)

##### 移动构造函数和移动赋值运算符应该完成的功能
- 完成必要的内存移动，斩断原对象和内存的关系
- 确保移动后原对象处于一种可以销毁对程序没有影响的状态

#### 移动构造函数演示

```cpp
class B {
public:
	int b_value;
	B() : b_value(100){
	cout << "调用了class B的构造函数" << endl;
	}
	B(const B& tmpb) : b_value(tmpb.b_value){
	cout << "调用了class B的拷贝构造函数" << endl;
	}
	virtual ~B(){
	cout << "调用class B的析构函数" << endl;
	}
};
class A {
private:
	B* pb;
public:
	A() : pb(new B()){	//用new B()对象递给pb这个指针，调用了B的构造函数
	cout << "调用了class A的构造函数" << endl;
}

	A(const A& tmpa) : pb(new B(*(tmpa.pb))){
	cout << "调用了class A的拷贝构造函数" << endl;	//其实还调用了B的拷贝构造函数，用已存在的tmpa(A类对象)的pb指针，传递给B的拷贝构造函数得到新的类B赋给新指针pb
	}
	
	//移动构造函数
	//直接把传入对象的指针(地址)给了临时对象
	A(A&& tmpa) noexcept : pb(tmpa.pb){	//参数不能是const类，因为需要改动
	tmpa.pb = nullptr;	//打断传入对象的指针和指向对象的联系
	cout << "调用了class A的移动构造函数" << endl;
	}
	
	virtual ~A(){
	delete pb;
	cout << "调用了class A的析构函数" << endl;
	}
};
```
`noexcept`是C++11标准，目的是通知标准库这个移动构造函数不抛出任何异常(提高编译器工作效率)。
#### 移动赋值运算符

```cpp
//拷贝赋值运算符
	A& operator=(const A& src){
		if (pb == &src)
			return *this;
		delete pb;
		pb = new B(*(src.pb));
		return *this; 
	}
//移动赋值运算符
	A& operator=(A&& src) noexcept{
		if (this == &src)
			return *this;
		delete pb;	//先把自己的pb内存干掉
		pb = src.pb;	//把传入对象的成员内存拿走
		src.pb = nullptr;	//斩断源(把对方和内存的关联斩断)
		return *this;
	}
```

#### 合成的移动操作
- 如果类有拷贝构造函数/拷贝赋值运算符/析构函数，那么编译器就不会合成移动构造函数和移动赋值运算符
- 如果没有移动构造函数/移动赋值运算符，系统会调用拷贝构造函数/拷贝赋值运算符
- 只有一个类没定义任何拷贝构造成员，且类的每个非静态成员都可以移动时，系统会自动合成移动操作

## 15 继承的构造函数、多重继承、虚继承
> 1 继承的构造函数
> 2 多重继承
>> 多重继承概述
>> 静态成员变量
>> 派生类构造函数与析构函数
>> 从多个父类继承构造函数
>
> 3 类型转换
> 4 虚基类、虚继承(虚派生)
> 5 总结

#### 继承的构造函数
*一个类只继承其直接基类(父类)的构造函数。*

```cpp
using A::A;
```
继承A的构造函数。`using`会让某个名字在当前作用域内可见。
会把基类中每个构造函数，都生成一个与之对应的派生类构造函数(除拷贝构造函数/移动构造函数)。
当**基类A的构造函数有默认参数**时，编译器会**构造出多个派生的构造函数**。***第一个构造函数是带有所有参数的构造函数，其余的构造函数，每个分别省略掉一个默认参数。***
#### 多重继承
> 一个类同时继承多个类

```cpp
class C : public A, public B
```
**子类(派生类)必须在构造函数中给父类构造函数初始化**
##### 静态成员变量

```cpp
class A {
public:
	static int a;	//声明一个静态成员
};
int A::a = 1;	//定义静态成员变量(分配内存)
```
##### 派生类构造函数与析构函数
- 构造一个派生类对象将构造并初始化所有基类子对象
- 派生类的构造函数初始化列表只初始化它的直接基类
- 派生类的构造函数初始化列表将实参分别传递给每个直接基类；基类的构造顺序和**派生列表**中基类的出现顺序保持一致

#### 虚基类、虚继承(虚派生)
派生列表中，同一个基类只能出现一次，除两种情况外：

- 派生类可以通过两个直接基类分别继承同一个间接基类
- 直接继承某个基类，然后通过另一个基类间接继承该类

**虚基类**：无论继承体系中出现多少次基类，都只会出现唯一一个共享的虚基类子内容。

```cpp
class A : virtual public B {
};
```
如果通过间接继承同一个基类，使用**虚基类**，需要用这个**间接的子类初始化重复继承的那个基类**，换句话说**虚基类需要由最底层派生类初始化**。

## 插入课：C++文件和流
标准库**fstream**(file stream文件流)

数据类型 | 描述
------ | ------
ofstream|该数据类型标书输出文件流，用于创建文件并向文件写入信息
ifstream|该数据类型表示输入文件流，用于从文件读取信息
fstream|该数据类型表示文件流，同时具有ofstream和ifstream两种功能

> 在C++中进行文件处理必须包含头文件<iostream>和<fstream>

#### 打开文件
open()函数是fstream、ifstream、ofstream对象的一个成员，它的**标准语法**是

```cpp
void open(const char* filename, ios::openmode mode);
//void std::fstream::open(const char *_Filename, unsigned int _Mode)
```
**第一个参数是文件的名称和位置，第二个参数定义文件被打开的模式。**

模式标志|描述
------|------
ios::app|追加模式。所有写入都追加到文件末尾
ios::ate|文件打开后定位到文件末尾
ios::in|打开文件用于读取
ios::out|打开文件用于写入
ios::trunc|如果该文件已经存在，其内容将在打开文件之前被截断，即把长度设为0

```cpp
ofstream outfile;
outfile.open("file.dat", ios::out | ios::trunc);
```
#### 关闭文件
close()函数也是fstream、ifstream、ofstream对象的成员
##### 写入文件
在C++编程中我们使用**流插入运算符(<<)**向文件写入信息，这里使用的是**ofstream**或**fstream**对象
##### 读取文件
在C++编程中我们使用**流提取运算符(>>)**从文件读取信息，这里使用的是**ifstream**或**fstream**对象

##### istream& getline(istream &is, string &str, char delim);
可读取整行，包括前导和嵌入的空格，并将其存储在字符串对象中。

槃 2020/2/12 20:55:26
- `istream &is`表示一个输入流，如cin
- `string &str`表示把从输入流读入的字符串存放在这个字符串中
- `char delim`表示遇到这个字符停止读入，默认是'\n'

##### cin.getline(字符指针(char *), 字符个数(int N), 结束符(char));
一次读取多个字符(包括空格)一指定的地址为存放第一个读取字符的位置，依次向后存放，知道读满N-1个。
##### cin.ignore(a, ch)
从输入流cin提取字符，提取的字符被忽略，不被使用。计数值达到a或提取到字符ch，函数终止。

```cpp
#include <iosstream>
#include <string>
using namespace std;

int main()
{
	string name;
	string city;
	cout << "Please enter your name: ";
	getline(cin, name);	//cin是正在读取的输入流，第二个参数是string变量的名称
	cout << "Enter the city you live in: ";
	getline(cin, city);
	cout << "Hello," << name << endl;
	cout << "You live in" << city << endl;
	return 0;
}
```

```cpp
#include <iostream>
#include <fstream>

int main(int argc, char** argv)
{
	char data[100];
	ofstream outfile;
	outfile.open("afile.dat");
	
	cout << "Writing to the file" << endl;
	cout << "Enter your name: "l
	cin.getline(data, 100);
	
	//向文件写入用户输入的数据
	outfile << data << endl;
	cout << "Enter your age: ";
	cin >> data;
	
	//ignore()函数会忽略掉之前读语句留下的多余字符
	cin.ignore();
	outfile << data << endl;
	
	outfile.close();
	
	//以读模式打开文件
	ifstream infile;
	infile.open("afile.dat");
	//从文件读取数据，并显示它
	infile >> data;
	cout << data << endl;
	
	inflie.close();
	return 0;
}
```
## 16 类型转换构造函数、运算符，类成员指针
> 1 类型转换构造函数
> 2 类型转换运算符(类型转换函数)
>> 显式的类型转换运算符
>> 有趣范例：类对象转换为函数指针
>
> 3 类型转换的二义性问题
> 4 类成员函数指针
>> 对于普通成员函数
>> 对于虚函数
>> 对于静态成员函数
>
> 5 类成员变量指针
>> 对于普通成员变量
>> 对于静态成员变量

#### 类型转换构造函数
**特点**：

- ***能够把其他类型转换成类类型***
- 只有**一个参数**，该参数其实是待转换的数据类型
- 在函数中，要指定转换的方法

#### 类型转换运算符：和类型转换构造函数能力相反
**格式**：`operator type() const;`
**特点**：

- ***能够把类类型转换成其他类型***，const是可选项，代表不能改变待转换对象内容
- type是想要转换成的某种类型
- 类型转换运算符没有形参(形参列表为)，因为类型转换运算符都是隐式执行的，同时，也不能指定返回类型
- 必须定义为类的成员函数

```cpp
class A {
public:
	explicit operator int() const	//explicit禁止了隐式的类型转换
	{
		return value;
	}
	int value;
};
A a;
a.value = 9;
int k = static_cast<int>(a) + 10;	//显式类型转换
int k = a.operator int() + 10;	//显式调用
```
##### 类对象转化成函数指针

```cpp
//定义一个函数指针类型
typedef void (*p) (int);
using p = void (*) (int);
```
#### 类成员函数指针
##### 对于普通成员函数/虚成员函数
**格式**：
`类名::*函数指针变量名`**来声明成员函数指针**
`&类名::成员函数名` **来获取成员函数的地址**

```cpp
class Name {
public:
	void func1(int getvalue) {}
};
int main()
{
	void (Name::*pointname) (int);
	pointname = &Name::func1;	//成员函数，有类就有成员函数，而不是需要定义类对象才分配地址

	Name person, *p;
	(person.*pointname) (int i);
	(p->*pointname) (int i);
}
```
##### 对于静态类成员函数
**静态类成员函数指针定义时`*函数指针变量名`**
#### 类成员变量指针
##### 对于普通成员变量
> 并不是真正意义上的地址，指针指向的不是内存中某个地址，而是该成员变量与该类对象指针(对象首地址)之间的偏移量

```cpp
class A {
	int a;
};
int main() {
	int A::*point = &A::a;
}
```
###### 如果一个类中有虚函数，则对象中就会有一个指向虚函数表的指针，占4个字节。
***而静态成员变量则属于类有自己的地址。定义时和普通指针相同无需加`类名::`***
# 三、模版与泛型
**Author:** XFFer_
## 01 模版概念，函数模版定义、调用
> 1 概述
> 2 函数模版的定义
> 3 函数模版的使用
> 4 非类型模版参数

#### 概述
> vector实际上就是一个模版，vector<int>才是一个类

- 所谓泛型编程是以独立于任何类型的方式编写代码。使用泛型编程时，我们需要提供具体程序实例所操作的类习惯或者值
- 模版是泛型编程的基础，模版是创建类或者函数的蓝图或者公式。我们给这些蓝图或者公式提供足够的信息，让这些蓝图或者公式真正的转变成具体的类或者函数，发生在编译时
- 模版支持将类型作为参数的程序设计方式，从而实现了对泛型程序设计的直接支持

#### 函数模版的定义
**overloaded function**(重载函数)实际上就是两个同名函数，但是形参列表有明显不同。

```cpp
template<typename T>
T funcadd(T a, T b)
{
	T add_result = a + b;
	return add_result;
}
```

- **模版定义是用`template`关键开头的，后边跟`<>`，里面叫模版参数列表(模版实参)**
- `<>`里必须有一个模版参数，模版参数前`typename/class`，模版参数列表里表示函数定义中用到的“类型”**或**“值”
- 多个模版参数时，需要用多个`template <typename A, typename B>`

#### 函数模版的使用
> 和正常调用函数相似，系统会**实例化**出推断出的形参类型对应的函数

模版函数可以是内联`inline`(加在template的下一行)的，模版定义不会生成代码，只会在调用函数模版时，才会实例化出一个特定版本的函数。
#### 非类型模版参数
用**传统的类型名**来指定非类型参数，当模版被实例化时，这些非类型模版参数的值必须是**常量表达式**，在编译时实例化。

```cpp
template<int a, int b>
int func()
{
	int result = a + b;
	return result;
}
int answer = func<12, 13>();	//显式的指定模版参数--在尖括号中提供额外的信息
```
## 02 类模版概念、类模版定义、使用
> 1 概述
> 2 类模版定义
> 3 类模版的成员函数
> 4 模版类名字的使用
> 5 非类型模版参数


##### 概述
> 用类模版实例化一个特定的类，需要在模版名后用`<>`提供额外的信息。实例化类模版需要包含全部信息，包括类成员函数的定义

#### 类模版定义

```cpp
template <typename 形参名1, typename 形参名2, ..., typename 形参名n>
class 类名
{
	...
};
```

```cpp
template<typename T>
class myvector
{
public:
	typedef T* myiterator;
public:
	myiterator mybegin();	//返回值是myiterator，其实就是指向容器内部对象的指针
	myiterator myend();
	void func();
	
	myvector& operator=(const myvector&);
};
```
#### 类模版的成员函数

- 类模版的成员函数可以写在类定义中，这种成员函数会被隐式声明为inline函数
- **类模版一旦被实例化之后，每个实例都会有自己版本的成员函数**
- 类模版的成员函数具有和这个类模版相同的模版参数
- 定义在**类模版之外的成员函数**必须以`template<模版参数表>`开始，类名后要用`<>`把模版参数列表里的参数名列出

```cpp
template<typename T>
void myvector<T>::func
{
	...
}

template<typename T>
myvector<T>& myvector<T>::operator=(const myvector&)
{
	return *this;
}
```
###### 浮点型/类类型 不能做类模版的非类型模版参数
## 03 用typename场合、默认模版参数、趣味写法分析
> 1 typename的使用场合
> 2 函数指针做其他函数的参数
> 3 函数模版趣味用法举例
> 4 默认模版参数

#### typename的使用场合
##### 类型成员

```cpp
typedef T* iterator;

vector<int>::iterator iter;
```
这个`typedef`出的就是**类型成员。**

```cpp
#include <vector>

vector<int> contain;
for (vector<int>::iterator iter = contain.begin(); iter != contain.end(); iter++) {}
```
这里的contain是一个**类对象**；iterator是实例化vector得到的类中的**类型成员**；iter是一个**指向int对象的指针**，因为`typedef *T iterator`，contain是一个**储存整形数据的类对象**，可以调用类成员函数`begin()`、`end()`，返回值也是指向整形变量的指针。

```cpp
template<typename T>
typename myvector<T>::myiterator myvector<T>::begin() {}
```
模版实例出的类后跟作用域标识符`::`默认被系统处理成成员，而myiterator在这里作为类型成员(返回值类型)，必须使用**typename**声明。
#### 函数模版趣味用法举例

```cpp
template<typename T, typename F>
void func(const T& i, const t& j, F funcpoint)
{
	funcpoint(i, j);
}
int mcfunc(int i, int j)
{
	return i+j;
}
func(2, 4, mcfunc);	//T->int，F->int (*) (int, int)的函数指针
```


## 04 成员函数模版，显式实例化、声明
> 1 普通类的成员函数模版
> 2 类模版的成员函数模版
> 3 模版显式实例化，模版声明

#### 普通类的成员函数模版
成员函数都可以是函数模版，成为“**成员函数模版**”，虚函数。
#### 类模版的成员函数模版

```cpp
template <typename T>
class A {
public:
	template <typename P>
	void func(P& p);
};

template <typename T>
template <typename P>
void A<T>::func(P& p) {}
```
类模版的成员函数(普通成员函数/模版成员函数)只有为程序所用才会实例化。
#### 模版显式实例化、模版声明
**Q**：为了防止在多个.cpp文件中都实例化相同的类模版
**A**：C++11提出“**显式实例化**”

```c
//“显式实例化”手段中的“实例化定义”
template A<float>;
//“显式实例化”手段中的“实例化声明”
extern template A<float>;	//不会再在本文件中生成这个实例化版本
//目的是告诉编译器，在其他文件中已经有了该模版的实例化版本
```
## 05 using定义模版别名，显式指定模版参数
> 1 using定义模版别名
> 2 显式指定模版参数

#### using定义模版别名(类型模版)

```cpp
typedef std::map<std::string, int> map_s_i;
```
但是`typedef`定义出的是固定的格式。
**C++98中：**

```cpp
template <typedef M>
struct map_s
{
	typedef map<string, M> map_c;
};
//很类似iterator定义了一个类型成员
map_s<int>::map_c mapl;
```
**C++11中：**

```cpp
template <typename T>
using str_map = map<string, T>;
```
## 06 模版全特化、偏特化(局部特化)
> 1 类模版特化
>> 类模版全特化
>> 类模版偏特化
>
> 2 函数模版特化
>> 函数模版全特化
>> 函数模版偏特化

### 类模版特化
#### 类模版全特化
**特化**：对特殊的类型(类型模版参数)进行特殊的处理。

```cpp
template <typename T, typename F>
struct test {
	void functest() {
	cout << "调用了泛型版本" << endl; }
};
//特化类模版
template <>
struct test<int, double> {
	void functest() {
	cout << "调用了特化版本" << endl; }
};
//特化成员函数
template <>
void test<double, float>::functest() {
	cout << "调用了特化版本的成员函数" << endl;
}
```
#### 类模版偏特化

```cpp
//参数数量进行偏特化
template <typename T, typename F, typename L>
struct test {
	... };
template <typename F>
struct test<double, F, int> {
	... };
//模版参数范围上的特化版本
template <typename T>
struct test {
	... };
template <typename T>
struct test<const T> {
	...};	//const特化版本
```
#### 函数模版全特化

```cpp
template <typename T, typename P>
void func(T& tmprv, P& tmprc)
{
	... }
template <>
void func(double& tmprv, int& tmprc)
{
	... }
```
**函数模版没有偏特化!**
**必须都有泛型模版，才可以定义特化模版。模版定义、实现都放在一个`.h`文件中。**

## 07 可变参模版
> 1 可变参函数模版
>> 简单范例
>> 参数包的展开
>
> 2 可变参类模版
>> 通过递归继承方式展开参数包

### 可变参函数模版
`...`**的位置很关键!**

```cpp
template <typename... T>
void myfunc(T... argc)
{
	cout << sizeof...(T) << endl;	//返回T...的类型数
	cout << sizeof...(argc) << endl;
}
```
T中存放的是**任意个不同类型**，称作**可变参类型**； argc中存放着**任意个形参**，称作**可变形参**。


#### 参数包的展开
一个参数`typename T`和一包参数`typename... F`，这种可变参函数模版更容易展开！

```cpp
//参数包用迭代方式展开
void func() {}	//终止迭代

template <typename T, typename... F>
void func(const T& src, const F&... stv)
{
	cout << src << endl;
	func(stv...);
}
```
### 可变参类模版
#### 通过递归继承的方式展开参数包

```cpp
template <typename... Args> class myclass { };	//为了保证可变参模版定义成功

template<> class myclass<> {	//特化空模版
public:
	myclass() {
		cout << "myclass<>::myclass()执行" << endl; 
	}
};

template <typename First, typename... Others>
class myclass<First, Others...> : private myclass<Others...>	//偏特化
{
public:
	myclass() : m_i(0)
	{
		cout << "myclass::myclass执行了" << ' ' << "this: " << this << endl;
	}
	First m_i;
};

int main 
{
	myclass<int, float, double> cls();
}
```
(**Debug结果：感觉挺难的**)

- 首先声明**构造函数的执行是从父类->子类的**
-  **实例化一个类对象，类`cls()`括号内的参数是根据构造函数中的参数确定的**
- (每次取**可变参**)类对象`<int, float, double>`继承于`<float, double>`；`<float, double>`继承于`<double>`；`<double>`继承于`< >`。**模版参数同样也是特化版本**
- 就这样`< >`是基类对象，控制台输出*"myclass<>::myclass()执行"*；紧接着`<double>`->`<float, double>`->`<int, float, double>`都会输出*"myclass:myclass执行了"*

## 08 可变参模版续、模版模版参数
> 1 可变参类模版
>> 通过递归组合方式展开参数包
>> 通过tuple和递归调用展开参数包
>> 总结
>
> 2 模版模版参数

### 可变参类模版
#### 通过递归组合方式展开参数包
**组合关系(复合关系)**：*类A中包含B对象(即在类A定义内部定义一个类B的对象)。*

```cpp
template <typename... Args> class myclass {};	//保证递归组合方式能够成功复合

template <>
class myclass<>
{
public:
	myclass() {
		cout << "myclass<>::myclass()执行" << endl;	}
};

template <typename First, typename... Others>
class myclass<First, Others...>
{
public:
	myclass(First prao, Others... pano) : m_i(0), m_t(pano)
	First m_i;
	
	myclass<Others...> m_t;
};
```
#### 通过tuple和递归调用展开参数包
**实现思路**：计数器从0开始，每处理一个参数，计数器+1，一直到把所有参数处理完；最后搞一个模版偏特化，作为递归调用结束。

```cpp
#include <tuple>
//mycount用于统计，从0开始，mymaxcount表示参数数量
template <int mycount, int maxmycount, typename... T>
class myclass {
public:
	static void mysfunc(const tuple<T...>& t)
	{
		cout << "value= " << get<mycount>(t) << endl;
		//get是tuple元组的用法get<整数(表示位置从0开始)>(tuple对象)
		myclass<mycount + 1, maxmycount, T...>::mysfunc(t);
		//递归调用，计数器+1，取下一个tuple位置中的值
	}
};

//特化一个结束版本
template<int maxmycount, typename... T>
class myclass<maxmycount, maxmycount, T...> {
public:
	static void mysfunc(const tuple<T...>& t)
	{
	}
};

template <typename... T>
void myfunc(const tuple<T...>& t)
{
	myclass<0, sizeof...(T), T...>::mysfunc(t);	
}

int main()
{
	tuple<float, int ,double> mytuple(3.2f, 3, 5);
	myfunc(mytuple);
}
```
(**也挺难的**能看懂就好)

- **get< >( )**是元组的一个**方法**，目的是取各索引下的值，0 ~ len - 1，< >中存索引，( )中存tuple对象名
- 这个例子中的**可变模版参数T...**，实际作用是用来代表**tuple元组中保存的多种类型**
- **myclass是一个计数器**，mycount是get的索引位，maxmycount是get方法的终止位，在函数myfunc中给mycount初始化为0，maxmycount初始化为传入元组内的元素个数`sizeof...(T)`
- **计数器内每get到tuple的一个元素，就迭代调用mycount索引值+1的计数器版本，maxmycount不变**
- 直到mycount==maxmycount时，也就是特化的版本，终止执行，**因为索引值执行到len - 1之后就没有内容了**

### 模版模版参数
**用于在模版中还要使用类模版的情况下！**
这是一个模版参数，前面都叫**类型模版参数**，这个**模版参数本身，又是一个模版。**
**第种写法**(第二种直接放里面了)

```cpp
template <
			typename T,	//类型模版参数
			template<class> class Container	//模版 模版参数
			//template<typename W> typename Container
			>
class myclass
{
public:
	T t_i;
	Container<T> myc;
	
	myclass()
	{
		for (i = 0; i <10; i++)
		{
			myc.push_back(i);
		}
	}
};

template<typename T>
using myvec = vector<T, allocator<T>>;	//需要确定一个分配器，系统没能自己确定

myclass<int, myvec> mvectobj;	
//这里是因为vector有第二个参数allocator分配器，所以需要自己用using手动定义一个
```
(**理解**)

- 模板模板参数`template<class/typename> class/typename 名字`
	- **这里的class不代表类定义**，而是和typename可互换
	- 下面使用`Container<T>`时，第一个typename系统确定为T，第二个确定为class(类)
- `using myvec = vector<T, allocator<T>>`是固定写法

# 四、智能指针
**Author:** XFFer_
## 01 直接内存管理(new/delete)、创建新工程观察内存泄漏
> 1 直接内存管理(new/delete)
> 2 创建新工程，观察内存泄漏

#### 直接内存管理(new/delete)
> C语言中是`malloc/free`

##### 定义初值

```cpp
int *pointi = new int(100);
string *points = new string(5, 'a');	//"aaaaa"
vector<int> *pointv = new vector<int>{1, 2, 3, 4, 5};  
```
**概念 “值初始化”**：用`()`来初始化

```cpp
int *pointi = new int();
auto pointi_t = new auto(pointi);
//前面的auto推断出的是int **
```
推荐在`delete`后将该指针设置成`nullptr`
C++中出现了**智能指针**，会帮助程序猿收回内存。
#### 创建新工程，观察内存泄漏
**MFC应用程序**能够在一定程度上(程序推出的时候)，帮助发现内存泄漏。
**MFC**：微软公司出的基础的程序框架(MFC基础类库)，可以生成一个带窗口(带界面)的程序框架，MFC简化了很多界面开发工作。

**快捷键** `ctrl + ]` 跳转到对应的`{` 或 `}`

## 02 new、delete探秘，智能指针概述、shared_ptr基础
> 1 new/delete探秘
>> new/delete是什么
>> operator new()和operator delete()
>> 基本new如何记录分配的内存大小供delete使用
>> 申请和释放一个数组
>> 为什么new/delete、new[]/delete[]要配套使用
>
> 2 智能指针总述
> 3 `shared_ptr`基础
>> 常规初始化(`shared_ptr`和`new`配合)
>> `make_shared`函数

### new/delete探秘
#### new/delete是什么？
`new/delete`类对象时，有**初始化/释放的能力**(调用构造函数/析构函数)，这些是`malloc/free`所不能的。
#### operator new()和operator delete()
> new/delete是操作符，operater new()和operator delete()是函数

- `new`简单理解为做了两件事：a)分配内存(实际上通过`operator new()`)；b)给内存初始化
- `delete`也做了两件事：a)反初始化(调用析构函数)；b)释放内存(`operator delete()`)

##### 基本new如何记录分配的内存大小供delete使用
不同编译器new内部有不同的实现方式，new内部有记录机制，记录分配出多少内存。
#### 申请和释放一个数组

```cpp
int *p = new int[2];
delete[] p;
```
###### 如果申请一个类数组，会在内存中存入该数组中类的个数，以便与调用等量的析构函数。
### 智能指针总述
- **裸指针**：直接用`new`返回的指针，强大灵活，但是需要开发者全程维护。
- **智能指针**：理解为“裸指针”进行了包装，能够“自动释放所指向的对象内存”。C++标准库std提供了四种智能指针：
	- 都是类模版
		- `auto_ptr`(C++98)*已经被unique_ptr取代*
		- `unique_ptr`(C++11)：独占式指针。同一时间内，只有一个指针指向该对象
		- `shared_ptr`(C++11)：共享式指针。多个指针指向同一个对象，最后一个指针被销毁时，这个对象会被销毁
		- `weak_ptr`(C++11)用来辅助shared_ptr
- 用来帮助我们进行**动态分配对象**(new出来的对象)的生命周期的管理。能够有效防止内存泄漏

### shared_ptr基础
#### 常规初始化(shared_ptr和new配合)
> 每个share_ptr的拷贝都指向相同的内存

**工作原理**：***引用计数***。只有最后一个指向该内存的`shared_ptr`不需要再指向该对象时，才会析构这个对象。**计数**的作用是每增加一个`shared_ptr`count + 1，销毁指针到count为0时，就会释放内存。

```cpp
std::shared_ptr<int> pi(new int(100));	
//智能指针explicit不允许隐式转换
//故std::shared_ptr<int> pi = new int;是错误的
```
#### make_share函数：标准库里的函数模版
在自定义删除器时会受到限制

```cpp
shared_ptr<int> pt = make_shared<int>(100);
```

## 03 shared_ptr常用操作、计数、自定义删除器
> 1 shared_ptr引用计数的增加和减少
>> 引用计数的增加
>> 引用计数的减少
>
> 2 shared_ptr指针常用操作
>> use_count()
>> unique()
>> reset()
>> *解应用
>> get()
>> swap()
>> =nullptr
>> 智能指针名字作为判断条件
>> 指定删除器以及数组问题

### shared_ptr引用计数的增加和减少
每个`shared_ptr`都会记录有多少个其他的`shared_ptr`指向相同的对象。
### shared_ptr指针常用操作
- `use_count()`：**返回多少个智能指针指向某个对象**，主要用于调试目的
- `unique()`：**是否该智能指针独占某个指向的对象**，如果是，返回True
- `reset()`：**复位/重置**
	- **不带参数时**
		- 若该指针是唯一指向该对象的指针，那么释放该对象，并将该指针置空(nullptr)
		- 若该指针不是唯一指向该对象的指针，那么不释放该对象，但计数减一，该指针置空(nullptr)
	- **带参数时**(一般是new出来的指针)
		- 若该指针是唯一指向该对象的指针，那么释放该对象，并将该指针指向新对象
		- 若该指针不是唯一指向该对象的指针，那么不释放该对象，但计数减一，该指针指向新对象
- `*解应用`：**获得指针指向的对象**
- `get()`：**返回保存的指针(裸指针)**。用于有些函数的参数需要的是一个内置裸指针而不是智能指针
- `swap()`：**交换两个智能指针所指向的对象**
- `=nullptr`
	- 将所指向的对象引用计数减一，若引用计数变为0，则释放该指针指向的对象
	- 将智能指针置空
- **指定删除器以及数组问题**
	- 可以指定自己的删除器函数取代系统的默认删除器
	- 管理动态数组时

```cpp
//定义一个删除器函数
void deletefunc(int *p)
{
	delete []p;
}
shared_ptr<int> pt(new int[100], deletefunc);

//打包
template<typename T>
shared_ptr<T> make_array(size_t n)
{
	return shared_ptr<T>(new T[n], default_delete<T[]>());
}
shared_ptr pt = make_array<int>(3);	//长度为3的整形数组，自定义删除器

//lambda函数做自定义删除器
shared_ptr<int> pt(new int[10], [](int *p) {
	delete []p;
	}

//default_delete做删除器
shared_ptr<int> pt(new int[10], default_delete<int[]>());
	
//C++17
shared_ptr<int[]> pt(new int[10]);	//在<>中加[]
```
`size_t` **源码中** -> `typedef unsigned __int64 size_t;`

- 32位系统的size_t是4字节的unsigned int
- 64位系统的size_t是8字节的unsigned long long

	**unsigned int** 0～4294967295
	**int** -2147483648～2147483647
	**unsigned long** 0～4294967295
	**long** -2147483648～2147483647
	**long long的最大值**：9223372036854775807
	**long long的最小值**：-9223372036854775808
	**unsigned long long的最大值**：18446744073709551615
	
	**__int64的最大值**：9223372036854775807
	**__int64的最小值**：-9223372036854775808
	**unsigned __int64的最大值**：18446744073709551615
## `weak_ptr`概述、`weak_ptr`常用操作、尺寸
> 1 weak_ptr概述
>> weak_ptr的创建
>
> 2 weak_ptr常用操作
>> use_count()
>> expired()
>> reset()
>> lock()
>
> 3 尺寸问题

### weak_ptr概述
**`weak_ptr`**：**用来辅助**`shared_ptr`**进行工作**。这个智能指针指向一个由`shared_ptr`管理的对象。但是它并不控制所指向对象的生命周期(不会改变`shared_ptr`的引用计数)。`shared_ptr`能够照常释放所指向的对象。
#### weak_ptr的创建
一般都用`shared_ptr`初始化。

```cpp
auto pi = make_shared<int>(100);
weak_ptr<int> pwi(pi);	
//不会改变强引用(strong ref)的引用计数，但是会增加弱引用(weak ref)计数
```

### weak_ptr常用操作
- `use_count`：**获取当前所观测资源的强引用计数**
- `expired()`：**是否过期，用来判断所观测资源是否被释放**
- `reset()`：**将该弱引用指针设置为**
- `lock()`：功能是**检查`weak_ptr`所指向的对象是否存在**。如果存在返回一个指向该对象的`shared_ptr`，如果不存在则返回一个空的`shared_ptr`

```cpp
//接着
auto pi2 = pwi.lock();	//会使强引用加1，pwi仍是弱引用
```
### 尺寸问题
`weak_ptr`的尺寸和`shared_ptr`一样大，是裸指针的2倍(8字节)。实际上在它们内部包含了两个指针。

## 05 shared_ptr使用场景、陷阱、性能分析、使用建议
> 1 `std::shared_ptr`使用场景
> 2 `std::shared_ptr`使用陷阱分析
> 3 性能说明
>> 尺寸问题
>> 移动语义

### `std::shared_ptr`使用陷阱分析
- **慎用裸指针**
	- 当把一个普通裸指针绑定到了一个shared_ptr上之后，内存管理的责任就交给了智能指针，这时就不应该再用裸指针访问shared_ptr指向的内存了
	- 不能用裸指针初始化多个shared_ptr，会导致多个智能指针之间不关联，删除器会由于两次释放相同内存而报错
- **慎用get()返回的指针**
	- get返回的指针不能delete，否则会异常
	- 不能将其他智能指针绑到get返回的指针上
- **不要把类对象指针(this)作为shared_ptr返回，改用`enable_shared_from_this`**(工作中需要返回该调用函数本身的类的智能指针时使用)
	- 工作原理：enable_shared_from_this中又一个弱指针weak_ptr，这个弱指针能够监视this，调用`shared_from_this`时，实际上调用了这个weak_ptr的lock方法
```cpp
class CT : public enable_shared_from_this<CT>
{
public:
	shared_ptr<CT> getself()
	{
		return shared_from_this(); //这个是enable_shared_from_this类模板中的方法
	}
};
```
### 性能说明
##### 尺寸问题
`shared_ptr`和`weak_ptr`均占8个字节，也就是两个指针，一个指针指向该指向对象的智能指针；一个指针指向控制块(包括强引用计数、弱引用计数、删除器、分配器等)

##### 移动语义
==移动构造一个新的智能指针==
```cpp
shared_ptr<int> p1(new int(100));
shared_ptr<int> p2(std::move(p1));
```
会将p1指向的对象移动给p2，p1不再指向该对象(变成空指针)。
## 06 unique_ptr概述、常用操作
> 1 unique_ptr概述
>> 常规初始化
>> make_unique函数
>
> 2 unique_ptr常用操作

### unique_ptr概述
独占式的概念(专属所有权)：同一个时刻只能有一个unique_ptr指向一个对象。当被销毁时，所指向的对象同时也被销毁。
```cpp
unique_ptr<int> pt(new int(103));

//c++14:make_unique
unique_ptr<int> pt = make_unique<int>(104);
auto pt = make_unique<int>(105);
```
### unique_ptr常用操作
- **移动语义**
```cpp
unique_ptr<string> ps1(new string("ingenious"));
unique_ptr<string> ps2(std::move(ps1));
```
- **`release()`**：放弃对指针的控制权，切断指针和对象之间的联系。返回裸指针，并将该智能指针置空，该裸指针需手动释放
```cpp
unique_ptr<string> ps1(new string("ingenuous"));
unique_ptr<string> ps2(ps1.release());
```
- **`reset()`**
	- 不带参数：释放智能指针指向的对象，并把指针置空
	- 带参数：释放智能指针指向的对象，并将智能指针指向括号内的新对象
```cpp
unique_ptr<string> ps3(new string("fractious"));
ps3.reset(ps1.release());
```
- **`= nullptr`**：释放指向的对象并置空该智能指针
- **`get()`**：返回智能指针中保存的裸指针
- **`swap()`**：交换两个指针所指向的对象
- ==转换成`shared_ptr`形式==：如果unique_ptr为右值就可以转换成shared_ptr形式
```cpp
auto func()
{
	return unique_ptr<string> st(new string("fd"))；	//返回的是临时对象，是右值
}

shared_ptr<string> p = func();
```
## 07 返回unique_ptr、删除器、尺寸、智能指针总结
> 1 返回unique_ptr
> 2 指定删除器
> 3 尺寸问题
> 4 智能指针总结

### 指定删除器
**格式：** `unique_ptr<指向的对象类型, 删除器类型> 指针名`
```cpp
void mydelete(string* p)
{
	delete p;
	p = nullptr;
}

//typedef void (*pr) (string *);
//using pr = void (*) (string *);
typedef decltype(mydelete)* pr;
unique_ptr<string, pr> point(new string("hei"), mydelete); 
```
unique_ptr自定义删除器需要在模板参数中加入删除器函数的类型，例中提供了用函数指针做模板参数的情况。
#### 尺寸问题
通常情况下，unique_ptr和裸指针的大小一样(4字节)。但是自定义删除器就可能增加所占用的内存。
### 总结
- 智能指针的设计目的：帮助释放内存，以防内存泄漏
- auto_ptr为什么被废弃？
	- 不能再容器中保存
	- 不能从函数中返回auto_ptr
	- C++11提出的unique_ptr相比C++98的auto_ptr更安全
	- ... ...
	
# 五、并发与多线程
(这章还没写)

# 六、内存高级话题
**Author:** XFFer_
## 01 new、delete的进一步认识
> 1 总述与回顾
> 2 从new说起

### 从new说起
##### new类对象时加不加括号的区别
```cpp
class A {
public:
	int m_i;
};
A* pa = new A();	//m_i = 0
A* pa_t = new A;	//m_i = 随机值
```
- 当类有成员变量，带有括号的初始化会把一些和成员变量有关的内存清零
- 当类中有构造函数，则这两种写法得到的结果没有区别

##### new干了啥
new 可以叫**关键字**/**操作符** `fn + F12`会跳转到operator new。

可以在Debug状态下使用 `调试` -> `窗口` -> `反汇编`得到如下：
![反汇编](https://img-blog.csdnimg.cn/20200221112413586.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70 =380x)
这里可以看出`call  operator new`这个函数
![malloc](https://img-blog.csdnimg.cn/20200221112904108.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70 =380x)
这里可以看到`call malloc`C语言中内存分配函数malloc(size传入堆中分配内存的大小)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200221114155946.JPG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
这里可以看到`call operator delete`这个函数
##### 简化流程
```mermaid
flowchat
st=>start: new一个对象
e=>end: 释放该对象
op1=>operation: 调用operator new函数
op2=>operation: C语言的malloc()函数
op3=>operation: C语言的free()函数
op4=>operation: 调用operator delete函数
op5=>operation: 调用类对象的构造函数
op6=>operation: 调用类对象的析构函数
cond=>condition: 是否为类对象
op7=>operation: 调用operator new函数
op8=>operation: C语言的malloc()函数
op9=>operation: C语言的free()函数
op10=>operation: 调用operator delete函数

st->cond
cond(yes)->op1->op2->op5->op6->op4->op3->e
cond(no)->op7->op8->op10->op9->e
```
## 02 new细节探秘，重载类内operator new、delete
> 1 new内存分配细节探秘
> 2 重载类内operator new和operator delete操作符
> 3 重载类内operator new[]和operator delete[]操作符

### new内存分配探秘
先介绍一个函数 **`void *memset(void *s, int ch, size_t n)`**。
作用是：将某一块内存中的内容全部设定为指定的值。
```cpp
char* ppchar = new char[10];
memset(ppchar, 0, 10);	//这里将这分配的十字节的内存初始化为0
delete[] ppchar;
```
内存的回收，实际上并不是只释放了分配的内存，影响的范围很广。给我一种感觉是：最初分配的多个变量的内存并不是连续的，会产生内存碎片，free为了避免碎片导致的内存没有足够的空间储存更大的信息，是一种很复杂的工作。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200221170436481.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
### 重载类内operator new和operator delete操作符
```cpp
class A {
public:
	static void* operator new(size_t size);
	static void operator delete(void *phead);
};

void* A::operator new(size_t size)
{
	A* ppoint = (A*)malloc(size);
	return ppoint；
}
void A::operator delete(void *phead)
{
	free(phead);
}

A* a = new A();
A* a_c = ::new A();	//::
```
如果做new前加 **`::`** 全局操作符，那就不会调用自己重载的operator new/delete函数了，而是调用系统内部的。
##### 重载类内operator new[]和operator delete[]操作符
和上一模块的代码很相似，当初始化类对象数组时，只会调用**一次**operator new[]，调用数组长度的构造函数；释放时，先调用数组长度的析构函数，再调用**一次**operator delete[]。在分配内存时还会多分配4个字节用来储存数组的长度。

## 03 内存池概念、代码实现和详细分析
> 1 内存池的概念和实现原理概述
> 2 针对一个类的内存池实现演示代码
> 3 内存池代码后续说明

### 内存池的概念和实现原理概述
`malloc`：内存浪费，频繁分配小块内存，浪费更加明显。

**Q:** 内存池要解决的问题?
**A:** 减少`malloc`的调用次数。

**内存池的实现原理：** 用malloc申请一大块内存，当需要分配时，就从该内存池一点点分配给对象。

### 针对一个类的内存池实现演示代码
```cpp
class A
{
public:
	static void* operator new(size_t size);
	static void operator delete(void* phead);
	static int m_iCout;	//分配计数统计，每new一次，就统计一次
	static int m_iMallocCount;	//每malloc一次，就统计一次
private:
	A* next;
	static A* m_FreePosi;	//总是指向一块可以分配出去的内存的首地址
	static int m_sTrunkCout;	//一次分配多少倍的该类内存
};
int A::m_iCout = 0;
int A::m_iMallocCount = 0;

A* A::m_FreePosi = nullptr;
int A::m_sTrunkCout = 5;

void* A::operator new(size_t size)
{
	A* tmplink;
	if (m_FreePosi == nullptr)
	{
		size_t relsize = m_sTrunkCout * size;	
		//申请内存池的大小
		m_FreePosi = reinterpret_cast<A*>(new char[relsize]);	
		//传统new，调用系统底层的malloc，char是1字节，这里开辟了relsize个字节的内存空间	
		tmplink = m_FreePosi;

		//把分配出的一大块内存彼此链起来供后续使用
		for (;tmplink != &m_FreePosi[m_sTrunkCout -1]; ++tmplink)
		{
			tmplink->next = tmplink + 1;	
			//这里对tmplink->next的改动，实际上也是对m_FreePosi的改动，进入循环前地址传递
		}
		tmplink->next = nullptr;
		++m_iMallocCount;
	}
	tmplink = m_FreePosi;
	m_FreePosi = m_FreePosi->next;	//把内存池中的下一个指针给m_FreePosi用于下次分配
	++m_iCout;
	return tmplink;
}

void A::operator delete(void *phead)
{
	(static_cast<A*>(phead))->next = m_FreePosi;
	m_FreePosi = static_cast<A*>(phead);
}
```
![内存池](https://img-blog.csdnimg.cn/2020022120303920.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
这里介绍一个库 **`#include <ctime>`** 单位：ms
1. `clock_t start, end;`
2. `start = clock();`
3. `end = clock();`
4. `cout << "start和end两条语句之间夹着的所有语句的运行时间是：" << end - start << endl;`

## 04 嵌入式指针概念及范例、内存池改进版
> 1 嵌入式指针
> 2 内存池代码的改进

### 嵌入式指针(embedded pointer)
> 一般应用在内存池中，为了节省下每次指向下个内存池中的内存地址的指针

**嵌入式指针工作原理：** 借用对象所占用内存空间的前4个字节，这4个字节用来链住空闲的内存块；一旦某一块被分配出去，这4个字节就可以正常使用。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020022120392519.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
```cpp
class Test_Embed {
public:
	int a;
	int b;	//为了凑4字节
	struct obj
	{
		struct obj* next;	//这个next就是个嵌入式指针
	};
};

Test_Embed::obj* ptemp;
Test_Embed test;
ptemp = (Test_Embed::obj*)&test;	//将类对象的首地址也就是前4个字节的首地址给嵌入式指针
ptemp->next = nullptr;	//这里的nullptr用下一个内存块的首地址就可以实现链表
```
### 内存池代码的改进
```cpp
class myallocator
{
public:
	void *allocate(size_t size)
	{
		obj *tmplink;
		if (m_FreePosi == nullptr)	//if内的内容就是在做链接
		{
			size_t realsize = m_sTrunkCout * size;
			m_FreePosi = (obj*)malloc(realsize);	//返回值void*万能指针
			tmplink = m_FreePosi;	//让tmplink这个嵌入式指针指向开辟内存的首地址

			for (int i = 0; i < m_sTrunkCout - 1; ++i)	//一直链接到最后一个内存块
			{
				tmplink->next = (obj*)((char*)tmplink + size);	//指向下一个内存块的首地址
				tmplink = tmplink->next;
			}
			tmplink->next = nullptr;	//最后一个内存块的next指针指向空用来下一次调用if，malloc一个新的内存池
		}
		//现在整个内存池的每个block都已经链接好了，next指针就指向下一个内存块
		templink = m_FreePosi;
		m_FreePosi = m_FreePosi->next;	//跟踪可用内存块
		return tmplink;
	}
	void deallocate(void* phead)
	{
		((obj*)phead)->next = m_FreePosi;
		m_FreePosi = (obj*)phead;
	}
private:
	struct obj
	{
		struct obj* next;
	};
	int m_sTrunkCout = 5;
	obj* m_FreePosi = nullptr;
};

//如何使用
class useit {
public:
	int m_i;
	int m_o;	//这两个纯属为了使类对象>4字节
public:
	static myallocator myalloc;	//在下部定义
	static void* operator new (size_t size)
	{
		return myalloc.allocate(size);	//返回的是一个指针
	}
	static void operator delete (void* tmp)
	{
		myalloc.deallocate(tmp);
	}
};
myallocator useit::myalloc;	//定义静态变量

//用宏简写
#define DECLEAR_POOLING_ALLOC() \
public:\
	static myallocator myalloc;\
	static void* operator new (size_t size)\
	{\
		return myalloc.allocate(size);\
	}\
	static void operator delete (void* tmp)\
	{\
		myalloc.deallocate(tmp);\
	}
#define IMPLEMENT_POOL_ALLOC(classname) \
myallocator classname::myalloc

class A {
	DECLEAR_POOLING_ALLOC()
public:
	int m_j;
	int m_k;
};
IMPLEMENT_POOL_ALLOC(A);
```
## 05 重载new、delete，定位new及重载

> 1 定位new (placement new)
> 2 多种版本的operator new重载

### 定位new(placement new)
> 没有placement delete

**功能：** 在已经分配的原始内存中初始化一个对象。
**格式：** `new (地址) 类对象()`
```cpp
//定位new也可以重载
void* operator new (size_t size, void* ppoint)
{
	return ppoint;
}
```
#### 多种版本的operator new重载
###### new调用了operator new的函数，和其他函数形式一样，operator new也可以通过不同参数表进行重载，但是这是个很猎奇的操作，通常不建议使用。

# 七、STL标准模板库大局观
**Author:** XFFer_
> 先分享一本 **《C++ 标准库 第二版》** ，望在STL的道路上从入门到放弃！(开玩笑的啦，愈行愈远~)
**链接：** https://pan.baidu.com/s/1nna7m5F11poNNvEi2ydOyQ 
**提取码：** otld 
## 01 STL总述、发展史、组成，数据结构谈
> 1 几个概念
> 2 推荐书籍
> 3 算法和数据结构浅谈
> 4 STL发展史和各个版本
> 5 标准库的使用说明
> 6 STL的组成部分

### 几个概念
- **C++标准库**：C++ Standard Library
- **标准模板库**：Standard Template Library(STL)
- **泛型编程**：Generic Programming

### 推荐书籍
![STL](https://img-blog.csdnimg.cn/20200222153951654.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
![C++标准库第二版](https://img-blog.csdnimg.cn/20200222153916548.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
>	**《STL源码剖析》**
> **链接：** https://pan.baidu.com/s/1apswforzS6dp5-3S05SKeA 
**提取码：** gk0l
> **《C++标准库》**
> **链接：** https://pan.baidu.com/s/1nna7m5F11poNNvEi2ydOyQ 
**提取码：** otld 

### STL发展史和各个版本
- **HP STL：** 惠普STL，是所有STL实现版本的始祖
- **SGI STL：** 参考惠普STL实现的，Linux下的GNU C++(gccc, g++)使用
- **P.J.Plauger STL：** Visual C++使用

### STL的组成部分
- **容器：** vector、list、map
- **迭代器：** 用于遍历或者访问容器中的元素
- **算法：** (函数)，用来实现一些功能，search、sort、copy...
- **分配器**
- **其他：** 适配器、仿函数等

## 02 容器分类、array、vector容器精解
> 1 容器的分类
> 2 容器的说明
>> `array`
>> `vector`

### 容器的分类
![容器](https://img-blog.csdnimg.cn/20200222165004866.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
- **顺序容器**(Sequence Container)：能控制插入位置
	- `array` `vector` `deque` `list` `forward_list`
	
- **关联容器**(Associative Container)：元素是 ==“键值对”==，适合用来查找。能够控制插入内容，但不能控制插入位置
	- `set` `multiset` `map` `multimap`
- **无序容器**(Unordered Container)：C++11推出，元素位置不重要，重要的是否存在该元素
	- `unordered_set` `unordered_multiset` `unordered_map` `unordered_multimap`
![无序容器](https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTYwNDEwMTIzNTE4Njky?x-oss-process=image/format,png)
![](https://imgconvert.csdnimg.cn/aHR0cDovL2ltZy5ibG9nLmNzZG4ubmV0LzIwMTYwNDEwMTIzNTI1NzM5?x-oss-process=image/format,png)
### 容器的说明
#### array
> 内存空间是连续的，大小是固定的

**使用形式：** `array<type_name, N> value_name`	可以就当做数组来用。
#### vector
vector有一个“空间”的概念，**容器内存是紧挨着的**，故vector从末尾添加元素`push_back`时，如果容器空间不足就会重新寻找一个足够大的内存存放对象。

容器中有多少个元素可以用`size()`来看，有多少空间可以用`capacity()`，$capacity\geq size$。

[vector基础知识](https://blog.csdn.net/qq_44455588/article/details/104389245)在前面的章节有所提到。

当`erase(iter)`容器内部一个元素时，处理是比较高效的，其后的元素地址都会顺次移动，仍然是连续的内存。
当`insert(iter, value)`插入一个元素时，代价很大，会造成其后的元素重新构造，导致降低效率。

故可以使用`reserve(size)`提前留出空间capacity，可以大量提高程序的预留效率。
## 03 容器的说明和简单应用例续
> 1 deque和stack
> 2 queue
> 3 list
> 4 其他
>> forward_list
>> set/map
>> unordered_set、unordered_multiset等

![容器](https://img-blog.csdnimg.cn/20200222165004866.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
### deque和stack
**`deque`** ：**双端数列**(double-ended queue) ，==分段连续内存==，以分段数组的形式存储。
```cpp 
#include <queue>

deque<type_name> value_name;

value_name.push_front();	//从队列的前面插入
value_name.push_back(); 	//从队列的后面插入
value_name.pop_front();		//从队列的前面删除
value_name.push_back();		//从队列的前面删除
```
**`stack`**：**堆栈/栈**，只有一个开口，==后进先出==，后进会放在栈顶，先进会压在栈底，不支持从总结插入/删除数据。deque实际上是包含着stack的功能的。

**`queue`** ：**普通队列** ==先进先出==
### list：双向链表
不需要内存是连续的，查找效率不突出，但是在任意位置插入和删除元素非常迅速。
- `begin()/end()` 返回一个起始位置/末端下一个位置的iterator
- `push_back()` `push_front()`	在末端/头部插入元素
- `empty()`	判断是否为空
- `resize()`	将list长度改为容纳n个元素
- `clear()`	清空
- `front()` `back()`	获取头部/末端元素，不能为空
- `pop_front()` `pop_back()`	从头部/末端删除一个元素
- `insert()`	插入一个或多个元素
	- `insert(iter, value)`
	- `insert(iter, number_of_v, value)`
- `erase()`	删除元素/区间内(用iter)元素
###### `vector` 和 `list`之间的差别
- vector类似于数组，内存空间是连续的，list双线链表，内存空间并不连续
- vector从中间或者开头插入元素效率比较低；但是list插入元素效率非常高
- vector当内存不足时，会重新找一块内存，对原来的内存对象做析构，再在新的内存重新构造
- vector能够高效的随机存取，而list做不到。vector可以通过迭代器，而list需要沿着链表一个个找，直到找到所需的元素

这里vector的细节知识可以参考[C++中list用法详解](https://blog.csdn.net/yas12345678/article/details/52601578)，本文只是简单的总述STL标准库。
### 其他
- **`forward_list`**：单向链表(受限list)
- **`set / map`**：关联容器。内部实现的数据结构多为红黑树。这些容器==没有==`push_front/back`的操作，因为内存并不是规律的
	- **常用操作**↓
```cpp
#include <map>
#include <functional>
#include <string>

map<int, string> mymap;
map<string, function<int(int)>> mymap2;	//可以存入函数类型为int(int)的函数

//插入的五种方式
mymap.insert(pair<int, string>(000, "first"));

mymap.insert(map<int, string>::value_type(000, "first"));

mymap.insert(std::make_pair(000, "first"));

mymap.insert({000, "first"});

mymap[000] = "first";	//相同key可覆盖

//find查找元素，返回迭代器指向当前查找元素的位置，否则返回map::end()位置即最后一个元素后(空)
auto iter = mymap.find(001);

if (iter != mymap.end())
	cout << "find it!" << endl;
else
	cout << "do not find" << endl;

//删除与清空元素
auto iter = mymap.begin();
mymap.erase(iter);	//用迭代器删除

mymap.erase(000);	//用键删除

mymap.erase(mymap.begin(), mymap.end());	//范围删除，等同于mymap.clear();
```
**快捷键补充** 
**`shift+Home`** 取光标前本行内容
**`shift+End`** 取光标后本行内容
## 04 分配器概述、使用，工作原理说
> 1 分配器概述
> 2 分配器的使用
> 3 其他的分配器及原理说
> 4 自定义分配器

>这节很水smirk~，因为我菜所以没有去详细了解分配器
### 分配器概述&分配器的使用
> 内存分配器，通过测试没有采用内存池的技术

- `allocate(num)` 是分配器内的重要函数，用来分配内存，这里的num值几个对象而不是字节数
- `deallocate(point, num)` 用于释放函数，point是指向分配内存的指针

↓图为侯捷老师讲授分配器时使用过的
![分配器 侯捷](https://img-blog.csdnimg.cn/20200224001414378.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQ0NDU1NTg4,size_16,color_FFFFFF,t_70)
这里可以参考[学习资料集聚地—小破站](https://www.bilibili.com/video/av68567064?p=7)侯捷老师的STL源码剖析。
## 05 迭代器的概念和分类
(这版今天更)
