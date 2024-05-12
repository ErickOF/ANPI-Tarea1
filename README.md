# **CE3102 - Numerical Analysis for Engineering - Homework 1**

* **University:** Instituto Tecnológico de Costa Rica (Costa Rica Institute of Technology)
* **Career:** Computer Engineering
* **Course:** CE-3102: Numerical Analysis for Engineering
* **Period:**  Semester II - 2019


## **Activity: Development of computational packages in GNU Octave and Python to solve nonlinear equations using iterative methods**

### **General Information**
* This task consists of developing two computational packages, one in GNU Octave and the other in Python.

* Each computational package contains the implementation of a set of functions. Each function represents an iterative method for approximating a solution to a nonlinear equation of the form $f(x) = 0$.

* Each group must investigate 12 iterative methods that approximate a solution of the equation $f(x) = 0$, of which 6 methods must include in their formula **the calculation of the derivative** of the function $f$, and the other 6 methods **must not include the calculation of no derivative**.


### **About Iterative Methods**
Each method must be implemented as a function containing the following initial parameters:

1. $f$, which is a text that represents the function $f(x)$. **Note:** If the syntax of the function f is incorrect, then the implemented function must generate a warning.

2. Initial values ($x_0$, $x_1$, ...) needed for the iterative method to work.

3. Tolerance $tol > 0$, which will determine the stopping criterion of each iterative method. The stopping criterion will be defined by $|f(x_k)| < tol$, where $x_k$ is the k-th iteration that approximates the root of the equation $f(x) = 0$.

4. Graph *graf*, which is a number. This parameter will allow you to display the graph of iterations ($k$) versus errors ($|f(x_k)|$) of the iterative method. If *graf* $= 0$, then it will not show the graph. If *graf* $= 1$ or the *graf* parameter is omitted, then it will display the graph. In any other case, the function must generate a warning

The function must return the following:

1. $x_{aprox}$, which is the approximation to the solution of the equation $f(x) = 0$.

2. *iter*, which represents the number of iterations that were used to approximate the zero of the function with a tolerance *tol*.

3. If *graf* $= 1$ or the *graf* parameter is omitted, then it will display the graph of iterations ($k$) versus errors ($|f(xk)|$) of the iterative method. Each graph must have a title, and the axes must be labelled.

Each implemented iterative method must stop if the respective denominator is zero in any of the iterations (to avoid division by zero). In this case, the method shows the results obtained up to that point.


### **About Computational Packages**
*  The name of each package must be **SolNE** (solving nonlinear equations).

* **In GNU Octave:** To create the computer package, use the information found at the following link: https://docs.octave.org/latest/Creating-Packages.html. The function names of the selected methods must have the following structure:
    * *sne_ud_#*, if it is a method that includes the calculation of derivatives (solving nonlinear equations - using derivative).
    * sne_fd_#*, if it is a method that does not include the calculation of derivatives (solving nonlinear equations - free derivative).

* **Python package:** To create each computational package, use the information found in the following link: https://docs.python.org/3/tutorial/modules.html. The package must contain the following 2 files:
    * *ud.py*, which contains the 6 functions of the iterative methods that include the calculation of derivatives. The name structure of such functions must be $sne$ ud #.
    * *fd.py*, which contains the 6 functions of the iterative methods that do not include the calculation of derivatives. The name structure of such functions must be $sne$ fd #.

* In both packages, the # symbol must be changed to 1, 2, 3, 4, 5, and 6, to list each of the methods.

* Each function implemented in GNU Octave and Python must have its helper. This help must indicate what the function consists of, which are the initial parameters and which are the output parameters.

* For each computer package, a user manual must be developed, which must be in LaTeX. The user manual must contain the following:

    * Cover with the package name, name of the TEC, name of the course, and the name of the group members.
    * Table of Contents.
    * A section explaining what the computational package consists of.
    * A section that explains how to install the computer package and what requirements are needed for its use.
    * A section explaining the use of the implemented functions, with illustrative examples. This section should contain everything necessary to know how to use the implemented functions.
    * Bibliographical references.

The structure of the manuals can be based on the manual developed for the Python package NumPy.
