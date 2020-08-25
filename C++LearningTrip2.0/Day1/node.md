## C++ learningTrip 2.0_Day_1

Linking和Compiling,是编译器编译的两个过程，
Code:
```c++
#include<iostream>
//这个const char*就是输入一串字符
void Log(const char* message)
{
  std::cout<<messsage<<std::endl;
}
int mian()
{
  Log("Hello World");
  std::cin.get();
}
```

编译器的原理：
预处理代码（pre-process)——》标记解释（tokenizing）—和解析（parsing）阶段：把代码处理成编译器可听懂和处理的语言——》生成abstract syntax tree（抽象语法树），也就是代码的表达，以这种形式

总结：编译器把代码穿换成常数资料或者指令（constant data & instructions），抽象语法树生成后，产生的代码就是CPU执行的机器码


头文件实际效果：将头文件的code复制到#include处，仅此而已
演示代码
EndBrace.h
```c++
}//此头文件中仅仅包含一个右括号
```
Math.cpp
```c++
int main()
{
 return 0;
#include"EndBrace.h"//EndBrace.h的内容会复制到这里，编译不会报错
```


