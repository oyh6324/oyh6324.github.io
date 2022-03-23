---
title: "Unity. 오브젝트 풀링(Object Pooling) 알아보기"
categories:
  - Unity
tags:
  - Unity
  - 중급
---

## 🌟 오브젝트 풀링이란?

2D는 괜찮지만 3D에서 오브젝트를 생성하고 파괴하는 건 무거운 작업이다. 생성할 때마다 메모리 할당하고 초기화하고...후에 파괴할 때 가비지 컬렉팅으로 프레임 드랍이 발생할 수 있음!

그래서 오브젝트 풀링으로 해결해야 한다.



## 🌟 풀링 방법

오브젝트를 담을 오브젝트 풀을 구성한다. 대충 비어 있는 오브젝트 하나 만들면 됨.

풀링할 오브젝트 생성해서 풀이 그 오브젝트들을 관리하게 한다. PoolManager!

외부에서 원하는 오브젝트를 꺼내서 쓴다.

사용이 끝나면 다시 풀에 넣어준다.

원하는 오브젝트가 이미 사용 중이라면 새로운 오브젝트를 생성함.



공부하자 영현아~