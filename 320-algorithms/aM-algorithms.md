# Algorithms

## Gale-Shapley

1. Man 1 engages to first Woman on his preference list

1. Man 2 engages to first Woman on his preference list

1. If the Woman Man 2 engages to is married, it either marries Man 2 (if it prefers man 2 to its current match)  
or keeps its current match and Man 2 proposes to the next Woman in his preference list.

1. Process is repeated, moving down men's preference list, until no man is left unmatched

```text
initialize all men in M and all women in W to unengage
while (an unengaged man with at least one woman on his preferance list remains)
  do choose such a man m (element of) M
    propose to the next woman w(element of)W on his preference list
      if( w is unengaged)
        then engage m to w
      else if w prefers m to fiance m'
        then break engagement of m' to w
          engage m to w
      cross w off m's preferance list
report set of engaged pairs as final matching.
```

