---
layout: post
title: strcasestr函数
tags: 计算机基础
---


    #define _GNU_SOURCE
    #include <string.h>

    char *strcasestr(const char *haystack, const char *needle);


`strcasestr`函数用于在字符串`haystack`中查找字符串`needle`，忽略大小写。如果找到则返回`needle`字符串在`haystack`字符串中第一次出现的位置的char指针。

在使用中不加上`#define _GNU_SOURCE`，编译时会出现`warning: assignment makes pointer from integer without a cast`。

这是因为函数的声明在调用之后。未经声明的函数默认返回int型。
 
因此要在所有头文件之前加`#define _GNU_SOURCE`，以此解决此问题。