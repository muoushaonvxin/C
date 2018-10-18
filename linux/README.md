    编译步骤:
        gcc -E b.c -o b.i
        gcc -S b.i -o b.s
        gcc -c b.s -o b.o
        gcc b.o  -o b
        ./b                # 执行程序
        
        
    也可以直接:
        gcc b.c -o b
        
