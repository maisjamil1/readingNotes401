
# Python Modules and Packages
## Modular programming
refers to the process of breaking a large,  programming task into smaller, more manageable and modules. Individual modules can then be cobbled together like building blocks to create a larger application.

### advantages to modularizing code in a large application:

- Simplicity
- Maintainability
- Reusability
- Scoping: Modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program.

three different ways to define a module in Python:

- A module can be written in Python itself.
- A module can be written in C and loaded dynamically at run-time, like the re (regular expression) module.
- A built-in module is intrinsically contained in the interpreter, like the itertools module.

### A module’s  are accessed the same way in all three cases: with the import statement.
*import <module_name>
*from <module_name> import <name(s)>
### It is also possible to import individual objects but enter them into the local symbol table with alternate names:
*from <module_name> import <name> as <alt_name>
*import <module_name> as <alt_name>
  
  
  ______________________________________
  ### The dir() Function
The built-in function dir() returns a list of defined names in a namespace. Without arguments, it produces an alphabetically sorted list of names in the current local symbol table:
  ______________________________________

#### Modules are often designed with the capability to run as a standalone script for purposes of testing the functionality that is contained within the module. This is referred to as unit testing. 
  ______________________________________
### Reloading a Module
For reasons of efficiency, a module is only loaded once per interpreter session. 
```
>>> import mod
a = [100, 200, 300]

>>> import mod

>>> import importlib
>>> importlib.reload(mod)

a = [100, 200, 300]
```


# pytest
The pytest framework makes it easy to write small tests, yet scales to support complex functional testing for applications and libraries.

## Features
- Detailed info on failing assert statements (no need to remember self.assert* names);

- Auto-discovery of test modules and functions;

- Rich plugin architecture, with over 315+ external plugins and thriving community;



# Recursion

The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. 

What is base condition in recursion?
In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems.
![recursion](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Recursive-Functions-in-c.png)

