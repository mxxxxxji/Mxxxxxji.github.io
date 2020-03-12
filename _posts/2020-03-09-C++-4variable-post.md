---
layout: post
title: "[C++] 변수"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [C++]
categories: [C++]
---

------------------------------------------------------------------------------------------------------------
## 변수(variable)
변수(variable)란 데이터(dat)를 저장하기 위해 프로그램에 의해 이름을 할당바든 메모리 공간을 의미한다.<br/>
즉, 변수란 데이터(data)를 저장할 수 있는 메모리 공간을 의미하며, 이렇게 저장된 값은 변경될 수 있습니다.<br/><br/>
C++에서 숫자 표현에 관련된 변수는 정수형 변수와 실수형 변수로 구분할 수 있다.<br/>
정수형 변수 : char, int, long, longlong<br/>
실수형 변수 : float, double<br/>
관련된 데이터를 한 번에 묶어서 처리하는 사용자 정의 구조체 변수도 있다.<br/>
<br/>
<br/>  
## 변수의 이름 생성 규칙
변수의 이름은 해당 변수에 저장될 데이터의 의미를 잘 나타내도록 짓는 것이 좋다.<br/>
다음은 변수의 이름을 생성할 때 반드시 지켜야할 규칙이다.<br/>
1. 변수의 이름은 영문자(대소문자), 숫자, 언더스코어(\_)로만 구성된다.<br/>
2. 변수의 이름은 숫자로 시작될 수 없다.<br/>
3. 변수의 이름 사이에는 공백을 포함할 수 없다.<br/>
4. 변수의 이름으로 C++에서 미리 정의된 키워드는 사용할 수 없다.<br/>
5. 변수 이름의 길이에는 제한이 없다.
<br/>
<br/>  

## 변수의 선언
C++에서는 변수를 사용하기 전에 반드시 먼저 해당 변수를 저장하기 위한 메모리 공간을 할당받아야 한다.<br/>
이렇게 해당 변수만을 위한 메모리 공간을 할당받는 행위를 변수의 선언이라고 부른다.<br/>
#### 변수의 선언만 하는 방법
{% highlight cpp %}
int num;
num = 20;
{% endhighlight %}
#### 변수의 선언과 동시에 초기화하는 방법
{% highlight cpp %}
int num1, num2;
double num3 = 1.23, num4 = 4.56;
{% endhighlight %}
<br/>
<br/>
<br/>
<참고자료><br/>
[코딩의 시작, TCP School](http://tcpschool.com/cpp/cpp_intro_program)
