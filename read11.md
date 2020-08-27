
# JupyterLab

* JupyterLab is a next-generation web-based user interface for Project Jupyter.It enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner.

* You can arrange multiple documents and activities side by side in the work area using tabs and splitters. Documents and activities integrate with each other, enabling new workflows for interactive computing.

* Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

* JupyterLab also offers a unified model for viewing and handling data formats. JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats.

# NumPy 
* NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem.
* Using NumPy To Read In Files
It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the `numpy.genfromtxt function`. 

### NumPy Data Types
 * NumPy array can store elements of a single data type. 
 * NumPy stores values using its own data types, which are distinct from Python types like float and str. This is because the core of NumPy is written in a programming language called C, which stores data differently than the Python data types. NumPy data types map between Python and C, allowing us to use NumPy arrays without any conversion hitches.

*You can find the data type of a NumPy array by accessing the dtype property:
```
thing.dtype

```
### NumPy has several different data types, which mostly map to Python data types, like float, and str. here are a few important ones:

- float — numeric floating point data.
- int — integer data.
- string — character data.
- object — Python objects.

