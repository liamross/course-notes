# TERMINOLOGY

`N = |V| = # of vertices`

`M = |E| = # of edges`

**Undirected simple graph**: m <= n(n-1)/2

**Tree**: An undirected graph is a tree if it is connected and does not contain a cycle; deleting any edge from a tree will disconnect it.

**Cycle**: a path that starts and end at the same vertex; a simple cycle repeats no other vertex (= if all vertices are distinct from one other)

**Simple Graph**: An unweighted, undirected graph containing no graph loops or multiple edges

**Undirected/ Directed**: A directed graph G’ consists of a set of nodes V and a set of directed edges E’.
Each e’ in E’ is an ordered pair (u, v);

in other words, the roles of u and v are not interchangeable, and we call u the tail of the edge and v the head

**Unweighted/Weighted
Connected (refers to undirected graphs)**: There exists a path between any pair of nodes, and there are no unreachable nodes

**Strongly Connected (refers to directed graphs)**: For every two nodes u and v, there is a path from u to v and a path from v to u

---

**Path**: A path of length k is a list of k+1 vertices with an edge b/w each consecutive pair of vertices; a simple path repeats no vertices.
In an undirected graph G = (V, E), a path is a sequence P of nodes V1, V2 ...Vk-1, Vk with the property

that each consecutive pair Vi, Vi+1 is joined by an edge in G.

**Simple Path**: A path with no repeating vertices, all nodes are distinct

**Articulation Point**: In an undirected graph, the articulation point is a vertex whose removal increases the number of connected components in the graph.  
*If you destroyed that vertex (node, etc) then the graph would break into multiple graphs.*

**Diameter**: The largest number of steps required to get between two nodes in the graph (assuming you take the shortest path to each vertex).

**Diametric**: When two nodes are the farthest distance possible from each other in the graph (assuming you take the shortest path)

---

**Degree**: a vertex’s degree is the number of edges incident on it

**In-degree**: (For directed graphs) A vertex’s in-degree is the number of edges ending at the vertex

**Out-degree**: “ the number of edges starting from the vertex

---

**Spanning Tree**: a subgraph that is a tree which includes all of the
vertices of G, with minimum possible number of edges

**Minimum Spanning Tree**: a subset of the edges of a connected,
edge-weighted undirected graph that connects all the vertices together,
without any cycles and with the minimum possible total edge weight.
That is, it is a spanning tree whose sum of edge weights is as small as
possible

**Dijkstra's algorithm**: an algorithm for finding the shortest
paths between nodes in a graph

**Prim's algorithm**: a greedy algorithm that finds a minimum spanning
tree for a weighted undirected graph

**Kruskal's algorithm**: a minimum-spanning-tree algorithm which
finds an edge of the least possible weight that connects any two
trees in the forest