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
