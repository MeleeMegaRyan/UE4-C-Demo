## DAY3:

### How to setup C++ project better?

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/1_1.jpg)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/1_2.jpg)

才此处可进行生产文件夹而不是Filter，可以帮助你更好的管理文件

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/1_3.jpg)

可手动设置项目build的时候生产的文件的位置，以便于更好的找到想找的

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/1_4.jpg)

### Control Flow in c++:contiune,break,return

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/2_1.jpg)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/2_2.jpg)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/2_3.jpg)

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/2_4.jpg)

## Pointers in c++

编程中最重要的部分是内存，内存就像一条街道，每个byte就像街道上的一户房屋，而pointer就是某个特殊房屋的地址，对内存内的内容进行修改，就需要知道房屋的地址

所有类型的指针都是一个整除，存放一个内存地址



```c++
#include<iostream>
#define log(x) std::cout<<x<<std::endl

int main()
{
    //在栈上创建的指针
    void* ptr = 0;//意味着这个指针指向的内容为void，内存地址（指针）为0（nullptr）
    int var =8;
    void *ptr2 = &var;//&为取地址符，得到var在内存中的地址，赋予给ptr2（指针）
    
    char* ptr3 = new char[8];//创建一个8字节的数组，用指针指向
    memset(ptr3,0,8);//在内存上开辟这个指针指向的数组空间
    delete[] ptr3; 
    std::cin.get(); 
}
```

## Reference in c++

> 如果想通过一个函数直接改变一个变量本身，通过指针的方法可做到

```c++
#include<iostream>
#define log(x) std::cout<<x<<std::endl


int Increment(int* value)
{
    (*value)++;
    
}
int main()
{
    int a = 5;
    Increment(&a);
    std::cin.get(); 
}
```

> 通过引用，可以更简单的做到

```c++
int Increment(int& value)
{
    value++;
}
int main()
{
    int a = 5;
    Increment(a);
    std::cin.get();
}
```



## Classes in c++

```c++
#include<iostream>
#define log(x) std::cout<<x<<std::endl

class player
{
    public:
    int x,y;
    int speed;
    void Move(int xa,int ya)
    {
        x += xa*speed;
        y += ya*speed;
    }
}
int main()
{
  player player;
    player.Move(1,1);
}
```





## Static in C++

static修饰的变量或者函数，仅仅存在于当前CPP(编译单元)下，LNK不会读取

![image](https://github.com/MeleeMegaRyan/UE4-C-Demo/blob/master/C%2B%2BLearningTrip2.0/Day3/Image/3_1.jpg)
