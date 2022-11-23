---
banner: "![[Pasted image 20220511002010.png]]"
banner_y: 0.45333
---

# Object Orientated Programming

 11/05/2022

- Object orientated programming allows for extensive planning leading for better designs.
- Each function is written and maintained independently of other objects.
- Software maintenance is easier due to the high modularity of it.

## Classes

### Classes Introduction

A class can be thought of as a blueprint or a master copy of a related group of items.
An object is an instance of a class.
Instantiation is the process of creating an object of the class.

### Constructers

A constructer is a special method which in OOP allows us to how objects are initialized. It grabs memory needed by an object when it is instantiated and initializes the attributes of the object it creates. constructers are not inherited

### Object Initialization

An object is an instance of a class, it requires memory for its data and mechanism for linking to the code for its methods. The code is shared with other methods belonging to the same class. Attribute data is not shared, each object maintains its own state.

### Inheritance

Inheritance allows a class to be derived from an existing class without the need to modify the existing class. The derived class has all the attributes and methods of the parent class, but adds new ones of its own.

A subclass inherits everything from the superclass (except constructors).
- You can define additional variables and methods
- You can override existing methods from the superclass
- You can access non-private members defined in the superclass
- You typically have to define constructors too
- Inheritance is an “is a” relationship

#### Polymorphism

Refers to a programming languages ability to process objects differently depending on their data type or class. A derived class may need to do more than just extend a class but may redefine so that it behaves differently to the base class.


> [!NOTE] Virtual
> A virtual method is defined in the base class using the key word Virtual but can be overridden by a method in the subclass.

> [!NOTE] Override
> Defining a method with the same name and formal argument types as a method from a superclass is called overriding and is achieved by using the key word override.

### Methods - Static, Virtual, Abstract

The class methods we have used so far are known as instance methods, these include:
Constructors (controls how objects are created prior to use)
Accessors (provides the means to obtain the state of an object)
Mutators (a method used to control changes to a variable)

Static methods are methods attached to a class itself and not any particular instance of the class.
Virtual methods are methods are those that can be overriden.
Abstract methods are methods that are empty but there to be overriden.

## Dry Running

Dry running algorithms helps to check bugs inside your code. Bugs may remain elusive even after compiled or with the operating system, hence the use of dry running.

## Recursive Algorithms

A recursive algorithm is an algorithm that calls upon itself inside the function.

> [!NOTE] A recursive routine has three essential characteristics:
> - A stopping condition or a ‘base case’ must be included which when met means that the routine will not call itself and start to “unwind”.
> - For input values other than the stopping condition, the routine must call itself.
> - The stopping condition must be reached after a finite number of calls.

Every time a sub routine is called the return address is put on the call stack. Even with a stopping condition, the recursive routine can only be called a limited number of times or the stack will overflow the maximum memory capacity.

### Factorials

$5! = 5 * 4 * 3 * 2 * 1$
5! is the shorthand way of expressing the product of numbers 1 to 5.
Factorials are also an easy example to show recursion:
![[Pasted image 20220511005154.png]]`center`

## Abstraction

Abstraction gives us the ability to engage a concept while ignoring some of the real life details ie a tube map. At a class level, the focus is on properties (attributes) and command/query operations.

### Abstraction by Generalisation

This is grouping by common characteristics to arrive at a hierarchical relationship of the “is a kind of” type arrived at by removing unnecessary details.

### Problem Abstraction

This is removing details until the problem reduces to one which has already been solved.

### Decomposition

Breaking a problem into a number of sub-problems, so that each sub-problem is a problem that can be solved.

### Procedural Abstraction

This is used to keep the actual values separate from the overall design. Ie procedures and passing parameters.

### Functional Abstraction

A function that is used to simplify problems ie sqrt of 3 instead of the actual decimal / how to work it out.

### Data Abstraction

The data or information that is relevant to solving a problem may be in the form of an abstract data structure such as an array, stack or queue.

## Encapsulation

Encapsulation is the grouping of data and methods together within the same object. This promotes the separation of the implementation and the interface. The methods (procedures and functions) act on the data within the object.

### Information Hiding

Information hiding is when the data within an object can only be accessed by the methods within that object. Code outside a class can only access the data through the defined methods. The parts exposed are called the class’s interface. The interface generally reveals little as possible about the inner workings of the class.

### Access Modifiers

Properties of a class are generally declared as private this is so that they cannot be accessed from outside the class. Methods can be declared as public, protected or private. These are the access modifiers that control the accessibility of types which includes classes, their methods and properties (members).
![[Pasted image 20220511012927.png]]`center`

## Relationships

In OOP objects can be related in different ways,

### Association

This is a “is a” relationship. Association in OOP is how two or more objects are related to each other, one to many. This case they are merely associated.

![[Pasted image 20220511013616.png]]`center`

### Association Aggregation

Aggregation is a way of creating new objects that contain objects which already exist. Association aggregation is when an object which contains other objects is destroyed, the other objects will still exist.

![[Pasted image 20220511014002.png]]`center`
Aggregation is sometimes called containment and a relationship between class/objects where one class is composed wholly or partly of other classes. It is a “has a” relationship

### Composition Aggregation

This is when an object that contains other objects and if destroyed, then the objects will no longer exist. In other words the child object cannot exist without the parent object, so the association is strong.
![[Pasted image 20220511014311.png]]`center`

## Pseudo Code

Pseudo code is a way of creating an algorithm for a given problem without worrying about the syntax or constructs of particular language. It still has a relatively structured approach, however, no specific coding rules are necessary. Once a a program has been designed in pseudo code it can be fairly easily converted into high level code.