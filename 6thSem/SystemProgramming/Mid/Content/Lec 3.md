# Lec 3
| command                         | output               |     |     |
| ------------------------------- | -------------------- | --- | --- |
| gcc -Og -S mstore.c             | Assembly (.s)        |     |     |
| gcc -Og -c mstore.c             | Reloc. Obj file (.o) |     |     |
| gcc -O mstore mstore.c          | exe                  |     |     |
| objdump -d mstore.o             | disassembled .o file |     |     |
| gcc -Og -o prog main.c mstore.c |                      |     |     |


## Referencing Memory Location
![[Pasted image 20220211083039.png]]