# Multi-Dimensional Arrays

Nested arrays are useful data structures to mimic n-dimensional spaces. Recall from our 1d list lecture that python lists can contain lists.
For example x = [[],[],[]] instantiates an array x with all indexes in the array pointing to another array. Notice that this data structure
can be manipulated to represent rows and columns of a grid, like so:

```python
x = [[1,2,3],
     [4,5,6],
     [7,8,9]]
```

In the 2d array shown above, "rows" in the grid are represented by lists in x. Columns are represented by the set of numbers in each
list that have the same index. For example, the first row of x is simply x[0]. The first column of x is x[0][0], x[1][0], x[2][0].

## static allocation of 2d lists
Syntax for accessing an element from a 2d array:
```python
print x[0][1] # prints the first index of the 0th list in x. In this case, prints the integer 2.
```
## dynamic allocation of 2d lists
## Getting 2d list dimensions
## Nested Looping over 2d arrays
## Jagged 2d lists
## n dimensional lists
