## C++ learningTrip 2.0_Day_2

How does Linker work in compiler?

ctrl+F7, 只会编译，并不会Linking，只有build或者F5，编译完成后会linking
![3bfc12a843b674af842e5c602bdf8842.png](en-resource://database/1618:1)
![5c67c65aa84ab91a0931445b7a142831.png](en-resource://database/1620:1)


```c++
//static 意味着，linking工作时，有cpp调用这个函数的时候，仅仅在此cpp内部使用，不会出现函数重复出现的错误
static void log(const char* message)
{

}
//同理，inline意味着仅仅调用函数里面的内容，也就是  std::cout<<message<<std::endl;也不会出现重复出现的错误
inline void log(const char* message)
{
  std::cout<<message<<std::endl;
}
```
![462f5493ca5ea28dea77356048644b38.png](en-resource://database/1622:1)
![252c3d33572b74bada9d8c26b92bae93.png](en-resource://database/1624:1)
![c59f93cd0f6b1cc465475a56761f705c.png](en-resource://database/1626:1)


条件语句：
![dfb648333d4842bbdb8261db38c19e22.png](en-resource://database/1628:1)这样会让代码变慢