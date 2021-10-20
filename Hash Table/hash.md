# Hash table
## What is a Hash Function?
Hash function is a function that map data of abitrary size to value of certain length. A hash function should be efficiently computed, randomly distributed and a one-way algorithm.
## What is Hash Table?
Hash table is a data structure that implements array data type. It maps keys to values
## What is the space complexity of a Hash Table?
O(n) 
n: size of array
## What is the time complexity of a Hash Table?
Insert, Update, Delete: O(1) -> best case, O(n) -> worst case
## When worst case happen?
When all values share the same key, we have to go through all node in linked list to perform insert, update, delete
## Explain in simple terms how Hash Tables are implemented?
Hash table is in the form of array ( or array of linked list). It uses hash function to compute index of a value in the array.

## Hash Collision? How to prevent?
Hash Collision is when hash function gives the same result for 2 different keys so it will possibly lead to data loss if we don't have any strategy to prevent it.

There are 2 ways to avoid collision:

1. Chaining: each slot in the hash table is a linked list. Therefore when the same value is calculated for 2 keys, the new value will be inserted to the linked list.
2. Open addressing: the hash table is just an array and the size of array must be bigger than the number of keys. When index computed by hash function is filled, we use probing to find suitable index for our value.
    
    Probing: 
    - insert:
    - update:
    - delete:

## What is load factor? When do we extend the hashtable size?
Load factor measures how full the table is. Depend on different languages, usually when load factor is larger then 75%

## Differentiate hashing, encoding and encryption? When to use what?
| Hashing  | Encoding | Encryption |
| ------------- | ------------- | ------------- |
| converting given key to smaller, fix-length value  | transformed data from one form to other form  | an encoding technique, in which message is encoded by encryption algorithm that only authorized people can read the message  |
| irreversible | reversible  | reversible  |
| get a key from value | transform data in a form that can be read by external process  | transfer private data  |

## Why search in hashtable is O(1) on average?
Let
- n: # of key stored in hashtable
- m: # of slots in hashtable

=> average length of each linked list = **n/m**

runtime complexity = O(1+n/m) = O(n/m)

in reality, n/m is a constant so O(n/m) ~ O(1)



