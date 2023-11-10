> In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this?
>

```
Decrypt my super sick RSA:
c: 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n: 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e: 65537
```

```
#solution
from sympy.ntheory import factorint

c = 861270243527190895777142537838333832920579264010533029282104230006461420086153423
n = 1311097532562595991877980619849724606784164430105441327897358800116889057763413423
e = 65537

p = 1955175890537890492055221842734816092141
q = 670577792467509699665091201633524389157003 
d = pow(e, -1, (p-1)*(q-1))

print(bytearray.fromhex(format(pow(c, d, n), "x")))
```

`bytearray(b'picoCTF{sma11_N_n0_g0od_13686679}')`