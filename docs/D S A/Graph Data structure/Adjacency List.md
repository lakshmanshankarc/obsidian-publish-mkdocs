# Adjacency List

Most common representation of graph

1. A lot easier than Matrix representation to traverse
2. Simply represented via a Dictionary or hash map or JavaScript object

## Example

![main.excalidraw(11).png](main.excalidraw(11).png)

Simply the Source is the key and the Array of values are the destinations

1. Advantage → A lot easier to traverse
2. We can also store weights in adj List but i don’t know how to do that in Adj matrix

```tsx
adj={
    0 : [ 1, 3 ],
    1 : [ 0, 2 ],
    2 : [ 1 ],
    3 : [ 0, 4 ],
    4 : [ 1, 3 ]
}
```

Okay that’s enough About What Graphs Now move on to traversal