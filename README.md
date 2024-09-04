# Zoleta_Exp-2

## Normalization Problem
  
  
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

## Divisble by 3 Problem
  
 
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
