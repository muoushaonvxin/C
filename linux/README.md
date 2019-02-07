编译步骤:

```shell
[root@zhangyz ~]# gcc -E b.c -o b.i
[root@zhangyz ~]# gcc -S b.i -o b.s
[root@zhangyz ~]# gcc -c b.s -o b.o
[root@zhangyz ~]# gcc b.o -o b
./b                
```

也可以直接:
```shell
[root@zhangyz ~]# gcc b.c -o b
```

### GCC

GCC原名为GNU C语言编译器(GNU C Compiler)，因此它原本只能处理C语言。GCC很快地扩展，变得可处理C++。后来又扩展能够支持更多编程语言，如Fortran，Pascal，Object-C，Java，Ada，Go以及各类处理器架构上的汇编语言等，所以改名GNU编译器软件。

GNU是GNU's Not UNIX的缩写，意思是说，GUN并不是UNIX，1984年，开展GNU项目，这个项目的目的是创建一个自由，开放的UNIX操作系统，并成立了软件基金会，邀请更多工程师与志愿者来编写软件，如GCC和C函数库以及用来操作系统内核的基本接口bash shell。

