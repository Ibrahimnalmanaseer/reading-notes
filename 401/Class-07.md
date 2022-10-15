# Data Analysis 

## Jupyter Lab 

 Interactive development environment for notebooks, code, and data,
 allows users to configure and arrange workflows in data science, scientific computing, and machine learning.
 
 ### ex:
- Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, for example.

- Kernel-backed documents enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.

- Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

- Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers. For example, it is easy to have live preview of Markdown, Delimiter-separated Values, or Vega/Vega-Lite documents.


- - - - 

## Numpy 

Data Analysis Package used in Python, speed up the workflow and interface mainly used to interact and minpiolate Data .


### Numpy 2-Dimensional Arrays

2-dimensional array is known as a matrix, A matrix has rows and columns, By specifying a row number and a column number, we’re able to extract an element from a matrix.

### Creating A NumPy Array

We can create a NumPy array using the numpy.array function
#### ex:

- Import the numpy package.
- Pass the list of lists wines into the array function, which converts it into a NumPy array.
   - Exclude the header row with list slicing.
   - Specify the keyword argument dtype to make sure each element is converted to a float. We’ll dive more into what the dtype is later on.

```
import csv
with open("winequality-red.csv", 'r') as f:
    wines = list(csv.reader(f, delimiter=";"))
import numpy as np
wines = np.array(wines[1:], dtype=np.float)
```

and we will get :

```
array([[ 7.4 , 0.7 , 0. , ..., 0.56 , 9.4 , 5. ],
[ 7.8 , 0.88 , 0. , ..., 0.68 , 9.8 , 5. ],
[ 7.8 , 0.76 , 0.04 , ..., 0.65 , 9.8 , 5. ],
...,
[ 6.3 , 0.51 , 0.13 , ..., 0.75 , 11. , 6. ],
[ 5.9 , 0.645, 0.12 , ..., 0.71 , 10.2 , 5. ],
[ 6. , 0.31 , 0.47 , ..., 0.66 , 11. , 6. ]])
```






