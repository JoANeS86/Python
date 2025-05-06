

<ins>Library (or package)</ins>: Broadley refers to a reusable collection of code.

    In Python, a library is a broader term referring to a collection of modules and/or packages designed to provide specific
    functionality, while a package is a directory containing modules and an __init__.py file, used to organize related code.
    Libraries are often composed of multiple packages and can be thought of as a larger, reusable unit of code.
    
    Here's a more detailed breakdown:
    
      Modules: A single Python file containing code (functions, classes, variables). 
      Packages: A directory containing modules and an __init__.py file, serving as a namespace for those modules. 
      Libraries: A broad term for collections of modules or packages that offer a particular set of functionalities, like NumPy
      for numerical computing or Requests for HTTP requests. 

<ins>NumPy (or Numerical Python)</ins>: An essential library that contains multidimensional array and matrix data structures
and functions to manipulate them.

<ins>Pandas (Python Data Analysis)</ins>: A powerful library built on top of NumPy that's used to manipulate and analyze
tabular data.

<ins>Module</ins>: A simple Python file containing a collection of functions and global variables (Modules are accessed from
within a package or a library).

    Modules are used to organize functions, classes, and other data in a structured way. Internally, modules are set up through
    separate files that contain these necessary classes and functions. When you import a module, you are using pre-written code
    components. Each module is an executable file that can be added to your scripts. Commonly used modules for data professional
    work are math and random.

<ins>Global Variables</ins>: Variables that can be accessed from anywhere in a program or script.

## NumPy

NumPy's power comes from vectorization: Vectorization enables operations to be performed on multiple components of a data object
at the same time.

The array (*N-dimensional array*, or *ndarray* for short) is the core data structure of NumPy. To create an array,
first I have to import NumPy, then the standard practice is to alias the array as np.

If I use the type() function on an array, it'll return NumPy array, so if I want to check the data type of the contents of an array,
then I'll use the NumPy attribute dtype().

Another NumPy attributes and methods are:

    shape: A NumPy attribute used to check the shape of an array.
    ndim: A NumPy attribute used to check the number of dimensions of an array.
    reshape(): NumPy method used to change the shape of an array.






