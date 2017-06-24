---
layout: post
date: 2016-07-16 12:00:00 +0530
image:
  feature: accpp.jpg
  thumb: acpng.jpg
title: Building a C++ Application to cheat the readings
info: Breakneck speed programming and the law breaker.
tags: [cpp, physics, programming, git, GitHub]
categories: cpp
---

### Program files
There are actually two files in this Set. The first of these programs is 'find.cpp'. find was built as a program to calculate the length of A.C. Sonometer wire which gives the correct reading, which we are looking for.
#### Header files
```
#include &#60;iostream&#62;
#include &#60;math.h&#62;

using namespace std;

float calc(float t,float u,float l){
return sqrt(t)/(2*l*sqrt(u));
}
float ten(float x){
return x*0.0098;
}
float com(float x1, float x2){
return(x1+x2)/200;
}
int main()
{
int w;
float n,t,u,l1,l2,l;
cout<<"Calculate Frequency of AC from lengths on Sonometer!!\n";
cout<<"What are the lengths?(cm)\nl.1:";
cin>>l1;
cout<<"l.2:";
cin>>l2;
l=com(l1,l2);
cout<<"Mean length = "<< l <<" What is the value of weights(g)? ";
cin>>w;
t= ten(w);
cout<<"Tension = "<< t;
cout<<" Kgm/s\nWhat is the value of linear density of wire U(g/m)?\n";
cin>>u;
n=calc(t,u,l);
cout<<"\nTherefore frequency of AC is "<< n <<" Hz\n";
return 0;
}
```
_Download source code from:_
[![GitHub](github.svg)](https://github.com/Devdutt-Shenoi/Devcpp/blob/master/WhatHz.cpp)
