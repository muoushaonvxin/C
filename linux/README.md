编写相关代码示例

```c
#include <stdio.h>

int main()
{
   printf("hello world!\n");
   return 0;
}
```

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

<br/>

### GCC编译选项

| 编译选项 | 说明 |
|---------|------|
| -E      | 只进行预处理，不做编译，汇编和链接 |
| -S      | 只进行编译，不做汇编和链接 |
| -c      | 只进行汇编，不做链接 |
| -o file | 指定输出文件的名称 |
| -v      | 打印编译器内部编译各个过程的命令行信息和编译器版本信息 |
| -X language | 指定输入文件的语言，编译器可根据后缀判断出源文件的语言 |
| -O      | 会在编译，链接过程中进行优化处理，这样产生的可执行文件的执行效率可以提高 |

<br/>

### GCC警告出错选项

| 选项 | 说明 |
|---------|------|
| -fsyntax-only | 检查程序中的语法错误，但不产生输出信息 |
| -w            | 禁止所有警告信息 |
| -Wunused      | 使用未声明的变量，静态函数或某条语句的运算结果没有使用，则发出警告 |
| -Wmain        | 如果把main函数声明或定义成非标准的类型，编译器就发出警告 |
| -Werror       | 视警告为错误，并放弃对其继续编译 |
| -Wredundant-decls | 在同一可见区域定义多次声明，编译器就给予警告 |
| -Wall         | 允许gcc提供所有的警告信息 |
| -pedantic-error | 允许发出ANSIC标准所列出的全部信息 |

<br/>

### GCC当中其它的编译选项


| 选项 | 说明 |
|---------|------|
| -I      | 指定头文件所在的目录 |
| -L      | 指定库文件所在的目录 |
| -l      | 指定编译时需要用的库名称 |
| -D      | 预先定义一个名为name的宏，如 -DNAME=VAL |
| -g      | 生成为gdb所用的调试信息 |
| -static | 只使用静态库，禁止动态库的链接 |
| -ansi   | 支持符合ANSI标准的c程序，关闭GNUC中不兼容ANSIC的特性 |
| -std    | 指定语言使用的标准，如 -std=c99 |

