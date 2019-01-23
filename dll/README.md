
### gcc编译动态链接库

以下是windows环境下用gcc编译动态链接库的尝试过程。

### 环境准备

编译使用的MinGW，64位的官网可以找到下载地址。

### 项目建立及代码编写
在任意地方新建一个目录，保存这个项目，然后新建一个c源程序文件main.c，输入程序。

### 编译

```shell
[root@zhangyz ~]# gcc -shared -Wall -o main.dll main.c
```

