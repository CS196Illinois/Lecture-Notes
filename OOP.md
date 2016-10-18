# Object Oriented Python and Other Things

## OOP in Python

Python is an "object-supported" language, which means that it is not strictly object-oriented, but does have features that allow
programmers to use OOP if they wish.

## Syntax

###Declaring a class
```python

class car:

  count = 0 # Class variable that is shared by all objects of class

  def __init__(self, brand):
    self.brand = brand # Instance variable that is unique to each object instantiation
  
  
```

###Instance Methods
Methods in classes look almost exactly the same as they do without, except you must pass in self:

```python
def getValue(self):
  return self.value
```

###Static Methods
Static methods are methods that do not require an instance of the class. Since these methods don't require an instance to be passed in, we do not pass in "self".

```python
@ staticmethod
def getValue():
  return "value"
```

Notice the @staticmethod decorator, which lets python know that the method signature does not require an instance of the class.

### Class Methods


###Inheritence

### Designing Variables for Inheritance
Private vs Public variables: <br>
Public attributes are those that you expect unrelated clients of your class to use, with your commitment to avoid backward incompatible changes. 

Culturally, in python, you don't want to write to other class' instance or class variables. 

## OOP Principles

Encapsulation
Inheritance
Polymorphism



## Abstract Classes vs Interfaces

## Decorators

## Command Line


