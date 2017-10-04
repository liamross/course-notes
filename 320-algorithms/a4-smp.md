# Stable Marriage Problem Worksheet 11/09/2017

## Trivial and Small Instances

1. Write down all the __trivial__ instances of SMP. We think of an instance as
  "trivial" if...

## Represent the Problem

1. What are the quantities tha matter in this problem? Give them in short
  usable names.

```text
M={m1, ...mn} W={w1, ...wn} n:# in set
p[mi]: permutation(W) representing list of preferences
p[wj]: permutations(M) representing list of preferences

We want to tell if:
wi > wj if wi is preferred to wj
mi > mj if mi is preferred to mj

space required: 2n^2 (p[mi] for each and p[wj] for each)
```

## Representing the Solution

### What are the quanities that matter in the solution to the problem

> Give them short, usable names

```text
solution is a set of pairs
S={(mi, wj): mi E m, wj E W}
f:m->w f(m)=w if (m,w) E S
g:w->m g(w)=m if (w,m) E S
```

### Describe using these quantities makes a solution __valid__ and __good__

- Valid solution is a _bijection:_ f=g^(-1) (or g=f(-1))
  - Pairs are mapped to each-other
  - This is not necessarily a _good_ solution though...

- Good solution is one that we say is _stable_
  - There is no pair with incentive to switch with other pair

### Go back to trivial, write out one or more solutions using these names

```text
S1 = {(m, w)} S2={(m1, w2), (m2, w1)}
```

## Similar Problems

1. Bipartite Matching

## Brute Force Solutions

```text
m: (m1, ...mn) -> each of these match to a w
    |
    V
    wj         : permutations of w
```

this is the number of "valid solutions" but we need a way to judge if valid
  solution is a good one
