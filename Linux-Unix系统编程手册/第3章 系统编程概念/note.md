# 第三章 系统编程手册

主要介绍一些基本概念
## 基本概念

### 系统调用

文件io调用  open read write close
文件描述符 是一个数字 进程级别的
文件句柄 系统级别的 一个文件句柄可能被多个进程中的文件描述符引用；句柄和i-node可能不是一对一的情况
i-node 文件在内存中和磁盘上的数据结构 会有差别

库函数


错误处理

系统调用失败时，会将全局整形变量 errno 设置为一个正值，以标识具体的错误。 
设置errno这个标识是线程安全的，类似java的threadlocal  
需要引入头文件 <errno.h>


