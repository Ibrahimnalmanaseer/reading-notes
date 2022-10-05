## Whiteboarding + Big O

Big O notation is a way to evaluate the algorithms based on their performance and the execution time required or the space, there are three types of big O (O(1), O(N), O(N²), O(2^N))

### O(1)

describes an algorithm that will consistently execute at the same time (or space) regardless of the input data set size.

### O(N)

describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set, even the matching found in early iterations of the Big O will 
will take the maximum iteration that the algorithm will take to complete the whole iteration.

### O(N²)

describes the algorithms that use nested iterations that square the size of the input data set, Deeper nested iterations will result in O(N³), O(N⁴), etc.

### O(2^N)

describes the algorithm whose growth doubles with each addition to the input data set, An example of an O(2^N) function is the recursive calculation of Fibonacci numbers.

### logarithm 
describes an algorithm using binary search, It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match, it will return success. If the target value is higher than the value of the probe element, it will take the upper half of the data set and perform the same operation against it.

