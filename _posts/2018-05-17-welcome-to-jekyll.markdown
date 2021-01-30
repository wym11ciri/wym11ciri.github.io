---
layout: post
title:  "C++引用"
date:   2021-1-22 14:05:21 +0800
tags: c++
color: rgb(255,90,90)
cover: '../assets/test.png'
subtitle: 'C++引用'
---
<pre name="code" class="c++"> 
void fun1(int &x){

x++;

}
void fun2(int x){

x++;

}
int mian(){

int abc = 100 , xyz = 13;

fun1(xyz); //13+1 = 14

abc = xyz;//abc = 14

fun2(abc); //这里实际上没加

printf(“%d\n”,abc);

}
</pre>
这里的结果是14

指针：指针是一个变量，只不过这个变量存储的是一个地址，指向内存的一个存储单元；
而引用跟原来的变量实质上是同一个东西，只不过是原变量的一个别名而已
