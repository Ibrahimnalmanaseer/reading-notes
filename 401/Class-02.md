## Testing and Modules

### Unit Test and TDD

unit test is a writing code to excersize the input ,the output and code behavior .

on other way the TDD is a strategy to think and write tests:

- Baby Steps:
 Do a smallest test on the feature by insert input and return output,inoder to achieve it we should know what to test and what is excpecetd ,
the test file should follow the same name of module name.
Other thing to care about is the structure. A convention widely used is the AAA: Arrange, Act and Assert.
   - Arrange: orgnize the input data;
   - Act: excersize the behavior and sxcute the code.
   - Assert: check if the output is the same as you were expecting.

- The Cycle
  The cycle is made by three steps:

    🆘 Write a unit test and make it fail.
    
    ✅ Write the feature and make the test pass.
    
    🔵 Refactor the code

- - -

### What does the if __name__ == “__main__”: do ?

python interptor always read the sourse of file beofre excuted, and define special variables and global variables, one of those varibales is __name__ having same value of __main__ variable incase excuted the code on the same file , if the file imported from another module ,the __name__ will be set to the module's name not the same value of __main__.



