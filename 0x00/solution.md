# 0x00

````assembly
xor      eax,eax ; eax = eax ^ eax = 0
lea      rbx,[0] ; rbx = 0
loop     $ ; jmp to same instruction until RCX = 0 -> At the end RCX = 0
mov      rdx,0 ; rdx = 0
and      esi,0 ; esi = esi and 0 = 0
sub      edi,edi ; edi = edi - edi = 0
push     0 
pop      rbp ; rbx = top element of the stack = 0
````

This code zeroes the registers in there.
