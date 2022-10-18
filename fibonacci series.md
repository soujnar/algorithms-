#Iterative
Procedure I_Fibonacci(n):
    int f0, f1, fib
    f0 = 0
    f1 = 1
    display f0, f1
    for int i := 1 to n:
        fib := f0 + f1   
        f0 := f1
        f1 := fib
        display fib
    END for loop
END Iterative_Fibonacci

#Recursive
Procedure R_Fibonacci(n)
    int f0, f1
    f0 := 0
    f1 := 1
    if(n <= 1):
        return n
    return Recursive_Fibonacci(n-1) + Recursive_Fibonacci(n-2)
END Recursive_Fibonacci
