# undirected Graph

These types of graph have no directions in edges

1. The can be traversed from source → destination or even destination to source
2. Example Facebook friends Kind of bidirectional Relationship

# Example

![main.excalidraw(3).png](data%20structures/D%20S%20A/Graph%20Data%20structure/undirected%20Graph%20img/main.excalidraw(3).png)

## Weighted undirected Graphs

Just add weights to edges, think of like distance between nodes.

<aside>
💡 Traveling along the edges can cost u the weight associated with it

</aside>

the cost of traveling form 1 → 3 is `4` like wise u can calculate

<aside>
💡 Dijkstra’s is the popular algorithm for shortest path. More about this on traversal page

</aside>

![main.excalidraw(8).png](main.excalidraw(8).png)

## Cycles

These are the directions that points to same nodes causing infinite loops

1. hash-set is used to avoid cycles in a graph
2. 

![main.excalidraw(9).png](main.excalidraw(9).png)

<aside>
💡 As u can see there is no direction this graph might contains cycles

</aside>

Example

`1` → `3` ⇒ `4` ⇒ `2` ⇒ `1`  which can be possible
