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
print x[0][1] # prints the 1st index of the 0th list in x. In this case, prints the integer 2.
```
## dynamic allocation of 2d lists
## Getting 2d list dimensions
How do we iterate over 2d lists if we don't know the list dimensions? Assuming that the 2d list is a square, we can simply get the length of any of the rows, which will also be the length of any arbitrary column. 

```python
rows = len(x)
cols = len(a[0])

print 'rows in x: ' + rows
print 'cols in x: ' + cols
```

## Nested Looping over 2d arrays
How do we go about iterating over all of the values in a 2d array? We can use nested for-loops, where the first for loop represents iteration of the rows, and the second for loop represents iteration of every index within each row. This means that your iteration will
start from the top-left of the grid, make its way to the end of the 0th array (ie the 0th row) and then make its way to the next row.

```python
# Instantiate a 2d list representing a matrix
a = [ [ 1, 2, 3] , [ 4, 5, 6 ] ] # notice that this is not a square 2d matrix!
print "Before: a =", a

# get the row AND column sizes, since it is not a square matrix
rows = len(a)
cols = len(a[0])

# And now loop over every element
for row in xrange(rows):
    for col in xrange(cols):
        print a[row][col]
```


## Jagged 2d lists

Lists do not have to be rectangular. We call these "jagged" or "ragged" lists. For these types of data structures, row and column lengths are unpredictable.

```python
x = [ [ 1, 2, 3 ] ,
      [ 4, 5 ],
      [ 6 ],
      [ 7, 8, 9, 10 ] ]

```


## n dimensional lists
## row-major vs column-major
