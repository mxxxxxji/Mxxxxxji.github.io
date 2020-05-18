---
layout: post
title: "[Algorithm] Recursion_2"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [Algorithm]
categories: [Algorithm]
---

------------------------------------------------------------------------------------------------------------

## 문자열의 길이계산
1. Base Case : 문자열 값이 null인 경우 -> retun 0;
2. Recursive Case : 첫번째 문자를 제외한 길이+1을 return 한다.

{% highlight cpp %}
public class RecursionTest6 {
	public static void main(String[] args){
		System.out.println(length("test"));
	}
	public static int length(String str){
		if(str.equals("")){
			return 0;
		}else
			return 1+length(str.substring(1)); //substring : 문자열자르는함수		
	}
}
{% endhighlight %}

    {% raw %}  
    4
    {% endraw %} 
<br/>
<br/>

## 문자열을 뒤집어 프린트

{% highlight cpp %}
public class RecursionTest7 {

	public static void main(String[] args) {
		printCharReverse("test");
	}
	public static void printCharReverse(String str){
		if(str.length()==0)
			return;
		else{
			printCharReverse(str.substring(1));
			System.out.print(str.charAt(0));
		}
	}
}
{% endhighlight %}
    
    {% raw %} 
    tset
    {% endraw %} 
<br/>
<br/>

## 2진수로 변환하여 출력

{% highlight cpp %}
public class RecursionTest8 {
	public static void main(String[] args){
		printInBinary(9);
	}
	public static void printInBinary(int n){
		if(n<2)
			System.out.print(n);
		else{
			printInBinary(n/2); //n을 2로 나눈 몫을 먼저 2진수로 반환하여 인쇄한 후
			System.out.print(n%2); //n을 2로 나눈 나머지를 인쇄한다.
		}
	}	
}
{% endhighlight %}

    {% raw %}  
    1001
    {% endraw %} 

<br/>
<br/>

## 최대값 찾기
{% highlight cpp %}
public class RecursionTest9 {
	public static void main(String args[]){
		int[] data = {1,2,5,6,2,8,9};
		System.out.println(findMax(data,0,6));
	}
	public static int findMax(int[] data, int begin, int end){
		if(begin==end)
			return data[begin];
		else{
			return Math.max(data[begin],findMax(data, begin+1, end));
		}
	}
}
{% endhighlight %}
    {% raw %}
    9
    {% endraw %}
<br/>
<br/>

## 순환함수(Recursion)와 반복문(iteration)
- 모든 순환함수는 반복문으로 변경가능하다.
- 그 역도 성립한다. 즉 모든 반복문은 순환함수로 표현 가능하다.
- 순환함수는 복잡한 알고리즘을 단순하고 알기쉽게 표현하는 것을 가능하게 한다.
- 하지만 함수 호출에 따른 오버헤드가 있다.(매개변수 전달, 액티베이션 프레임 생성 등)

<br/>
<br/>
<br/>
**참고자료**<br/>
[Recursion의 개념과 기본 예제들](https://excelsior-cjh.tistory.com/category/Algorithms?page=2)

