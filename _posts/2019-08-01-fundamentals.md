---
layout: post
author: Joeny Bui
---

# Data Structures

## Linked Lists

A linked list is a linear datat structure, in which the element are not stored at contiguous memory locations.  The elements in a linked list are linked using pointers.

![Image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/gq/2013/03/Linkedlist.png)

Arrays can be used to store linear data of similar types, but arrays have following limitations.

1. The size of the arrays if fixed.  We must know the upper limit in advanced.  Memory allocations is equal to the upper limit irrespective of the usage.
2. Insert a new element in an array is expensive, because room has to be created for the new elements and to create room existing elements have to shifted.

Pros:

* Dynamic Size
* Ease of insertion/deletion

Cons:

* Random access is not allowed.  We have to access elements sequentially starting from the first node.  Cannot do binary search with linked lists efficiently with its default implementation.
* Extra memory space for a pointer is required with each element of the list.
* Not cache friendly.

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None
```

## Binary Trees

Trees are hierarchical data structures.    A tree with whoose elements have at most 2 children is called a binary tree (typically called left and right child).

1. Good for file system.
2. Provide moderate access/search
3. Provide moderate insertion/deletion
4. No upper limit of number of nodes

```python
# binary tree
class Node:
    def __init__(self, key):
        self.left = None
        self.right = None
        self.val = key
```

### Tree Include

1. Manipulate hierarchical data.
2. Make information easy to search (see tree traversal)
3. Manipulate sorted lists of data.
4. As a workflow for compositing digital images for visual effects.
5. Router algorithms
6. Form of a multi-stage deicision-making

**Terms**

* root - topmost node
* children - elements that are directly under an elements
* parent - directly above an element

## Tries (aka digitial tree, radix tree or prefix tree)

Trie is an efficient information re**Trie**val data structure (often used to store characters).  Allowed for very fast lookup.  
Using Trie, search complexities can be brought to optimal limit (key length).

```
Binary Tree ==> M * log (N)
Trie ==> O(M)

where:
    M is maximum strength length
    N is number of keys in tree
```

Penalty is on Trie storage requirements.

```
class Node:
    children = <Character, Node>    
    is_complete_word = None
```

* store location in tree (index or return node of location)
* validation of words

## Stacks

### FIFO

### FILO

## Queues

## Vectors / ArrayLists

## Hash Tables

# Algorithms

## Breadth First Search

## Depth First Search

## Binary Search

## Merge Sort

## Quick Sort

## Tree Insert / Find /etc

# Concepts

## Bit Manipulation

## Singleton Design Pattern

## Factory Design Pattern

## Memory (Stack vs Heap)

## Recursion

## Big-O Time