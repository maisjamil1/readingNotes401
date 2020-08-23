## Python Scope & the LEGB Rule: Resolving Names in Your Code
global 
nonlocal

The concept of scope rules how variables and names are looked up in your code. It determines the visibility of a variable within the code. The scope of a name or variable depends on the place in your code where you create that variable. The Python scope concept is generally presented using a rule known as the LEGB rule.


## Python Scope vs Namespace
In Python, the concept of scope is closely related to the concept of the namespace. As you’ve learned so far, a Python scope determines where in your program a name is visible. Python scopes are implemented as dictionaries that map names to objects. These dictionaries are commonly called namespaces. These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called .__dict__.

Names at the top level of a module are stored in the module’s namespace. In other words, they’re stored in the module’s .__dict__ attribute. 
```
import sys
>>> sys.__dict__.keys()
dict_keys(['__name__', '__doc__', '__package__',..., 'argv', 'ps1', 'ps2'])

```
suppose that you need to use the name ps1, which is defined in sys. If you know how .__dict__ and namespaces work in Python, then you can reference ps1 in at least two different ways:
```
>>> sys.ps1
>>> sys.__dict__['ps1']
```
 ## LEGB 
 stand for Local, Enclosing, Global, and Built-in scopes.
 
## Global scope: 
The names that you define in this scope are available to all your code.

## Local scope:
The names that you define in this scope are only available or visible to the code within the scope.
