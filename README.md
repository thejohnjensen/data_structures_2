# Data-Structures
![alt image](https://travis-ci.org/thejohnjensen/data-structures.svg?branch=master)

**Classic data structures in python.  Paired programming.**

**Authors: Zach Taylor & John Jensen**

**Linked List**
Linked list is a linked data structure with only one pointer to the next node. Implemented in Python and JavaScript

`def push(self, data):` O(1)

`def pop(self):` O(1)

`def size(self):` O(1)

`def search(self, val):` O(n)

`def display(self):` O(n)

`def __len__(self):` O(1)

`def remove(self, node):` O(n)

`def __str__(self):` O(1)

**Stack**
A stack is a data structure where elements are stacked on top of one another. It operates in a first in first out fashion.

`def __len__(self):` O(1)

`def push(self, value):` O(1); unless pushed with iterable, then O(n)

`def pop(self):` 

**Doubly Linked List**
Doubly linked list is a linked data structure that has a link to previous and next nodes from inside of it. Also implemented in JavaScript

Time Complexity:

`def __len__(self):` O(1)

`def push(self, val):` O(1); unless initiated with iterable, then O(n)

`def append(self, val):` O(1)

`def pop(self):` O(1)

`def shift(self):` (1)

`def remove(self, val):` O(n)


**Queue**
We used composition from our doubly linked list to build our queue. The queue adds(enqueues) elements on one end and removes (dequeues) from the other end.

Time Complexity:

`def enqueue(self):` O(1); unless initiated with iterable, then O(n)

`def dequeue(self):` O(1)

`def peek(self):` O(1)

`def __len__(self):` O(1); count changes as enqueued and dequeued


**Deque**
The deque is a data structure that allows data to be inserted and removed from each end.

Time Complexity:

`def append(val):`  0(1)

`def appedleft(val):`  O(1)

`def pop()`:  O(1)

`def popleft()`:  O(1)

`def peek()`:  O(1)

`def peekleft()`:  O(1)

`def size()`:  O(1)


**Binary Heap**
A binary heap data structure is a tree type data structure that sorts the nodes relative to their parent/child relationship.

`def pop()`:  O(log n)
`def push(val)`:  O(log n)


**Priority Queue**
The priority queue data structure provides a way to represent data in a ordered "priority".  The benefit using this data structure has is that you can insert a new value at the given priority level without having to resort the entire list.  This makes adding new values much more efficient.  Our priority queue uses a high number = higher priority structure.

`def insert(val, priority)`: O(1)
`def pop()`:  O(n)
`def peek()`:  O(n)


**Unweighted Directed Graph**
A graph datastructure is an abstract way to represent data. Our graph uses a dictionary to store the node values and the edges are stored in a list for each node.

`nodes()`: O(n)
`edges()`: O(n^2)
`add_node(val)`: O(1)
`add_edge(val1, val2)`: O(1)
`del_node(val)`: O(n)
`del_edge(val1, val2)`: O(1)
`has_node(val)`: O(1)
`neighbors(val)`: O(1)
`adjacent(val1, val2)`: O(1)
`breadth_first_traversal(val)`: O(E + V) *
`depth_first_traversal(val)`: O(E + V) *
* where E is the number of edges and V is the number of Vertices via: https://stackoverflow.com/questions/6850357/explanation-of-runtimes-of-bfs-and-dfs


**Weighted Directed Graph**
A weighted graph is a graph that has weights assigned to the pointers.  A useful example of weighted pointers is how mapping software determines the distance between objects.  The objects are nodes, the weight in the pointers are the distances.

`nodes()`: O(n)
`edges()`: O(n * k)
`add_node(val)`: O(1)
`add_edge(val1, val2, weight)`: O(1)
`del_node(val)`: O(n)
`del_edge(val1, val2)`: O(1)
`has_node(val)`: O(1)
`neighbors(val)`: O(1)
`adjacent(val1, val2)`: O(1)
`breadth_first_traversal(val)`: O(n * k)
`depth_first_traversal(val)`: O(n * k)

###### Shortest Path Alogorithms:
`dijkstra(start, targe)`: O(E + VlogV)
`bellmanford(start, target)`:O(V * E)

The benefit of Dijkstra's shortest path algorithm is its efficiency and time complexity. However it does not report if the graph contains any negative looping paths.

The Bellmanford will alert the user of any negative cycles in the graph. However, this algorithm has a worse time complexity than Dijkstras.

**Binary Search Tree**
The binary search tree is a usefull algorithm for storing data and quickly being able to find it.

`insert(val)`: O(2log n) `since after insert I recursively assign depth values`
`search(val)`: O(log n)
`size()`: O(1)
`depth()`: O(1)
`contains(val)`: O(log n)
`balance()`: O(1)

Traversals:
* in_order: Traverse the nodes on the left, then root, then nodes on the right.
* pre_order: Return the root, then the nodes on left as they are visited then the right.
* post_order: Return the nodes on the left starting from the bottom up, then the right, then root.
* breadth_first: Return all nodes on level before goint to the next level.

`in_order()`: O(n)
`pre_order()`: O(n)
`post_order()`: O(n)
`breadth_first()`: O(n) 

BST Node Deletion:

`delete(val)`: O(log n)

**Hash Table**
The hash table uses a hashing algorithm to randomize the location of data in a table. This creates a simple dictionary.

`set(key, value)`: O(k) where k is the number of items in individual buckets.
`get(key)`: O(k) where k is the number of items in individual buckets. 
`hash()`: O(n) where n is length of key

Hashing Algorithms:
* Additivie: Adds the integer value of Unicode for each character. Similar permutations in same bucket.
* Bernstein: Uses a factor of 33 to offset the Unicode value for each character resulting in a more random placement of data. Similar permutations can end up in different buckets.


**Trie**
Tree of words linked with nodes containing the letters of the word. 

`insert(string)`: O(n) where n is length of string
`contains(string)`: O(n) where n is length of string
`size()`: O(1)
`remove(string)`: O(n) where n is length of string
`traverse(string)`: O(k + n) where k is length of string parameter and n is length of all words in trie.


**Bubble Sort**
Bubble sort is a bad sorting algorithm, very bad. Enough said.

`bubble_sort(list)`: O(n^2)

**Insertion Sort**
Insertion sort compares a current value against each value to its left until it finds the correct spot.

`insertion(list)`: O(n^2)

**Merge Sort**
Merge sort divides the list into smaller lists and then sorts each sub list. Then it rebuilds the list comparing each sub list.

`merge_sort(list)`: O(nlogn)

**Quick Sort**
Divide and conquer sorting algorithm.

`quick_sort(list)`: O(nlogn) -> worst case O(n^2)

**Radix Sort**
Sorting algorithm that sorts based on individual digits in the same position.

`radix_sort(list)`: O(n*w) where w is the length of the longest number