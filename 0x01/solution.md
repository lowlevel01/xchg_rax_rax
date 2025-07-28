````assembly

.loop:
    xadd     rax,rdx
    loop     .loop ; loop is run RCX times

````

``xadd rax, rdx`` has effect : `rdx = rax` and `rax = rax + rdx` and it is run RCX times

After 1 iteration:
  `rdx = rax` and `rax = rax + rdx`
  
After 2 iterations:
  `rdx = rax+rdx` and `rax = (rax + rdx)+rax = 2*rax + rdx`

After 3 iterations:
  `rdx = 2*rax+rdx` and `rax = 3*rax + 2*rdx`

....

these two registers seems to follow this pattern

rax[i] = rax[i-1] + rdx[i-1] (i.e. sum of old ones)

rdx[i] = rax[i-1] (i.e. rdx becomes old rax each time)

-> rax[i] = rax[i-1] + rax[i-2] Similar to Fibonacci sequence, difference in initial conditions.
