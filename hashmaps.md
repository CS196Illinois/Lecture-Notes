# Hashmaps

## What are Hashmaps
Hashmaps are called 'Dictionaries' in python. </n>
Dictionaries are unordered collections of key-value pairs. </n>
Because dictionaries are unorderded, you cannot access elements by index. Instead, you access values by assigned 'keys'. 

## How do dictionaries work
Syntax:
```python
newDict = {} # initializes a dictionary with no values
newDict['newKey'] = 'newValue' # inserts a new key-value pair

stateMap = { 'pittsburgh':'PA', 'chicago':'IL', 'seattle':'WA', 'boston':'MA' } # initializes a dictionary with predefined values
print stateMap['pittsburgh'] # returns 'PA'

if 'pittsburgh' in stateMap:
  return stateMap['pittsburgh'] # prints 'PA'

```
