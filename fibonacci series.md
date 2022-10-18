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
