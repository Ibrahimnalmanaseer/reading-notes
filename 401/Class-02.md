## Testing and Modules

### Unit Test and TDD

unit test is writing code to exercise the input, the output, and code behavior.

In another way the TDD is a strategy to think and write tests:

- Baby Steps:
 Do the smallest test on the feature by inserting input and return output, in order to achieve it we should know what to test and what is expected,
the test file should follow the same name as the module name.
Another thing to care about is the structure. A convention widely used is the AAA: Arrange, Act and Assert.
   - Arrange: organize the input data;
   - Act: exercise the behavior and execute the code.
   - Assert: check if the output is the same as you were expecting.

- The Cycle
  The cycle is made in three steps:

    🆘 Write a unit test and make it fail.
    
    ✅ Write the feature and make the test pass.
    
    🔵 Refactor the code

- - -

### What does the if __name__ == “__main__”: do ?

python interpreter always read the source of the file before executed, and defines special variables and global variables, one of those variables is`__name__` having `__main__` value in case executed the code on the same file, if the file imported from another module, the `__name__` will be set to the module's name not the same value of `__main__`.

#### Advantages : 

- Every Python module has its __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
- If you import this script as a module in another script, the __name__ is set to the name of the script/module.
- Python files can act as either reusable modules or as standalone programs.
- if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.



- - - 

### Recursion – Data Structure and Algorithm

kind of function where called itself directly or indirectly, as the problems can be solved quite easily, A recursive function solves a particular problem (The Factorial of a number)by calling a copy of itself and solving smaller subproblems of the original problems.

the recursive functions use LIFO (LAST IN FIRST OUT) structure, 




