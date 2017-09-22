# Reductions and Resident Matching

## Quantities

```text
R={r0, ... , rn}
H={h0, ... , hm}

n >= m (less or equal hospitals than residents)

each hospital has "slots"

S:H={s0, ... , sm} where S(index of h) returns #Slots
```

## Solution

```text
solution is a set of pairs
S={(ri, hj): ri E R, hj E H}
f:r->h f(r)=h if (r,h) E S
g:h->r g(h)=r if (h,r) E S
```