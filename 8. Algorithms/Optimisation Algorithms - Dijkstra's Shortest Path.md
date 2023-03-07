Whenever you need to send a message across the internet your ip-router has to determine the best and fastest way to send your message.

This is where Dijkstra's shortest path algorithm can be used.

Designed to find the shortest path between a start node and every other node in a weighted graph.

The implementation of the algorithm is similar to a breadth first search.

It uses a priority queue as the supporting data structure to keep a record of which vertex to visit next.

It starts by assigning a temporary distance value to each node.

The temporary distance is 0 at the start node, and infinity at every other node.

 ```mermaid
 graph LR
 A
 B
 C
 D
 E
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

## How to Do it

<https://www.youtube.com/watch?v=pVfj6mxhdMw>

First we start at A and assign the distance it took to get there (0)

 ```mermaid
 graph LR
 A
 style A fill:#bbf
 B
 C
 D
 E
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

```mermaid
graph TB
A=0 
B=?
C=?
D=?
E=?
```

Next we see the distance it takes to get to B or D the neighbours of A.

 ```mermaid
 graph LR
 A
 style A fill:#ffffff
 B
 style B fill:#bbf
 C
 
 D
 style D fill:#bbf
 E
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

```mermaid
graph TB
D=3
B=7
C=?
E=?
```

Next we follow the shortest distance (D) and go to it adding it to our count.

We then visit the neighbours of D (everyone) and see the distance to each node.

 ```mermaid
 graph LR
 A
 style A fill:#ffffff
 B
 style B fill:#bbf
 C
 style C fill:#bbf
 D
 style D fill:#ffffff
 E
 style E fill:#bbf
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

We then count the distance from origin to D (3) + the distance to each other node.

```mermaid
graph TB
B=5
C=7
E=10
```

Then we move to B

 ```mermaid
 graph LR
 A
 style A fill:#ffffff
 B
 style B fill:#ffffff
 C
 style C fill:#bbf
 D
 style D fill:#ffffff
 E
 style E fill:#bbf
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

And then we check if the distance to the remaining neighbours are greater than or less than their pre-recorded values. ie 5 to get to B + 3 to get to c = 8, and as this is greater than our pre-recorded value we do not change it as we get to it faster from A-D-C rather than A-D-B-C

```mermaid
graph TB
C=7
E=10
```

We are now at C where we can count if A-D-B-C-E (7+1) is faster than any other method.

 ```mermaid
 graph LR
 A
 style A fill:#ffffff
 B
 style B fill:#ffffff
 C
 style C fill:#ffffff
 D
 style D fill:#ffffff
 E
 style E fill:#bbf
 A-- 7 --- B
 A-- 3 --- D
 B-- 2 --- D
 B-- 3 --- C
 B-- 6 --- E
 C-- 1 --- E
 C-- 4 --- D
 D-- 7 --- E
```

```mermaid
graph TB

E=8
```

And now we have the full distances:

```mermaid
graph TB
A=0 
B=5
C=7
D=3
E=8
```
