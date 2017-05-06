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
Python does not have access modifiers, so it would not be a good idea to use getters or setters. To access a class member use the ‘.’ operator.

## Interfaces/ Protocols

### Swift

### Python 

Python is a duck type language so you do not necessarily need interfaces so the Java-style distinction between abstraction and interface does not exist. Python has multiple inheritance  

An abstract base class compliments duck - typing by providing a way to define interfaces. Python comes with multiple ABC’s for data structures, numbers and streams. 

```python

class Foo(object):
    def __getitem__(self, index):
        ...
    def __len__(self):
        ...
    def get_iterator(self):
        return iter(self)

class MyIterable:
    __metaclass__ = ABCMeta

    @abstractmethod
    def __iter__(self):
        while False:
            yield None

    def get_iterator(self):
        return self.__iter__()

    @classmethod
    def __subclasshook__(cls, C):
        if cls is MyIterable:
            if any("__iter__" in B.__dict__ for B in C.__mro__):
                return True
        return NotImplemented

MyIterable.register(Foo)
```


## Reflection

### Swift

### Python 

Because Python is a dynamic type language, it does not actually have reflection. It actually has something called Object introspection. Introspection is the ability to determine the type of object at runtime. Python ships with a few functions and modules to determine an object. 


Dir returns a list of attributes and methods belonging to an object.

```python 
my_list = [1, 2, 3]
dir(my_list)
# Output: ['__add__', '__class__', '__contains__', '__delattr__', '__delitem__',
# '__delslice__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__',
# '__getitem__', '__getslice__', '__gt__', '__hash__', '__iadd__', '__imul__',
# '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__',
# '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__',
# '__setattr__', '__setitem__', '__setslice__', '__sizeof__', '__str__',
# '__subclasshook__', 'append', 'count', 'extend', 'index', 'insert', 'pop',
# 'remove', 'reverse', 'sort']
```

Type returns the type of object. 

The inspect module provides useful functions to get information about live objects. 


## Memory Management

### Swift

### Python 

Python automatically manages memory within a private heap containing all python objects and data structures. The memory manager managers the private heap with different modules of the manager handling different types. The management of the private heap is ensured internally by the memory manager. At the lowest level a raw memory allocator ensures there is enough room in the private heap for all the data by interacting with the memory manager of the OS. The management of the python heap is performed by the interpreter itself and the user has no control over it.

## Comparison of References and Values

### Swift

### Python 
Python variables are compared by value by using the == operator. To compare variables by reference use the ‘is’ command. 

```python
	x = 5
	y = 5
	x == y #compares by value
	x is y #compares by reference
```
	


## Null/Nil References

### Swift

### Python 

Python uses the ‘none’ for null values. None is an instantiated singleton object. There is no null pointer exception in Python 

## Errors & Exception Handling

### Swift

### Python 

Python uses try and except statements. 
First, the try clause (the statement(s) between the try and exceptkeywords) is executed.
If no exception occurs, the except clause is skipped and execution of thetry statement is finished.
If an exception occurs during execution of the try clause, the rest of the clause is skipped. Then if its type matches the exception named after the except keyword, the except clause is executed, and then execution continues after the try statement.
If an exception occurs which does not match the exception named in the except clause, it is passed on to outer try statements; if no handler is found, it is an unhandled exception and execution stops with a message as shown above.
A try statement may have more than one except clause
At most one handler will be executed. 

The try ... except statement has an optional else clause, which, when present, must follow all except clauses

## Lambda Expressions, Closures, Functions as Types

### Swift

### Python 

## Implementation of Listeners and Event Handlers

### Swift

### Python 

Python does not have a native event listener. A programmer can import pre made libraries or make event listeners themselves. One example of the event listener is a library called EventHook. 

```Python
class MyBroadcaster()
    def __init__():
        self.onChange = EventHook()

theBroadcaster = MyBroadcaster()

# add a listener to the event
theBroadcaster.onChange += myFunction

# remove listener from the event
theBroadcaster.onChange -= myFunction

# fire event
theBroadcaster.onChange.fire()


class EventHook(object):

    def __init__(self):
        self.__handlers = []

    def __iadd__(self, handler):
        self.__handlers.append(handler)
        return self

    def __isub__(self, handler):
        self.__handlers.remove(handler)
        return self

    def fire(self, *args, **keywargs):
        for handler in self.__handlers:
            handler(*args, **keywargs)

    def clearObjectHandlers(self, inObject):
        for theHandler in self.__handlers:
            if theHandler.im_self == inObject:
                self -= theHandler
```	

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

```python
def DoAdd(MyList):
    Sum = 0
    if type(MyList) is list:
        for X in MyList:
            Sum += X
    return Sum
MyList = [1, 2, 3, 4, 5]
print(DoAdd(MyList))

```
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

Python is a high level programming language for general use programming. Python was created by Guido Van Rossum in 1991. Python has a philosophy to emphasize code readability. Python uses white spaces and code blocks rather than keywords and curly braces. Python has many practical uses to it and it is very versitile.
