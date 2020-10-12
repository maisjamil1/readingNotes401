## What Are Dunder Methods?
In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:
```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
To fix this, you can add a __len__ dunder method to your class:

class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
Another example is slicing. You can implement a __getitem__ method which allows you to use Python’s list slicing syntax: obj[start:stop].
```
## Python Iterators
Iterators provide a sequence interface to Python objects that’s memory efficient and considered Pythonic. Behold the beauty of the for-in loop!
To support iteration an object needs to implement the iterator protocol by providing the __iter__ and __next__ dunder methods.
Class-based iterators are only one way to write iterable objects in Python. Also consider generators and generator expressions.
## Python Generators 
Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code needed when writing class-based iterators.
The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.
