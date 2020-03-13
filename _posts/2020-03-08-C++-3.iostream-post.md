---
layout: post
title: "[C++] iostream"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [C++]
categories: [C++]
---

------------------------------------------------------------------------------------------------------------
## iostream
C++의 모든 것은 객체로 표현되므로, 입출력을 담당하는 수단 또한 C언어의 함수와는 달리 모두 객체이다.<br/><br/>
C언어의 printf()함수나 scanf()함수처럼 C++에서도 iostream 헤더 파일에 표준 입출력 클래스를 정의하고 있다.<br/><br/>
C++에서는 cout 객체로 출력 작업을, cin 객체로 입력 작업을 수행하고 있다.<br/>
또한, C++에서는 기존의 C언어 스타일처럼 printf()함수나 scanf()함수로도 입출력 작업을 수행할 수 있다.<br/>
<br/>
<br/>
## cout 객체
cout객체는 다양한 데이터를 출력하는 데 사용되는 C++에서 미리 정의된 출력 스트림을 나타내는 객체이다.<br/><br/>
삽입 연산자(<<)는 오른쪽에 위치한 출력할 데이터를 출력 스트림에 삽입한다.<br/>
이렇게 출력 스트림에 삽입된 데이터는 스트림을 통해 출력 장치로 전달되어 출력된다.<br/>
{% highlight cpp %}
cout<<"Hello!";
{% endhighlight %}
<br/>
<br/>
## cin 객체
cin객체는 다양한 데이터를 입력받는 데 사용되는 C++에서 미리 정의된 입력 스트림을 나타내는 객체이다.<br/><br/>
추출 연산자(>>)를 통해 사용자가 입력한 데이터를 입력 스트림에서 추출하여, 오른쪽에 위치한 변수에 저장한다.<br/>
이때 cin 객체는 자동으로 사용자가 입력한 데이터를 오른쪽에 위치한 변수의 타입과 동일하게 변환시켜준다.<br/>
#### 예제
{% highlight cpp %}
#include <iostream>

using namespace std;

int main()
{
	int age;
	cout << "나이를 입력하세요 : ";
	cin >> age;  
	cout << "나이는 " << age << "살 입니다" << endl;
	return 0;
}
{% endhighlight %}
#### 실행결과
    {% raw %}  
    나이를 입력하세요 : 24
    나이는 24살 입니다
    {% endraw %}  
<br/>
<br/>

## C언어 표준 입출력함수와의 차이점
C언어 표준 입출력 함수인 printf함수나 scanf()함수와 C++표준 입출력 객체와의 차이점은 다음과 같다.<br/><br/>
1.삽입연산자(<<)와 추출연산자(>>)가 데이터의 흐름을 나타내므로 좀 더 직관적이다.<br/>
2.++표준 입출력 객체는 입출력 데이터의 타입을 자동으로 변환시켜주므로 더욱 편리하고 안전하다.<br/>
<br/>
<br/>
<br/>
<참고자료><br/>
[코딩의 시작, TCP School](http://tcpschool.com/cpp/cpp_intro_program)
