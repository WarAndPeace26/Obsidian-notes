# New Line and Spaces
***
```Assembly
.DATA
	SPACE DB ' $'	
	NEWLINE DB 10,13,'$'
.CODE
	MAIN PROC
		LEA dx, NEWLINE		;Load Effective Address
		mov ah, 09h				;09h is print
		int 21h

		LEA dx, SPACE
		mov ah, 09h
		int 21h
	MAIN ENDP
END MAIN
```