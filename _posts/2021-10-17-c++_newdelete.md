---
title: "C++. new와 delete로 동적 할당하기"
categories:
  - C++
tags:
  - C++
  - 프로그래밍 언어
  - 중급
  - 동적 할당
  - 포인터
---

## 🌟 C++의 동적 할당

C에서는 동적 할당을 위해 malloc과 calloc, realloc을 사용했지만, C++에서는 간단하게 new와 delete로 동적 할당을 구현할 수 있다.



new는 메모리를 만드는 연산자고, delete는 메모리를 해제하는 연산자다. 연산자이기 때문에 C의 동적 할당보다 빠르다는 장점이 있음!



## 🌟 사용법

```c++
#include <iostream>
using namespace std;

int main()
{
    int* pInt = new int; //4바이트만큼 공간 할당
    *pInt = 1; //메모리에 값 넣음
    delete pInt; //메모리 해제
}
```

사용하는 법은 간단하다. 포인터와 new로 원하는 타입을 만들어 주고, 값을 넣은 뒤, 필요 없어지면 delete 하면 된다.



배열도 만들 수 있는데 배열로 만든 경우,

```c++
int* pArray = new int[10];
delete[] pArray;
```

delete[]로 해제해줘야 한다.



## 🌟 동적 할당을 사용하는 이유

프로그래밍을 하다 보면 메모리 낭비가 심하거나, 한 번에 많이 사용해야 하는 경우가 있는데 그때 정적 변수가 아닌 동적 변수를 사용하면 메모리를 재활용할 수 있어서 굉장히 효율적이다. 



또한 배열같은 경우 공간이 얼만큼 필요한지 알 수 없을 때 동적 할당을 사용하면 후에 원하는 만큼 자리를 잡을 수 있으니 편함!