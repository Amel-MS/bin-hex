name "hex-bin"

org 100h

; load binary value:
; (hex: 5h)
mov al, 00000101b

; load hex value:
mov bl, 0ah

; load octal value:
; (hex: 8h)
mov cl, 10o

; 5 + 10 = 15 (0fh)
add al, bl     
mov bl,al

; 15 - 8 = 7
sub al, cl




; print result 
mov dl,bl
mov ah,02
int 21h

mov dl, al
mov ah,02
int 21h


; wait for any key press:
mov ah, 0
int 16h

ret




