---
layout: post
title: "[Algorithm] Recursion_3"
description: "Demo post displaying the various ways of highlighting code in Markdown."
tags: [Algorithm]
categories: [Algorithm]
---

------------------------------------------------------------------------------------------------------------

## 순환 알고리즘의 설계(Designing Recursion)
- 적어도 하나의 base case, 즉 순환되지 않고 종료되는 case가 있어야한다.
- 모든 case는 결국 base case로 수렴해야한다.
<br/>
<br/>

## Recursion의 응용 미로찾기
![image](https://user-images.githubusercontent.com/52437364/82180610-d8483900-991b-11ea-8d5c-eef8e2ef2209.png)

{% highlight cpp %}
public class RecursionTest10 {
	private static int N=8;
	private static int[][] maze ={
			{0,0,0,0,0,0,0,1},
			{0,1,1,0,1,1,0,1},
			{0,0,0,1,0,0,0,1},
			{0,1,0,0,1,1,0,0},
			{0,1,1,1,0,0,1,1},
			{0,1,0,0,0,1,0,1},
			{0,0,0,1,0,0,0,1},
			{0,1,1,1,0,1,0,0}
	};
	
	private static final int PATHWAY_COLOR = 0;
	private static final int WALL_COLOR = 1;
	private static final int BLOCKED_COLOR =2;
	private static final int PATH_COLOR=3;
	
	public static boolean findMazePath(int x, int y){
		if(x<0 || y<0 || x>=N || y>=N){
			return false;
		}else if(maze[x][y] != PATHWAY_COLOR){
			return false;
		}else if(x==N-1 && y==N-1){
			maze[x][y] = PATH_COLOR;
			return true;
		}else{
			maze[x][y] = PATH_COLOR;
			if(findMazePath(x-1,y)||findMazePath(x, y+1)||
					findMazePath(x+1, y)||findMazePath(x, y-1)){
				return true;
			}
			maze[x][y] = BLOCKED_COLOR;
			return false;
		}
	}
	
	public static void main(String[] args){
		findMazePath(0, 0);
		for(int i=0; i<N; i++){
			for(int j=0; j<N; j++){
				System.out.print(maze[i][j]);
			}
			System.out.println();
		}
	}
}
{% endhighlight %}

    {% raw %}
    32222221
    31121121
    32212221
    31221122
    31112211
    31333121
    33313331
    01110133
    {% endraw %} 


<br/>
<br/>
<br/>
**참고자료**<br/>
[Recursion의 개념과 기본 예제들](https://excelsior-cjh.tistory.com/category/Algorithms?page=2)

