---
layout: post
title: "[Algorithm] Queue"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [Algorithm]
categories: [Algorithm]
---

------------------------------------------------------------------------------------------------------------

## 큐(Queue)의 정의
큐(Queue)는 ~~~~~~~  
가장 먼저 삽입된 데이터가 가장 먼저 제거되는 선입선출(FIFO - First In First Out) 형태의 자료구조이다.
![image](https://user-images.githubusercontent.com/52437364/82183351-c4530600-9920-11ea-999f-651fcd5fff9d.png)
가장 먼저 입력된 데이터를 front라고 하면 가장 나중에 입력된 데이터를 rear라고 한다.  
데이터의 삽입은 rear에서 이루어지고 삭제는 front에서 이루어지기 때문에 큐를 구현하기 위해서는 front와 rear를 관리하는 **배열**을 이용하거나 font노드와 rear노드를 관리하는 **연결 리스트**를 이용할 수 있다.

- 삽입(insert)
큐에 새로운 데이터를 삽입하는 작업을 insert라고 한다.  
이는 리스트의 끝 부분을 가리키는 rear에서 발생하며 데이터가 삽입될 때 하나 증가시킨 후 새로운 데이터를 삽입하도록 구현한다.  
- 삭제(remove)
큐에서 데이터를 제거하는 작업을 remove라고 하며 이는 항상 front에서 발생한다.  
front가 가리키고 있ㄴ는 데이터를 꺼낸 후 front 값을 하나 증가시키도록 구현한다.  
front값이 rear를 추월하게 되면 더 이상 제거할 데이터가 없는 상태, 즉 자료가 없는 빈 큐임을 의미한다.  
- 읽기(peek)
큐에서 font가 가리키는 데이터를 읽는 작업을 peek라고 하며 데이터를 제거하지 않고 읽는 작업만 수행하므로 front값을 변경시키지 않는다.  
<br/>
<br/>

## 배열을 이용한 큐 구현
<br/>
<br/>
<br/>
**참고자료**<br/>
[개발이 하고 싶어요](https://hyeonstorage.tistory.com/263)
