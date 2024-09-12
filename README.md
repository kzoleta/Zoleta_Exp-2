# Zoleta_Exp-2

## Numerical Python (NUMPY)

## Instructions
Write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter
notebook in the dedicated submission bin.

## Problem 1:

**_NORMALIZATION PROBLEM:_**
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:

𝑍 =
𝑋 − 𝑥̅
𝜎

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.
In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy

#### Normalization Problem Code
  
  import numpy as np #Start of program

    X = np.random.rand(5, 5) #Create randomized array

    #Normalize array
    X_mean = X.mean()
    X_std = X.std()
    X_normalized = (X - X_mean) / X_std
    
    #Save normalized array
    np.save('X_normalized.npy', X_normalized)
    
    #Print
    print("Original Array X:\n", X)
    print("Mean of X:", X_mean)
    print("Standard Deviation of X:", X_std)
    print("Normalized Array X_normalized:\n", X_normalized)


## Problem 2:

**_DIVISBLE BY 3 PROBLEM:_**
Create the following 10x10 ndarray which are the squares of the first 100 positive integers. 
From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy

### Divisble by 3 Problem Code
  
  import numpy as np #Start of program
    
    #Create 10x10 array with the squares of <100 numbers
    A = np.arange(1, 101)**2
    A = A.reshape(10, 10)
    
    #Check elements that can be divided by 3
    div_by_3 = A[A % 3 == 0]
    
    #Save the result
    np.save('div_by_3.npy', div_by_3)
    
    #Print
    print("Array A (10x10 ndarray of squares):\n", A)
    print("Elements divisible by 3:\n", div_by_3)
