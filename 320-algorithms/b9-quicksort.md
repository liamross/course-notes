# QuickSort and QuickSelect 23/10/2017

```javascript
/**
 * Sort an array using QuickSort.
 * @param {number[]} A - Array of elements to sort.
 */
function QuickSort(A) {
  if(A.length > 1) {
    const pivot = A[1] // or choose random

    const Lesser = allElementsLess(A, pivot)
    const Greater = allElementsGreater(A, pivot)

    const LesserSorted = QuickSort(Lesser)
    const GreaterSorted = QuickSort(Greater)

    return [
      ...LesserSorted,
      ...GreaterSorted,
    ]
  } else {
    return A
  }
}
```

```javascript
/**
 * Select the kth largest element of an Array. Precondition: |A| >= k.
 * @param {number[]} A - Array of elements to sort.
 * @param {number} k - The kth number to use in QuickSelect.
 */
function QuickSelect(A, k) {
  const pivot = A[1] // or choose random

  const Lesser = allElementsLess(A, pivot)
  const Greater = allElementsGreater(A, pivot)

  if (Greater.length = k - 1) {
    return pivot
  }
  else if (Greater.length > k - 1) {
    // All larger elts are in Greater; k is unchanged.
    return QuickSelect(Greater, k)
  }
  else {
    // Subtract from k the # of larger elts removed (Greater and the pivot).
    return QuickSelect(Lesser, k - Greater.length - 1)
  }
}
```

Runtime:

T(n) = T(3/4 * n) + O(n)

T(n) = T(cn) + O(n), c < 1 &rArr; T(n) = O(n)

* explains why any fixed fraction is good for us

* **c can go arbitrarily close to 1, and it will help us**

## Working through a real code example

[See example here.](https://www.ugrad.cs.ubc.ca/~cs320/misc/Deterministic-Select-in-O-of-n-blank.html)

1. bind c so that it is less than 1

1. divide into rows (5 x 10 perhaps)

1. sort each row based, then sort the columns based on middle value  
**1** **2** **3** 4 5  
**2** **4** **6** 8 10  
**3** **6** **9** 12 15  
4 8 12 16 20  
5 10 15 20 25  

1. recursively call the function we are writing, find median of each row without
having to mergesort it (nlog(n))

```python
def deterministic_select(A, i):
    """
    Given a list of numbers A and a number 1 <= i <= len(A), return the i'th
    largest element of A.
    """
    # Base Case: When we have fewer than five elements, just find the i'th largest directly.
    if len(A) < 5:
        # TODO
        return 0

    # Note: Python's documentation stipulates that a slice like a[i:j] where
    # j > len(a) behaves as if j were len(a).
    # That's handy for us here.

    # Divide into blocks of five and sort the blocks in preparation for finding
    # their medians. Does sorting here take n lg n time? NO. We sort a bunch of
    # blocks EACH OF LENGTH 5. It takes constant time to sort 5 numbers! So,
    # overall, this operation takes linear time.
    blocks = []
    for b in range((len(A) - 1) //5 +1): # same as finding the ceiling.
      blocks.append(sorted(A[b*5:(b+1)*5]))
    print (blocks)

    # Find the median of the medians
    medians = [b1[len(b1)//2] for b1 in blocks]
    print (medians)
    # (use recursive call to find medians)
    median_of_medians = deterministic_select(medians, len(medians)//2 +1)

    # Partition out the smaller/larger elements.
    lesser = [] # TODO: all elements less than the mom (median_of_medians)
    greater = [] # TODO: all elements greater than the mom
    moms = [] # TODO: all elements equal to the mom; yes, there could be many

    # Depending on the sizes of lesser, moms (median of medians),
    # greater, figure out whether we are:
    #  1) Done (when the ith largest element is in moms)
    #  2) Recursing to the left (from our perspective, into greater)
    #  3) Recursing to the right (from our perspective, into lesser)
    # Note that this is no different from quickselect. Indeed, deterministic and
    # quick select only differ on how they pick the pivot.

    # TODO: finish!
    return 0
```