# Strings
```Assemply
org 100h

.DATA
	astring db "Hello World$"
.CODE
	mov ax, @DATA
	mov ds, ax
	xor ax, ax
	
	mov ah, 09h ;for printing
	mov dx, OFFSET astring
	
	int 21h
	ret
```