# Object Oriented Language Comparison
### By Mark Madden and Miranda Reese

# Swift vs. Python

![alt text](https://upload.wikimedia.org/wikipedia/commons/7/7a/Apple-swift-logo.png "Swift") 
![alt text](https://www.iconattitude.com/icons/open_icon_library/apps/png/128/development-python.png "Python")

## Language Purpose/ Genesis

### Swift

Swift is a multi-paradigm programming language developed by Apple for iOS, macOS, watchOS, tvOS, and Linux systems. It works with Apple's extant programs such as Cocoa and Cocoa Touch Frameworks and Objective-C, the predecessor to Swift. Swift is considered safer, with more error checking and concise coding. It was first introduced in 2014 at Apple's Worldwide Developers Conference, with Swift 2 being revealed at the 2015 conference, and Swift 3 in 2016. In 2017, Swift was named one of the top ten programming languages in the monthly TIOBE rankings. 

### Python 

Python is a high level programming language for general use programming. Python was created by Guido Van Rossum in 1991. Python has a philosophy to emphasize code readability. Python uses white spaces and code blocks rather than keywords and curly braces. This results in fewer lines of code. The language provides constructs intended to enable writing clear programs on both a small and large scale. 

## Unique Features

### Swift
Though it is an alternative to Objective-C, Swift shares some similar syntax. Swift does not utilize pointers, as this would typically lead to many errors if handled incorrectly. The core data framework was introduced in Swift 3, as a quicker way to manage data by utilizing NSManaged Objects. Swift's editing board is primarily designed for creating iOS application and offers a unique mapping view to easily visualize a project. It allows buttons, labels, text fields, and more to be linked directly into code through IB Outlets and IB Actions. 
```swift
 @IBOutlet weak var taskTextField: UITextField!
 //example of an IBOutlet connected to a text field
 
 @IBAction func buttonTapped(_ sender: UIButton)
 //example of an IBAction connected to the push of a button
```
Swift also utilizes delegates, giving a chain of responsibility typically to higher classes, or in the iOS apps, usually a ViewController, a.k.a. the main screen. A smaller feature with coding is that Swift doesn't use semi-colons to end a line. Swift also has a unique feature in optionals, or allowing a reference or value to be nil. To access a value that is optional, the programmer must unwrap it with an exclamation mark(!) first. There is also optional chaining to test if something is nil, and only unwrap it if it isn't. This is done with a question mark (?).

```swift
  let myValue = anOptionalInstance!.someMethod()
  //the ! operator unwraps anOptionalInstance to expose the instance inside, allowing the method call to be made on it
  
  let myValue = anOptionalInstance?.someMethod()
  //the runtime only calls someMethod if anOptionalInstance is not nil
 
```


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
## Name Spaces

### Swift
Namespaces, while advertised during the WWDC, seem to be more implicit for developers. Though it's intention was not to be conflicting, such as when an imported kit contains the same name, something called "name mangling" takes place and Swift handles it. No class prefixes are needed either. Swift doesn't offer as much flexibility with namespace types or constants within modules.

```swift
import FrameworkA
import FrameworkB

FrameworkA.foo()
```

### Python 

Python implements most namespaces. Namespaces in python have had many lifetimes because they are created at different times. The namespace containing Python’s built in names is created when the interpreter starts up. Namespaces read from a script file are called _main_ and have their own global namespace. 

## Types

### Swift

In Swift, there are two kinds of types: named types and compound types. A named type is a type that can be given a particular name when it is defined. Named types include classes, structures, enumerations, and protocols. Basic or primitive data types are also considered named types, so programmers can extend their behavior to suit the needs of their programs using an extension declaration. A function type represents the type of a function, method, or closure and consists of a parameter and return type separated by an arrow (->). A tuple type is a comma-separated list of types, enclosed in parentheses.

```swift
var someTuple = (top: 10, bottom: 12)  // someTuple is of type (top: Int, bottom: Int)
someTuple = (top: 4, bottom: 42) // OK: names match
someTuple = (9, 99)              // OK: names are inferred
someTuple = (left: 5, right: 5)  // Error: names don't match
```

### Python 

The type system in Python is dynamic. Which means you do not need to declare a type when you are declaring a variable. Python supports,  booleans, integers, longs, floats, complex numbers, strings, bytes, byte arrays, lists, tuples, sets, and dictionaries. Numeric types, strings, tuples and sets are immutable. 

## Classes

### Swift

Swift does not require you to create separate interface and implementation files for custom classes and structures. You define a class or a structure in a single file, and the external interface to that class or structure is automatically made available for other code to use. Whenever you define a new class or structure, you effectively define a brand new Swift type. Classes are typically upper camel cased, while methods and functions are lower camel cased. Class instances are always passed by reference.

```swift
class SomeClass {
     var name: String?
     var interlaced = false
     var double = 0.0

}
```

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

As stated before, Swift classes are passed by reference. When an object is created from a class, this is often referred to as an "instance." Classes use initializer syntax for new instances. The simplest form of initializer syntax uses the type name of the class or structure followed by empty parentheses. This creates a new instance of the class or structure, with any properties initialized to their default values. 

```swift
let classInstance = Instance()
```

### Python 

## Properties

### Swift

Properties associate values with a particular class, structure, or enumeration. Stored properties store constant and variable values as part of an instance, whereas computed properties calculate a value directly. Computed properties come from classes, structures, and enumerations. Stored properties are from only by classes and structures. Swift also has lazy properties, which are not calculated until the first time it is used. There are also type properties, which are associated with instances of a particular type.

```swift
struct Rect {
    var origin = Point()
    var size = Size()
    var center: Point {
        get {
            let centerX = origin.x + (size.width / 2)
            let centerY = origin.y + (size.height / 2)
            return Point(x: centerX, y: centerY)
        }
        set(newCenter) {
            origin.x = newCenter.x - (size.width / 2)
            origin.y = newCenter.y - (size.height / 2)
        }
    }
}
var square = Rect(origin: Point(x: 0.0, y: 0.0),
                  size: Size(width: 10.0, height: 10.0))
//example of computed properties

struct FixedLengthRange {
    var firstValue: Int
    let length: Int
}
var rangeOfThreeItems = FixedLengthRange(firstValue: 0, length: 3)
// the range represents integer values 0, 1, and 2
rangeOfThreeItems.firstValue = 6
//example of stored properties

class DataManager {
    lazy var importer = DataImporter()
    var data = [String]()
    // the DataManager class would provide data management functionality here
}
//example of a lazy property being used

```

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

Small anonymous functions can be created using the lambda keyword. Lambda functions can be used wherever function objects are required. They are syntactically restricted to a single expression. Lambda functions can reference variables from the containing scope. 

```python
>>> def make_incrementor(n):
...     return lambda x: x + n
...
>>> f = make_incrementor(42)
>>> f(0)
42
>>> f(1)
43
```

A Closure is a function object that remembers values in enclosing scopes even if they are not present in memory. Let us get to it step by step

Firstly, a Nested Function is a function defined inside another function. At least in python, they are only readonly. However, one can use the "nonlocal" keyword explicitly with these variables in order to modify them.


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
