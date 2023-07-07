A tree like Struct which has 2 pointer one for left sub Tree and other for right sub tree.

Creation
```python
class Node:
    def __init__(self, val) -> None:
        self.val = val
        self.left = None
        self.right = None

a = Node(1)
b = Node(2)
c = Node(3)
d = Node(4)
e = Node(5)

a.left = b
a.right = c

b.left = d
b.right = e
```

```
		a
	   / \
	  b   c
	 / \
	d   e
```


## Traversal
1. Depth First Traversal stack
```python
def dfsstack(root: Node):
    stack = [root]
    while stack:
        curr = stack.pop()
        print(curr.val)
        if (curr.left):
            stack.append(curr.left)

        if (curr.right):
            stack.append(curr.right)
	

```
2. DFS (recursion) 
```python
def dfs(root: Node):
    if not root:
        return
    dfs(root.left)
    print(root.val)
    dfs(root.right)
```
![[btree.png]]
The above is a binary Tree Traversal will be like this
1. Root (1) then push 2 and 3 onto stack the pop 3 then pop 2 
do this while stack is not empty

## Inorder Traversal
![[inorder.png]]
1. Left print
2. root then right
** ANS=> 4 2 5 1 3 ** 
```python
def inorder(root: Node):
    if not root:
        return

    inorder(root.left)
    print(root.val)
    inorder(root.right)
```

## Pre order
1. Traverse the root first 
2. then the left 
3. finally right
![[preorder.png]]
```python

def preorder(root: Node):
    if not root:
        return

    print(root.val, end="-> ")
    preorder(root.left)
    preorder(root.right)
```

## Post Order
1. Left
2. right Sub tree
3. then Print(root)
![[postorder.png]]

```python
def postorder(root: Node):
    if not root:
        return

    postorder(root.left)
    postorder(root.right)
    print(root.val, end="-> ")
```


# Level Order Traversal

1. BFS
   - using Queue we can implement BFS
   - Goes Level By level 
   - same as dfs stack but instead we use queue key diff  is we can traverse by levels 
```py

def bfs(root: Node):
    queue = [root]
    while queue:
        curr = queue.pop(0)
        print(curr.val)
        if (curr.left):
            queue.append(curr.left)

        if (curr.right):
            queue.append(curr.right)
```