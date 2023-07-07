# Matrix Form (Adj Matrix)

1. Usually graphs are represented using 2D matrix of rows and cols

# Example

![main.excalidraw(10).png](main.excalidraw(10).png)

`0` means that there is no edge from that source node to destination node

`1` represents the direct edge between two nodes

<aside>
💡 In python this can be given as  a List[List[int]]

</aside>

```tsx
graph=[
[0,1,0,1,0],
[1,0,1,0,1],
[0,1,0,0,0],
[1,0,0,0,1],
[0,1,0,1,0],]
```

1. DFS and BFS are the popular algorithms for traversing these graphs

## Keep in mind

1. While traversing a matrix use set to keep track of visited (row,cols)
2. don’t  overflow