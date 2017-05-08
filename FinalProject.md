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
Though it is an alternative to Objective-C, Swift shares some similar syntax. Swift does not utilize pointers, as this would typically lead to many errors if handled incorrectly. The core data framework was introduced in Swift 3, as a quicker way to manage data by utilizing NSManaged Objects. Swift works well when used with XCode, also Apple's program, an editing board that is primarily designed for creating iOS applications and offers a unique mapping view to easily visualize a project. It allows buttons, labels, text fields, and more to be linked directly into code through IB Outlets and IB Actions. 
```swift
 @IBOutlet weak var taskTextField: UITextField!
 //example of an IBOutlet connected to a text field
 
 @IBAction func buttonTapped(_ sender: UIButton)
 //example of an IBAction connected to the push of a button
```
Swift also utilizes delegates, giving a chain of responsibility typically to higher classes, or in the iOS apps, usually a ViewController, a.k.a. the main screen. A smaller feature with coding is that Swift doesn't use semi-colons to end a line. Swift also has a unique feature in optionals, or allowing a reference or value to be nil. This explained more in detail later.

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


The instantiation operation (“calling” a class object) creates an empty object. Many classes like to create objects with instances customized to a specific initial state. Therefore a class may define a special method named __init__(), like this:

```python
def __init__(self):
    self.data = []
```
When a class defines an __init__() method, class instantiation automatically invokes __init__() for the newly-created class instance. So in this example, a new, initialized instance can be obtained by:

```python
x = MyClass()
```

## Properties

### Swift

Properties associate values with a particular class, structure, or enumeration. Stored properties store constant and variable values as part of an instance, whereas computed properties calculate a value directly. Computed properties come from classes, structures, and enumerations. Stored properties are from only by classes and structures.  There are also type properties, which are associated with instances of a particular type.

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
```

Swift also has lazy properties, which are not calculated until the first time it is used.
```swift
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
A protocol defines a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality. It can be adopted by a class, structure, or enumeration to provide an actual implementation of those requirements. Any type that satisfies the requirements of a protocol is said to conform to that protocol. A protocol is defined similarly to a class or struct with curly braces. 
```swift
protocol SomeProtocol {
    // protocol definition goes here
}
//basic protocol definition
```
Multiple protocols can be listed, and are separated by comma.
```swift

struct SomeStructure: FirstProtocol, AnotherProtocol {
    // structure definition goes here
}
//multiple protocol definition
```
 If a class has a superclass, list the superclass name before any protocols it adopts, followed by a comma.
```swift
class SomeClass: SomeSuperclass, FirstProtocol, AnotherProtocol {
    // class definition goes here
}
//superclass protocol definition
```

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
Swift's reflection capabilities are based around a struct called Mirror. You create a mirror for a particular subject and the mirror will then let you query it. To create a mirror, you use the reflecting initializer.
```swift
public init(reflecting subject: Any)

let aMirror = Mirror(reflecting: aClass)
```
The mirror has a few types to determine the information to query. There is a display enum for each type.
```swift
public enum DisplayStyle {
    case Struct
    case Class
    case Enum
    case Tuple
    case Optional
    case Collection
    case Dictionary
    case Set
}
```
And there is an ancestor representation enum.
```swift
public enum AncestorRepresentation {
    /// Generate a default mirror for all ancestor classes.  This is the
    /// default behavior.
    case Generated
    /// Use the nearest ancestor's implementation of `customMirror()` to
    /// create a mirror for that ancestor.      
    case Customized(() -> Mirror)
    /// Suppress the representation of all ancestor classes.  The
    /// resulting `Mirror`'s `superclassMirror()` is `nil`.
    case Suppressed
}
```

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
Swift utilizes the Automatic Reference Counting technology for some aspects of memory management. ARC automatically frees up the memory used by class instances when those instances are no longer needed. When a new instance of a class is created, the ARC allocates a chunk of memory to store information about that instance. The memory holds all the information about that instance, including properties and variables. When the instance is no londer needed the ARC automatically frees up the memory so that it can be utilized somewhere else. It is important to note that the ARC may cause a program to crash if it deallocates memory while the instance is still in use. As a preventative measure, the ARC tracks how many properties, constants, and variables are currently referring to each class instance. ARC will not deallocate an instance as long as at least one active reference to that instance still exists.
Here is a simple class being created:
```swift
class Person {
    let name: String
    init(name: String) {
        self.name = name
        print("\(name) is being initialized")
    }
    deinit {
        print("\(name) is being deinitialized")
    }
}
```
Now we can assign references to a person, along with variables.
```swift
var reference1: Person?
var reference2: Person?
var reference3: Person?

reference1 = Person(name: "John Doe")
// Prints "John Doe is being initialized"
```
Because the new Person instance has been assigned to the reference1 variable, there is now a strong reference from reference1 to the new Person instance. Because there is at least one strong reference, ARC makes sure that this Person is kept in memory and is not deallocated.
```swift
reference2 = reference1
reference3 = reference1
```
If we continue to assign reference2 and reference3 to reference1, this creates an even stronger reference to ensure the ARC will not deinitialize Person.

```swift
reference1 = nil
reference2 = nil
```
Now, even though the original reference has been broken, there is still a single reference to Person with reference3 due to it not being completely broken. Once we write:
```swift
reference3 = nil
// Prints "John Doe is being deinitialized"
```
The program now sees Person is no longer used at all, and deinitializes it.

### Python 

Python automatically manages memory within a private heap containing all python objects and data structures. The memory manager managers the private heap with different modules of the manager handling different types. The management of the private heap is ensured internally by the memory manager. At the lowest level a raw memory allocator ensures there is enough room in the private heap for all the data by interacting with the memory manager of the OS. The management of the python heap is performed by the interpreter itself and the user has no control over it.

## Comparison of References and Values

### Swift
Types in Swift have two categories. Value types are where each instance keeps a unique copy of its data, usually defined as a struct, enum, or tuple. 
```swift
// Value type example
struct S { var data: Int = -1 }
var a = S()
var b = a						// a is copied to b
a.data = 42						// Changes a, not b
println("\(a.data), \(b.data)")	// prints "42, -1"
```
The second are reference types, where instances share a single copy of the data, and the type is usually defined as a class.
```swift
// Reference type example
class C { var data: Int = -1 }
var x = C()
var y = x						// x is copied to y
x.data = 42						// changes the instance referred to by x (and y)
println("\(x.data), \(y.data)")	// prints "42, 42"
```

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

As stated before, Swift allows a unique way to handle null/nil references via something called optionals. To access a value that is optional, the programmer must unwrap it with an exclamation mark(!) first.

```swift
  let myValue = anOptionalInstance!.someMethod()
  //the ! operator unwraps anOptionalInstance to expose the instance inside, allowing the method call to be made on it
```
There is also optional chaining to test if something is nil, and only unwrap it if it isn't. This is done with a question mark (?).
```swift
  let myValue = anOptionalInstance?.someMethod()
  //the runtime only calls someMethod if anOptionalInstance is not nil
```

### Python 

Python uses the ‘none’ for null values. None is an instantiated singleton object. There is no null pointer exception in Python 

## Errors & Exception Handling

### Swift
Swift has features that enable throwing, catching, propagating, and manipulating recoverable errors at runtime. Optionals and optional chaining are important features to utilize to find nil values before running it through a method. Errors are represented by values of types that conform to the Error protocol. Enums are often used to make cases for certain types of errors. It's easy to throw an error back, however, there usually needs to be some code written around it to deal with the problem. There are four ways to handle errors in Swift: propagate the error from a function to the code that calls that function, handle the error using a do-catch statement, handle the error as an optional value, or assert that the error will not occur. 

```swift
enum VendingMachineError: Error {
    case invalidSelection
    case insufficientFunds(coinsNeeded: Int)
    case outOfStock
}

throw VendingMachineError.insufficientFunds(coinsNeeded: 5)
//error is throwing the integer 5 back to the error
```
Swift does have try...catch elements, where if an error is thrown by the code in the do clause, it is matched against the catch clauses to determine which one of them can handle the error.
```swift

do {
    try buyFavoriteSnack(person: "Alice", vendingMachine: vendingMachine)
} catch VendingMachineError.invalidSelection {
    print("Invalid Selection.")
} catch VendingMachineError.outOfStock {
    print("Out of Stock.")
} catch VendingMachineError.insufficientFunds(let coinsNeeded) {
    print("Insufficient funds. Please insert an additional \(coinsNeeded) coins.")
}
//example of a try...catch statement
```

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
Closures in Swift are similar to blocks in C and Objective-C and to lambdas in other programming languages. Swift will handle the memory management of closures automatically, storing references of the objects and variables the closure captured. There are three types of closures: global functions that have a name and do not capture any values, nested functions that have a name and can capture values from their enclosing function, and closure expressions that are unnamed and written in a lightweight syntax that can capture values from their surrounding context.
Closure expression syntax has the following general form:
```swift
{ (parameters) -> return type in
    statements
}
```
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
Swift has event handlers much like Objective-C. The Event class has a generic parameter T which defines the type of data that this event conveys and the EventHandler typealias declares a function that accepts this type. You can pass in multiple parameters to events as tuples.

```swift
class Event<T> {

  typealias EventHandler = T -> ()

  private var eventHandlers = [EventHandler]()

  func addHandler(handler: EventHandler) {
    eventHandlers.append(handler)
  }

  func raise(data: T) {
    for handler in eventHandlers {
      handler(data)
    }
  }
}
```

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

Singletons were typically abused in Objective-C as global varbiales, but were still carried over into Swift, just implemented differently. Singleton patterns are pretty simple too.
```swift
// Shared URL Session
let sharedURLSession = URLSession.shared

// Default File Manager
let defaultFileManager = FileManager.default
```
A singletone allows you to create only one instance of a class, but that instance becomes a global variable, which can lead to problems if not handled correctly. You can access the variable within the AppDelegate of the class as well, which honestly, saves time and convenience. Global variables are initialized lazily, so they aren't run until they need to be. Swift also has static properties, which can be an easier and more elegant alternative to global variables.
```swift
class example {
    static let sharedInstance = example()
}
```

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
Swift does support procedural programming, which can be demonstrated within a playground. Here, taking in an array of names, is a function that can sort through them all in a procedure and return the new order.  The logic of sorting rides by name has been captured in a single, testable modular and reusable function.

```swift
func sortedNames(rides: [Ride]) -> [String] {
  var sortedRides = rides
  var i, j : Int
  var key: Ride

  // 1
  for (i = 0; i < sortedRides.count; i++) {
    key = sortedRides[i]

    // 2
    for (j = i; j > -1; j--) {
      if key.name.localizedCompare(sortedRides[j].name) == .OrderedAscending {
        sortedRides.removeAtIndex(j + 1)
        sortedRides.insert(key, atIndex: j)
      }
    }
  }

  // 3
  var sortedNames = [String]()
  for ride in sortedRides {
    sortedNames.append(ride.name)
  }

  print(sortedRides)

  return sortedNames
}
```

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
Swift is not a functional language, but does allow functional programming. It offers immutability for certain variables with the "let" functionality. This may seem contradictory with changing an unchagneable object, but Swift offers something different with functional programming. When tossed into a function, rather than mutating the object, a new object with the desired changes is returned. With Swift, there is a way to design the class so as to declare a constant stored property. The method would then produce new instance that stored the new state.

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
Swift uses the Grand Central Dispatch (GCD), a low-level API for managing concurrent operations, for multi-threading. In Swift 3, GCD was updated from a more C-based API to an API that included new classes and new data structures. Threads are usually handled independently. Single-core devices can achieve concurrency through time-slicing. They would run one thread, perform a context switch, then run another thread. Multi-core devices can handle multiple threads due to parallelism. There are also dispatch queues that handle multiple tasks in a FIFO manner. There are three different types of queues: main, global, and custom. When you set up queues, instead of giving a priority system, you assign one of four wuality of service classes. User-interactive which represent the tasks that need to be done immediately in order to provide a nice user experience such as UI updates, event handling and small workloads that require low latency. This should run on the main thread and the overall workload kept small. Tasks that are initiated from the UI and can be performed asynchronously are user-initiated. It should be utilized user is waiting for immediate results, and for tasks required to continue user interaction.
Utility are long-running tasks, typically with a user-visible progress indicator used for computations, I/O, networking, continous data feeds and similar tasks. This class is designed to be energy efficient and will get mapped into the low priority global queue. Lastly, background QoS are tasks that the user is not directly aware of such as prefetching, maintenance, and other tasks that don’t require user interaction and aren’t time-sensitive. This will get mapped into the background priority global queue.

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
Swift is very useful language for programmers to learn, especially with its rising popularity since its inception. The technology trend has seen a shift from websites to mobile platforms, something Swift is built for. As a future programmer, it is important to know many languages that operate on different platforms. Swift, when utilized with the easy-to-use interface of XCode, has great features for any size company to use to build powerful iOS applications. With more time, Swift will only grow to be more powerful and useful.


### Python 

Python is a high level programming language for general use programming. Python was created by Guido Van Rossum in 1991. Python has a philosophy to emphasize code readability. Python uses white spaces and code blocks rather than keywords and curly braces. Python has many practical uses to it and it is very versitile. Many companies such as Google use python as their main language because it is so versitile. 
