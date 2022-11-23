---
banner: "![[Pasted image 20220510003018.png]]"
banner_y: 0.25334
---

# Data Structures

10/05/2022

## Introduction

### Data Types

| Category             | Word                         |
| -------------------- | ---------------------------- |
| h0dobo               |                              |
| text                 | text                         |
| Elementary data type | Integer, real, boolean, char |
| Composite data type  | string, array                |
| Abstract data type   | list, stack, queue           |

### Abstraction

An abstract data type (ADT) is a logical description of how we view the data and possible operations. We are only concerned with what the data is representing and not how it is constructed. Creating an encapsulation around the data - a form of information hiding.

### Dynamic Vs Static

Static data structures are fixed in size, they cannot grow or shrink. An array is an example of a static data structure.
Dynamic data structures can grow and shrink, allocating and deallocating memory from the heap (an area of memory used for this purpose)

### Arrays and Lists

> An **Array** is a systematic arrangement of similar objects, usually in rows and columns.
> [Wikipedia](https://en.wikipedia.org/wiki/Array)

Arrays are ordered sets of data of the same type grouped together using a single identifier. Arrays can have multiple dimensions.


> [!NOTE] Lists
> Lists are similar to arrays however they are dynamic and can shrink or grow depending on the amount of data in the structure.

### Overflow and Underflow

Overflow - Attempting to push onto a data structure that is full.
Underflow - Attempting to pop from a data structure that is empty.

## Queues

> In computer science, a queue is a collection of entities that are maintained in a sequence and can be modified by the addition of entities at one end of the sequence and the removal of entities from the other end of the sequence. By convention, the end of the sequence at which elements are added is called the back, tail, or rear of the queue, and the end at which elements are removed is called the head or front of the queue, analogously to the words used when people line up to wait for goods or services.
> The operation of adding an element to the rear of the queue is known as enqueue, and the operation of removing an element from the front is known as dequeue.
> Another usage of queues is in the implementation of breadth-first search.
> [Wikipedia](https://en.wikipedia.org/wiki/Queue%20(abstract%20data%20type))

A queue is a data structure under a first in last out (FIFO) system. With either adding items to the rear or removing items from the front. A queue as a fixed size array may easily run into problems as the pointer of where the head is increases by one rather than changing the data beneath it. Therefore circular queues are made.

### Circular Queue

A circular queue fixes this problem by reusing spaces that have been freed by dequeuing from the front of the array instead of just moving the pointer along one.

### Priority Queue

In a priority queue some items are allowed to jump the queue as each item has a different priority associated with it.

## Stacks

> In computer science, a stack is an abstract data type that serves as a collection of elements, with two main principal operations:
> Push, which adds an element to the collection, and
> Pop, which removes the most recently added element that was not yet removed.
> A stack is needed to implement depth-first search.
> [Wikipedia](https://en.wikipedia.org/wiki/Stack%20(abstract%20data%20type))

A stack is similar to a queue however the order of insertion is the reverse of the order of removal ie Last in first out (LIFO).

### Call Stacks

A common example of a stack is the call stack which is a system level data structure that provides the mechanism for passing parameters, return addresses and any processor register values to subroutines.

A stack frame contains all the parameters, the return address and the local variables for a single call to a subroutine which has not yet completed.

## Hash Tables

Hash tables are used to speed up searches for data dramatically. Each record in the data set is undergone a hashing algorithm or a hash function the resulting data structure used to store the data is called a hash table.

### Collision

A collision happens when an algorithm generates the same address for different primary keys. You need to deal with collision, the simplest way is to put the item in the next free slot available but this leads to clustering.

### Deletion

Items to be deleted should rather be replaced with dummy items so that when searching instead of finding an empty spot and returning null for the item it instead continues searching. If a new item is to be added then it replaces the dummy.

## Dictionary

A dictionary is an abstract data type made up of associated pairs, each pair has a key and a value. The key is the hashed function with the value matched to it.

## Graphs

A graph is a diagram consisting of circles, called vertices, joined by lines called edges. It is an abstract data structure that can be used to represent a wide range of different systems. A common type of graph is a tree.

### Trees

A tree is a common abstract data type (ADT).
![[Pasted image 20220510020140.png]]`center`
A tree is a connected, undirected graph with no cycles.
    A rooted tree is a tree but one that has an identified root, so every node has a unique parent apart from the root.
        A binary tree is a rooted tree in which each node has a maximum of two children.
            A balanced binary tree is a tree where the nodes are distributed in such a way that the height is kept to a minimum, allowing for more efficient searching.

A binary tree can be traversed in three different ways:
![[Pasted image 20220510021908.png]]`center`

### Graph Traversal Algorithms

There are two ways of traversing a graph:
- Depth-first, going down as far as you can down a path before back tracking and going down the next.
- Breath-first, exploring all of the neighbours of the current vertex then the neighbours of each vertex after that.

![[Pasted image 20220510022449.png]] `left`
Depth first: A, B, C, G, D, F, E
Breadth first: A, B, D, E, C, F, G










#compsci #datascience #linkback