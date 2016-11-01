# Linked Lists

##Contiguous vs Linked Data Structures
Data Structures can be classified as either Contiguous or linked, depending on whether they use arrays or pointers.

### Contiguous Data Structures
Contiguous Data Structures are allocated using a single slice of memory. Contiguous data structures include arrays, heaps, and hash tables.

### Linked Data Structures
Linked data structures are constructed using distinct chunks of memory and are tied together using pointers. These include trees, graphs, and linked lists.

##Linked Lists
There are several different types of linked lists such as:

### Singly Linked List vs Doubly Linked List

![alt text](https://cloud.githubusercontent.com/assets/7456865/19910374/8493c2b0-a05a-11e6-975c-b4ef9c0f82d8.png)

### Circularly Linked List

Circularly Linked Lists have a tail that has a pointer pointing back to the first node. Useful for things like Round-Robin Queues.

![alt text](https://cloud.githubusercontent.com/assets/7456865/19910394/a1d5e5ec-a05a-11e6-8ca2-aaeb0f8335a7.png)

## Why use linked Lists?

![alt text](https://cloud.githubusercontent.com/assets/7456865/19910299/1cf4958a-a05a-11e6-867f-44f2ffa386d1.png)

## The Linked List Class

```python
 class Node(object):
 
   def __init__(self, data=None, next_node=None):
       self.data = data
       self.next = next_node
```

## Iterating through a linked list
```python
  def print_list(head):
      while(head != None):
          print head.data
          head = head.next
```

## Add a node to the tail of a linked list
```python
  def Insert(head, data):
      if(head == None):
          return Node(data,None)
      else:
          pointer = head
          while(head.next != None):
              head = head.next
          head.next = Node(data, None)
      return pointer
```

## Keeping track of the Head Pointer
There are many problems where after conducting a manipulation, you have to return the entire linked list. This implies that you have to keep track of the head node. Make sure you keep a copy of the head node to return at the end of the problem.

## Tortoise and Hare Strategy - Detecting a Cycle in Linked Lists

Given a linked list, how do you figure out if it has a cycle?
Instantiate a slow and fast pointer
![alt text](https://cloud.githubusercontent.com/assets/7456865/19910310/2747f5ae-a05a-11e6-86d4-5bca17109c06.png)

Increment both pointers at different speeds
![alt text](https://cloud.githubusercontent.com/assets/7456865/19910315/3198f71a-a05a-11e6-80f1-c7f7187226ca.png)
![alt text](https://cloud.githubusercontent.com/assets/7456865/19910321/39f1b488-a05a-11e6-812b-38ce8991bf43.png)

If they meet, you know that there is a cycle!
![alt text](https://cloud.githubusercontent.com/assets/7456865/19910331/44b7e41e-a05a-11e6-893a-0f8a1f966909.png)

## Popular Linked List Questions
Iterate through a linked list <br>
Get value of node N in linked list<br>
Reverse a linked list<br>
Insert Node at head of linked list<br>
Insert Node at tail of linked list<br>
Insert Node at Nth position of linked list<br>
delete node at Nth position of linked list<br>
Merge two sorted linked lists<br>
Delete duplicate values in linked list<br>
Detect cycle in linked list<br>
Find whether or not two linked lists merge<br>
Given two merged linked lists, find the merge node<br>



