# Growth Continued 27/09/2017

```javascript
function FindNeighboringInversion(A) { // Double loop, detects if not sorted.
  returns -1; // if not sorted
};

let i = FindNeighboringInversion(A);

while (i >= 0) {
  Swap(A[i], A[i+1]);
  i = FindNeighboringInversion(A);
}
```

An inversion exists when `i < j but A[i] > A[j]`

> Prove that if any inversion exists, a neighboring inversion exists...

If there exists a neighboring inversion, there exists an inversion...

&exist; x NI(x) -> &exist; x I(x)

&exist;asy stuff, but... if there exists an inversion there exists a neighboring
inversion???

&exist; x I(x) -> &exist; x NI(x) is this true? Let's assume it is not true and try to prove.

We will try to prove the inverse to disprove this.

We assume: that there can be an inversion without having a neighboring inversion

`A[i] < = A[i + 1] <= A[i + 2] <= A[i + 3] <= ... <= A[j]`

or by **transitivity**...

`A[i] <= A[j]`

huh.

This contradicts the fact that there was ever an inversion in the first place

Therefore: if there is an inversion, there must be a neighboring inversion

> Give upper and lower bounds

The termination condition of the function is when there are no NI...

&forall; x ~ NI(x)

n(n+1/2) aka n choose 2 aka O(n<sup>2</sup>)

the # of inversions <= (n choose 2) = n(n-1)/2 = O(n<sup>2</sup>)

`no inversions <=> array is sorted`

> Give a measure of progress through the array

The # of inversions remaining would be one measure of progress. We know the
total number of inversions is `n choose 2` -> reduces the number of inversions
since we are fixing one. The loop can only continue O(n<sup>2</sup>)

> Prove that the algorithm sorts A


&exist; x I(x) => &exist; x NI(x)

&equiv; ~&exist; x NI(x) => &exist; x I(x)

&equiv; &forall; x ~NI(x) => &forall; x ~I(x)

(algorithm assures)






