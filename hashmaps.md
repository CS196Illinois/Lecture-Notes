# Hashmaps

## What are Hashmaps
Hashmaps are called 'Dictionaries' in python. </n>
Dictionaries are unordered collections of key-value pairs. </n>
Because dictionaries are unorderded, you cannot access elements by index. Instead, you access values by assigned 'keys'. 

## How do dictionaries work
Syntax:
```python

### Constructor
newDict = {} # initializes a dictionary with no values
newDict['newKey'] = 'newValue' # inserts a new key-value pair

### Constructor overload
stateMap = { 'pittsburgh':'PA', 'chicago':'IL'} # initializes a dictionary with predefined values
print stateMap['pittsburgh'] # returns 'PA'

### Constructor overload
pairs = [("cow", 5), ("dog", 98), ("cat", 1)]
d = dict(pairs) # has {'cow':5, 'dog':98, 'cat':1}
```

### Check for membership
```python
if 'pittsburgh' in stateMap:
  return stateMap['pittsburgh'] # prints 'PA'

### Key requirements
keys must be immutable types - no iterables!
```

### print the number of items in dictionary.
```python
d = { 1:[1,2,3,4,5], 2:"abcd" }
print(len(d))
```
### Dictionary Clear
```python
d = { 1:"a", 2:"b" }
d.clear()
print(d, len(d))
```
### Iterate over key/values in dictionary
```python
d = { 1:"a", 2:"b" }
for key in d:
   print(key, d[key])
```
### Check for membership
```python
d = { 1:"a", 2:"b" }
print(0 in d)
print(1 in d)
print("a" in d) # surprised?

### Check for non-membership
d = { 1:"a", 2:"b" }
print(0 not in d)
print(1 not in d)
print("a" not in d)
```
### Delete item
```python
d = { 1:"a", 2:"b" }
print(1 in d)
del d[1]
print(1 in d)
del d[1] # crash!

```
