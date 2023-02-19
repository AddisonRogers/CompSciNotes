## Queues

A queue is a data structure under a first in last out (FIFO) system. With either adding items to the rear or removing items from the front. A queue as a fixed size array may easily run into problems as the pointer of where the head is increases by one rather than changing the data beneath it. Therefore circular queues are made.

### Circular Queue

A circular queue fixes this problem by reusing spaces that have been freed by dequeuing from the front of the array instead of just moving the pointer along one.

### Priority Queue

In a priority queue some items are allowed to jump the queue as each item has a different priority associated with it.