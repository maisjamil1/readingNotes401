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
 The LEGB rule is a kind of name lookup procedure, which determines the order in which Python looks up names. For example, if you reference a given name, then Python will look that name up sequentially in the local, enclosing, global, and built-in scope. If the name exists, then you’ll get the first occurrence of it. Otherwise, you’ll get an error.
 
### Global scope (or module): 
The names that you define in this scope are available to all your code.


### Local (or function) scope 
is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. 

### Enclosing (or nonlocal) scop
e is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

### Built-in scope
is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.
