# Even or Odd
```Assembly
org 100h

.Data
	o DB "odd $"
	e DB "even $"
	NEWLINE DB 10,13,'$'
	SPACE DB ' $'
.Code
	MAIN PROC
		mov ax, @DATA
		mov ds, ax
		
		mov ah,	1		;Input
		int 21h				;execute whatever's in ah

		mov bl, 2
		div bl				;divide contents of al by bl (because we're using bl, it'll only divide the contents of al)

		cmp ah, 1 ;the remainder is stored in the ah
		mov ah, 09h			;print
		jne EVEN

		

		lea dx, o
		int 21h;
		jmp EXT

		EVEN:
			lea dx, e
			int 21h;

		EXT: ret
	MAIN ENDP
```