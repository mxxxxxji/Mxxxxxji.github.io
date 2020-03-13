---
layout: post
title: "[C++] Simple Program"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [C++]
categories: [C++]
---

------------------------------------------------------------------------------------------------------------

## 간단한 C++프로그램

다음은 간단한 C++프로그램의 예제이다.
{% highlight cpp %}
#include <iostream>
#define TEXT "Welcome to C++ Programming!!"

int main()
{
    std::cout << TEXT;
    return 0;
}
{% endhighlight %}
  
    
### main() 함수
C++프로그램은 가장 먼저 main() 함수를 찾고, 그 곳에서부터 실행을 시작한다.  
따라서 모든 C++프로그램은 반드시 하나의 main() 함수를 가지고 있어야 한다.  
만약 main() 함수를 발견하지 못하면 C++컴파일러는 오류를 발생시킨다.    
  <br/>
### 명령문(statement)
C++프로그램의 동작을 명시하고, 이러한 동작을 컴퓨터에 알려주는 것에 사용되는 문장을 명령문이라고 한다.  
이러한 C++의 모든 명령문은 반드시 세미콜론(;)으로 끝나야한다.      
  <br/>
### 반환문(return)
반환문은 함수의 종류를 의미하며, 함수를 호출한 곳으로 결과값을 반환하는 역할을 한다.  
특히 main()함수가 반환되면, 프로그램 전체가 종료된다.    
  <br/>
### 선행처리문(preprocess)문
#include문과 #define문은 모두 선행처리기에 의해 처리되는 선행 처리문이다.  
  
#include문은 외부에 선언된 함수나 상수 등을 사용하기 위해서 헤더 파일의 내용을 현재 파일에 포함할 때 사용한다.  
C언어에서는 헤더파일에.h 확장자를 사용했지만, C++에서는 헤더파일의 확장자를 사용하지 않기로 한다.  
따라서, 기존 C언어 헤더파일의 이름 앞에 C를 추가하여 C++스타일의 헤더 파일로 변환하기도 한다.  
  
#define문은 함수나 상수를  단순화해주는 매크로를 정의할 때 사용한다.    
  <br/>
### 네임스페이스(namespace)
네임스페이스란 이름이 기억되는 영역을 뜻하며, 이름이 소속된 공간을 의미한다.  
네임스페이스는 C++프로그램을 작성할 때 발생하는 이름에 대한 충돌을 방지해 주는 방법을 제공한다.  
이러한 네임페이스는 C언어에는 없는 C++만의 새로운 기능이다.  
  
C++프로그램의 표준 구성 요소인 클래스, 함수, 변수 등은 std라는 이름 공간에 저장되어 있다.  
위의 예제 처럼 std라는 네임스페이스에 있는 정의를 사용하려면,  
std::접두어를 붙여 해당 정의가 std라는 네임스페이스에 있다는 것을 컴파일러에게 알려줘야 한다.  
  
이러한 네임스페이스에 속한 정의를 간단하게 사용하려면 다음의 명령문을 추가하면 된다.
{% highlight cpp %}
#include <iostream>
#define TEXT "Welcome to C++ Programming!!"
using namespace std;

int main()
{
	cout << TEXT;
	return 0;
}
{% endhighlight %}     
 <br/>
 <br/>
 <br/>
<참고자료><br/>
[코딩의 시작, TCP School](http://tcpschool.com/cpp/cpp_intro_program)
