## C++ learningTrip 2.0_Day_2

How does Linker work in compiler?

ctrl+F7, 只会编译，并不会Linking，只有build或者F5，编译完成后会linking

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1618_1.png)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1620_1.png)




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
![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1622_1.png)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1624_1.png)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1626_1.png)




条件语句：
![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day2/image/1628_1.png)
