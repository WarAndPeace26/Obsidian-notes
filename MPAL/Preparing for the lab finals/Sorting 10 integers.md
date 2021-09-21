# Sorting
***
```Assembly 
org 100h
.DATA
	input db 10 dup(0)
	prompt db 10,13, 'Enter the numbers please: $'
	answer db 10,13, 'The numbers in sorted order: $'
	
.CODE
	MAIN PROC
		mov ax, @DATA
		mov ds, ax
		xor ax, ax
		
		mov ah, 09h
		lea dx, prompt
		int 21h
		
		mov ah, 01h
		mov cx, 10
		mov si, OFFSET input
		
		inploop:
			int 21h
			mov [si], al
			inc si
		Loop inpLoop
		
		Call Sort
		
		mov ah, 09h
		lea dx, answer
		int 21h
		
		mov cx, 10
		mov si, OFFSET input
		mov ah, 02h
		
		outloop:
			mov dx, [si]
			int 21h
			inc si
		Loop outLoop
		
		mov ah, 4ch
		mov ah, 00h
		int 21h
	MAIN ENDP
	
	Sort PROC
		mov cx, 10
		dec cx
		
		outerloop:
			mov bx, cx
			mov si,0
			
			compLoop:
				mov al, input[si]
				mov dl, input[si+1]
				cmp al,dl
				
				jc noSwap
				
				mov input[si], dl
				mov input[si+1], al
				
				noSwap:
					inc si
					dec bx
				jnz comploop
		Loop outerLoop
		ret
	Sort ENDP
```
