# Growth of functions

```javascript
var max = null;
for (var a in A) { // n times --> O(n)
  if (max < a)
    max = a;
}
```

```javascript
var first = A[1];
var last = A[n];
var middle = a[floor(n/2)];

if (first <= middle && middle <= last) { // constant time --> O(1)
  return middle;
} else (someting) {
  return first
}
```

```javascript
// loop inside for loop, O(n^2)
```

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