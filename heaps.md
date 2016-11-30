# Heaps

## What is a Heap?
Heap is a tree-based data structure where each level of the tree follows the "heap rule". For example, if the "heap rule" is
that all parent nodes must be bigger than their child nodes, this dictates how the nodes are ordered in the tree.

### We assume that all heaps are binary heaps. Every node has two children (like a BST!). There are different implementations of heaps, such as binomial and fibonacci
heaps, which are essentially a collection of trees where root nodes are linked together in a doubly linked list. These
configurations allow for runtime gains on insert, delete, and merge.

![heap](https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Min-heap.png/240px-Min-heap.png)

## Min vs Max Heap

A Min heap is a heap that follows the rule that "all parent nodes must be less than or equal to their child nodes". This means
that the root node of the heap is always the smallest number in the collection. The Max Heap is just the opposite. This means
the root node is the greatest in the collection.

## Runtimes

find-min(max): O(1) <br>
delete-min: O(logn)<br>
insert: O(logn)<br>
merge: O(n)<br>

### Question: How do you find the median of a running stream of integers?

