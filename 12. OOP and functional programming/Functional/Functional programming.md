A programming paradigm is a style of programming. Different types of problem need to be tackled in different ways.

A functional program describes a series of functions. Each function takes in some data as arguments and returns an output. Functional programming has a lot in common with mathematics.

The domain is a set from which the function's input values are chosen. The co-domain is a set from which the function's output values are chosen. A function is mapping from a set of inputs, called the domain, to a set of possible outputs, known as the co-domain.

Using one function as an argument of another is called composition of functions.

Functions are first class objects. First class objects may appear in expressions, be assigned to a variable, be assigned as an argument and can be returned in a function call.

Functional programming is not totally different from other paradigms, which also use functions. However there are important differences, particularly in things which do not happen in functional programming.

Variables in functional programming are immutable and the program is stateless.

The only thing a function can do is calculate something and return a result, and it is said to have no side effects. A consequence of not being able to change the value of an object is that every time a function is called with the same parameters it will always return the same result.
A simple function can be proved to be correct and then used to build more complex functions

A function is a higher-order function if it takes a function as an argument or returns a function as a result or does both.

## The map function
Map is a higher-order function that takes a list and the function to be applied to the elements in the list as inputs, and returns a list made by applying the function to each element of the old list.

A list is a collection of elements which can be written in square brackets.

## The filter function
Filter is another higher-order function which takes a predicate (to define a Boolean condition) and a list. It returns the elements within the list that satisfy the Boolean condition.

## Fold (reduce function)
