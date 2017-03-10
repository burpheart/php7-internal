# PHP语法实现
写在前面：

这一章是根据PHP语法的实现详细解析Zend内核的处理过程，即各个opcode的handler处理，比如变量的赋值、函数的调用……有些内容前会跟之前部分章节内容重复，这里将再从具体的操作总结性的分析下，相比《第3章 Zend虚拟机》的内容，这一章分析的内容更加具体，虽然可能没有太大意义，但可以帮助我们更好的了解PHP的实现。

本章内容主要涉及zend_vm_def.h、zend_vm_execute.h，其中zend_vm_execute.h是根据zend_vm_def.h的定义通过zend_vm_gen.php脚本生成的，所以开发者实际编写opcode的handler是在zend_vm_def.h中，但是为了更加直观的分析各handler的处理，我们将重点分析生成的zend_vm_execute.h，同时只分析常见的用法，也不会把所有情况统统分析一遍。

目录：

## 1.变量
### 1.1 变量的定义、赋值
### 1.2 变量类型转换

## 2.运算符
### 2.1 算数运算
### 2.2 赋值运算
### 2.3 比较运算
### 2.4 逻辑运算
### 2.5 位运算

## 3.选择结构
### 3.1 if条件语句
### 3.2 switch条件语句

## 4.循环结构
### 4.1 for循环
### 4.2 while循环
### 4.3 foreach循环

## 5.跳转语句

## 6.函数
### 6.1 函数定义
### 6.2 函数调用
### 6.3 函数返回值

## 7.文件加载

## 8.面向对象

