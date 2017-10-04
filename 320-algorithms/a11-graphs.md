# Graphs 27/09/2017

## Definitions

**Component** - the entire body of the connected graph.  
*There can be multiple components, if there are multiple disconnected node groups.*

**Edges** - connecting paths between nodes.  
*There are always `n-1` edges if `n` is number of nodes*

**Articulation Point** - vertex whose removal would increase the number of
connected components in the graph.  
*If you destroyed that vertex (node, etc) then the graph would break into multiple graphs.*

**Diameter** - the largest possible value of the smallest number of edges between two nodes.  
*Of all the shortest paths between two nodes, the diameter is the longest. If there are 5 nodes, diameter is 4.*

> By convention: the path between two disconnected verteces is considered infinitely long.

## Design an algorithm to determine diameter

Design an algorithm to find the **diameter** of an unweighted, undirected, **connected** graph.
For short, we'll call this problem DIAM.

### Find trivial instances of DIAM

1. An empty graph

1. A single node within the component

1. A complete graph of any size k

### Find small instances of DIAM

1. Any number of nodes in an acyclic connected path

### Represent the problem

G(V, E)  
V: set of vertices {v<sub>1</sub>, ... , v<sub>n</sub>}  
E: set of pairs {(u, v): where u &isin; V, v &isin; V}

Is it connected?

Is it directed? if so then (u, v) &ne; (v, u)

