---
layout: post
title: "[C++] 디폴트 인수"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [C++]
categories: [C++]
---

------------------------------------------------------------------------------------------------------------

## 디폴트 인수(default argument)
C++에서 새롭게 정의된 디폴트 인수는 기본값이 미리 정의되어 있는 인수를 의미한다.  
함수를 호출할 때 인수를 전달하지 않으면, 함수는 자동으로 미리 정의되어 있는 디폴트 인수값을 사용하게 된다.  
물론 인수를 전달하여 함수를 호출하면, 디폴트 인수값이 아닌 전달된 인수를 가지고 호출하게 된다.
<br/>
<br/>

## 디폴트 인수의 설정
C++에서 디폴트 인수를 설정할 때에는 다음과 같은 사항에 주의해야한다.  
1. 디폴트 인수는 함수의 원형에만 지정할 수 있다.
2. 디폴트 인수는 가장 오른쪽부터 시작하여 순서대로만 지정할 수 있다.
3. 가운데 인수들만 별도로 디폴트 인수를 지정할 수 는 없다.

#### 예제
{% highlight cpp %}
1. void Display(int x, int y, char ch, int z = 4); //가능
2. void Display(int x, int y, char ch = 'a', int z = 4); //가능
3. void Display(int x, int y = 2, char ch, int z = 4); //오류
4. void Display(int x, int y = 2, char ch, int z); //오류
{% endhighlight %}
<br/>
<br/>

## 디폴트 인수가 설정된 함수의 호출
함수로 전달된 인수는 왼쪽부터 순서대로 매개변수 목록에 대입된다.  
따라서 디폴트 인수가 설정된 함수를 호출할 때에는 인수의 전달을 건너뛸 수 없다.  

#### 예제
{% highlight cpp %}
void Display(int x, int y, char ch = 'a', int z = 4); //함수의 원형

1. Display(1, 2); //가능
2. Display(3, 4, 'b'); //가능
3. Display(5, 6, 'c', 9); //가능
4. Display(7, 8, 9); //오류 : 인수 전달은 건너뛸 수 없음
{% endhighlight %}

<br/>
<br/>
<br/>
**참고자료**<br/>
[코딩의 시작, TCP School](http://tcpschool.com/cpp/cpp_cppFunction_default)
