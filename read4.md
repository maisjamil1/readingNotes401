# Classes and Objects
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

Classes are created using the keyword class and an indented block, which contains class methods (which are functions).
Below is an example of a simple class and its objects.
```
class Cat:
  def __init__(self, color, legs):
    self.color = color
    self.legs = legs

felix = Cat("ginger", 4)
rover = Cat("dog-colored", 4)
stumpy = Cat("brown", 3)
```
The __init__ method is the most important method in a class.
This is called when an instance (object) of the class is created, using the class name as a function.

All methods must have self as their first parameter, although it isn't explicitly passed, Python adds the self argument to the list for you; you do not need to include it when you call the methods. Within a method definition, self refers to the instance calling the method.
_____________________________________________________________
# Thinking Recursively in Python

## A recursive function is a function defined in terms of itself via self-referential expressions.
This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

### As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision.
![](https://files.realpython.com/media/stack.9c4ba62929cf.gif)
### Behind the scenes, each recursive call adds a stack frame (containing its execution context) to the call stack until we reach the base case. Then, the stack begins to unwind as each call returns its results
