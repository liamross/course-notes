# Clustering 04/10/2017

You get a bunch of photos, and categories to group them into, and a similarity
measure for each pair of photos (a complete graph)

## Trivial and Small Instances

### Trivial

1. No photos
1. One Photo, one category  
|P| = k (set of photos has cardinality k)  
C = 1 (one category)
1. One category for each photo (one photo per category)  
P = C

### Small Instances

1. Three photos  
|P| = 3  
w<sub>1</sub> = [P<sub>1</sub>, P<sub>2</sub>] = 1  
w<sub>2</sub> = [P<sub>1</sub>, P<sub>3</sub>] = 1  
w<sub>3</sub> = [P<sub>2</sub>, P<sub>3</sub>] = 1  

### Reasonable Graph for Set of Pictures

![b1_weights](images/b1_weights.png)

However, this is not based on the parameters of the problem, which outline the
number of categories required.

&forall; e in E, e = (u, V, w) where w is the simmilarity of u + v,
S(u, v) -> w 0 <= w <= 1.

V = {p<sub>1</sub>, ..., p<sub>n</sub>}, n is # of photos.

C = k.
