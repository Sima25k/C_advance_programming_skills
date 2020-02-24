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
