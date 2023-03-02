## Graphs

A graph is a diagram consisting of circles, called vertices, joined by lines called edges. It is an abstract data structure that can be used to represent a wide range of different systems. A common type of graph is a tree.

### Trees

A tree is a common abstract data type (ADT).

```mermaid
graph TB
A((A))
B((B))
C((C))
D((D))
E((E))
F((F))
G((G))
H((H))
I((I))
J((J))
K((K))

A --- B
A --- C
A --- D

B --- E
B --- F

E --- I

C --- G
G --- J

D --- H
H --- K
```

A tree is a connected, undirected graph with no cycles.

A rooted tree is a tree but one that has an identified root, so every node has a unique parent apart from the root.

A binary tree is a rooted tree in which each node has a maximum of two children.

A balanced binary tree is a tree where the nodes are distributed in such a way that the height is kept to a minimum, allowing for more efficient searching.

A binary tree can be traversed in three different ways:

```mermaid
graph TB  

subgraph PostOrder

Pos1((3)) --> Pos2((1))

Pos1 --> Pos3((2))

end


subgraph InOrder

In1((2)) --> In2((1))

In1 --> In3((3))

end
subgraph PreOrder

Pre1((1)) --> Pre2((2))

Pre1 --> Pre3((3))

end  

```

### Graph Traversal Algorithms

There are two ways of traversing a graph:

- Depth-first, going down as far as you can down a path before back tracking and going down the next.
- Breath-first, exploring all of the neighbours of the current vertex then the neighbours of each vertex after that.

```mermaid
graph LR
A((A)) --- B
B((B)) --- C
C((C)) --- G((G))
A --- D
D((D)) --- B
D --- F((F))
A --- E
E((E)) --- D
```

Depth first: A, B, C, G, D, F, E

Breadth first: A, B, D, E, C, F, G

#TODO
