# Object Oriented Language Comparison
### By Mark Madden and Miranda Reese

![alt text](https://upload.wikimedia.org/wikipedia/commons/7/7a/Apple-swift-logo.png "Swift") 
![alt text](https://www.iconattitude.com/icons/open_icon_library/apps/png/128/development-python.png "Python")

# Swift vs. Python

### Swift

### Python

## Language Purpose/ Genesis

### Swift

### Python 

Python is a high level programming language for general use programming. Python was created by Guido Van Rossum in 1991. Python has a philosophy to emphasize code readability. Python uses white spaces and code blocks rather than keywords and curly braces. This results in fewer lines of code. The language provides constructs intended to enable writing clear programs on both a small and large scale. 

## Unique Features

### Python

Python uses white spaces and code blocks rather than keywords and curly braces. Whitespace is used to denote blocks. In other languages curly braces are common. When you indent it becomes a child of the previous line. In addition to the indentation, the parent also has a colon following it. A line does not end with a semicolon ,which results in fewer lines of code.  Python does have many other unique features to it like the interactive interpreter, descriptors, yield, and the use of generators and coroutines. 



```javascript
something{ 
    something1 
    something2 
} something3
```

```python
Something 
   something1 
   something2 
Something3`
```


### Swift

### Python 

## Name Spaces

### Swift

### Python 

Python implements most namespaces. Namespaces in python have had many lifetimes because they are created at different times. The namespace containing Python’s built in names is created when the interpreter starts up. Namespaces read from a script file are called _main_ and have their own global namespace. 



## Types

### Swift

### Python 

The type system in Python is dynamic. Which means you do not need to declare a type when you are declaring a variable. Python supports,  booleans, integers, longs, floats, complex numbers, strings, bytes, byte arrays, lists, tuples, sets, and dictionaries. Numeric types, strings, tuples and sets are immutable. 


## Classes

### Swift

### Python 

Declaring a class in python is very simple and python does not have access modifiers. 

```python
class SampleClass     
```

To instantiate a class. 

```python
x = SampleClass()     
```

In python there are no access modifiers. To construct an object with arguments you have to define an _init_ method in the class.

```python
Class SampleClass
	Def __init__ (self, var1, var2)
		Self.var1 = var1

		Self.var2 = var2
```
    



```python
x = SampleClass('foo',18)
```



## Instance Reference

### Swift

### Python 

## Properties

### Swift

### Python 

## Interfaces/ Protocols

### Swift

### Python 

## Reflection

### Swift

### Python 

## Memory Management

### Swift

### Python 

Python automatically manages memory within a private heap containing all python objects and data structures. The memory manager managers the private heap with different modules of the manager handling different types. The management of the private heap is ensured internally by the memory manager. At the lowest level a raw memory allocator ensures there is enough room in the private heap for all the data by interacting with the memory manager of the OS. The management of the python heap is performed by the interpreter itself and the user has no control over it.

## Comparison of References and Values

### Swift

### Python 

## Null/Nil References

### Swift

### Python 

## Errors & Exception Handling

### Swift

### Python 

## Lambda Expressions, Closures, Functions as Types

### Swift

### Python 

## Implementation of Listeners and Event Handlers

### Swift

### Python 

## Singleton 

### Swift

### Python

There are multiple ways to implement a singleton in Python. You can use a decorator, a base class, a metaclass or a decorator returning a class with the same name. 

Here is an example of a singleton method created with a meta class

```python 
class Singleton(type):
    _instances = {}
    def __call__(cls, *args, **kwargs):
        if cls not in cls._instances:
            cls._instances[cls] = super(Singleton, cls).__call__(*args, **kwargs)
        return cls._instances[cls]

#Python2
class MyClass(BaseClass):
    __metaclass__ = Singleton

#Python3
class MyClass(BaseClass, metaclass=Singleton):
    pass
```

## Procedural Programming

### Swift

### Python 

Procedural programming is supported. Tasks are treated as a step by step iteration where tasks are placed in functions that are called as needed. This style favors iteration, sequencing, selection and modularization. The procedure style relies on procedure calls to create modularized code. 





## Functional Programming

### Swift

### Python

Python supports functional programming. Every statement is treated as a mathematical equation and any form of state or mutable data is avoided. This coding style lends itself well to parallel processing because there is no state to consider. 

```python
import functools
MyList = [1, 2, 3, 4, 5]
def AddIt(X, Y):
    return (X + Y)
Sum = functools.reduce(AddIt, MyList)
print(Sum)
```


## Multithreading

### Swift

### Python 

The thread class represents an activity that is run in a separate thread of control. There are two ways to specify the activity by passing an object to the constructor or by overriding the run()  method in a subclass. Once a thread is started, the thread is considered alive. It stops being alive when its run() method is terminated. There is a “main thread” object this corresponds to the initial thread control in the python program. Each thread instance has a name. 

The simplest way to use a thread is to instantiate it with a target function and call start().

```python
import threading

def worker():
    """thread worker function"""
    print 'Worker'
    return

threads = []
for i in range(5):
    t = threading.Thread(target=worker)
    threads.append(t)
    t.start()
```

## Conclusions

### Swift

### Python 
