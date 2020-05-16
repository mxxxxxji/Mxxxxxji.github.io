
---
layout: post
title: "[Algorithm] Recursion"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [Algorithm]
categories: [Algorithm]
---

------------------------------------------------------------------------------------------------------------

## Recusion의 개념
순환 또는 재귀함수라고 부른다.  
메소드를 정의할 때 자기 자신을 재참조 하는 방법을 말한다.  
<br/>
<br/>

## Recursion의 기본예제
#### 무한루프가 발생하는 경우
다음의 코드는 func()이라는 메소드를 아무런 조건 없이 다시 호출하여 무한루프에 빠지게 된다.
{% highlight cpp %}
public class RecursionTest1 {
	public static void main(String[] args){
		func();
	}
	public static void func(){
		System.out.println("Hello");
		func();
	}
}
{% endhighlight %}

#### 조건을 추가해 준 경우
Recursion이 항상 무한루프에 빠지는 것은 아니다.
{% highlight cpp %}
public class RecursionTest1 {
	public static void main(String[] args){
		int  n=4;
		func(n);
	}
	public static void func(int k){
		if(k<=0){
			return; //base case
		}else{
			System.out.println("Hello");
			func(k-1);	//recursive case
		}
	}
}
{% endhighlight %}

    {% raw %}
    Hello
    Hello
    Hello
    Hello
    {% endraw %} 

#### 무한루프에 빠지지 않는 조건
1. **Base Case** : 적어도 하나의 recursion에 빠지지 않는 경우가 존재해야 한다.
2. Recursive Case : recursion을 반복하다 보면 결국 Base Case로 수렴해 한다.

#### Recursion의 해석 - 1 ~ n 까지의 합
{% highlight cpp %}
public class RecursionTest2 {
	public static void main(String[] args){
		int result = func(4);
		System.out.println(result);
	}
	public static int func(int n){
		if(n==0){
			return 0;
		}else{
			return n+func(n-1);
		
		}
		
	}
}
{% endhighlight %}

    {% raw %}
    10
    {% endraw %} 

#### Recursion을 이용하여 Factorial : n!구하기
{% highlight cpp %}
public class RecursionTest3 {
	public static void main(String[] args){
		int result = func(4);
		System.out.println(result);	
	}
	public static int func(int n){
		if(n==0){
			return 1;
		}else{
			return n*func(n-1);
		}
	}
}
{% endhighlight %}
    
    {% raw %}
    24
    {% endraw %} 

#### Recusion을 이용하여 n번째 Fibonacci 구하기
{% highlight cpp %}
public class RecusionTest4 {
	public static void main(String[] args){
		int result = func(6);
		System.out.println(result);
	}
	public static int func(int n){
		if(n<2)
			return n;
		else{
			return func(n-1)+func(n-2);
			
		}
	}
}
{% endhighlight %}
    {% raw %}  
    8
    {% endraw %} 

<br/>
<br/>
<br/>
**참고자료**<br/>
[Recursion의 개념과 기본 예제들](excelsior-cjh.tistory.com/28)
