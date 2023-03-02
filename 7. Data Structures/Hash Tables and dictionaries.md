## Hash Tables

Hash tables are used to speed up searches for data dramatically. Each record in the data set is undergone a hashing algorithm or a hash function the resulting data structure used to store the data is called a hash table.

### Collision

A collision happens when an algorithm generates the same address for different primary keys. You need to deal with collision, the simplest way is to put the item in the next free slot available but this leads to clustering.

### Deletion

Items to be deleted should rather be replaced with dummy items so that when searching instead of finding an empty spot and returning null for the item it instead continues searching. If a new item is to be added then it replaces the dummy.

## Dictionary

A dictionary is an abstract data type made up of associated pairs, each pair has a key and a value. The key is the hashed function with the value matched to it.
