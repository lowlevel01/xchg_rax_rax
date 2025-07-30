# 0x02 : https://www.xorpd.net/pages/xchg_rax/snip_02.html

````assembly

neg      rax
sbb      rax,rax
neg      rax

````

neg rax <=> rax = 0 - rax. Unless rax is 0. This represents a borrow so Carry Flag is set ( https://stackoverflow.com/questions/52998644/why-does-the-neg-instruction-interfere-with-the-carry-flag )

sbb rax, rax <=> rax = rax - rax - CF = - CF

remember, initial rax = 0 => CF = 0 otherwise CF = 1. So at this point, RAX = 0 or -1

last neg is to make the values positive.

So, this routine checks whether rax is Zero or not.

