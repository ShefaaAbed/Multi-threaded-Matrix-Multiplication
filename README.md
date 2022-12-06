# Multi-threaded-Matrix-Multiplication

In src file you can find the codes.

This code is implement a multi-threaded matrix multiplication using C/C++.
The program will create T worker threads to perform the operation (T will be passed to the program with the Linux command line). Each of the threads needs to perform part of the total matrix multiplication operation.



These global variables: numOfOdd, numOfEven, and totalCells will be incremented by all the threads when a thread finds a cell in the output matrix. numOfOdd and numOfEven will be incremented when the output cell is odd or even, respectively. The variable “totalCells” will be incremented for each cell in the output matrix regardless of being odd/even. 



When any of the threads starts executing, it will print its number (0 to T-1), and then the range of loops that it is operating on from the total matrix multiplication problem. When all threads are done, the main thread will print the final values in the counter variables: numOfOdd, numOfEven, and totalCells.



The FirstVersion.cpp doesn’t consider race conditions, and the SecondVersion is thread-safe. The input will be provided in an input file (in.txt), and the output should be printed to an output file (out.txt).



The input will start with an integer number (N) representing the dimension of the input matrices (assume both matrices are square, with the same dimensions). This will be Followed by two NxN matrices representing the two input matrices A, and B.
