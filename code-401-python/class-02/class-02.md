# TDD with Python

## Unit tests :

### are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want

## TDD :

###  Test-Driven Development is a strategy to think (and write!) tests first

#### A convention widely used is the AAA: Arrange, Act and Assert.
- Arrange: you need to organize the data needed to execute that piece of code (input);

- Act: here you will execute the code being tested (exercise the behaviour);

- Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

### TDD: the cycle
- 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

- ✅ Write the feature and make the test pass! (you can dance after that)
 
- 🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

### Benifits of TDD

- The greatest advantage about TDD is to craft the  software design first

- Your code will be more reliable: after a change you can run your tests and be in peace

- Beginning may be hard — and that’s fine. You just need to practice!

## What does the if __name__ == “__main__”: do?

### A module: 
#### is a file containing Python definitions and statements. The file name is the module name with the suffix .py appended. 

**If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable.**

### Why Do we need it?

- Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.
- If you import this script as a module in another script, the __name__ is set to the name of the script/module.
- Python files can act as either reusable modules, or as standalone programs.
- if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.

## What is Recursion? 

### The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called a recursive function. 

## Need of Recursion

### we can reduce the length of our code and make it easier to read and write. It has certain advantages over the iteration technique 

### Properties of Recursion:

- Performing the same operations multiple times with different inputs.
- In every step, we try smaller inputs to make the problem smaller.
- Base condition is needed to stop the recursion otherwise infinite loop will occur.

#### How are recursive functions stored in memory?

- Recursion uses more memory, because the recursive function adds to the stack with each recursive call, and keeps the values there until the call is finished. The recursive function uses LIFO (LAST IN FIRST OUT) Structure just like the stack data structure

#### How a particular problem is solved using recursion? 

- The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion.

#### What is the difference between direct and indirect recursion? 

- A function fun is called direct recursive if it calls the same function fun.

- A function fun is called indirect recursive if it calls another function .

>//
 An example of direct recursion
 void directRecFun()
 {
    // Some code....

    directRecFun();

    // Some code...
 > }

>// An example of indirect recursion
>void indirectRecFun1()
 > {
    // Some code...

    indirectRecFun2();

    // Some code...
 > }
> void indirectRecFun2()
 > {
   > // Some code...

    indirectRecFun1();

    // Some code...
 > }

### What are the disadvantages of recursive programming over iterative programming? 

##### The recursive program has greater space requirements than the iterative program as all functions will remain in the stack until the base case is reached. It also has greater time requirements because of function calls and returns overhead.


#### Summary of Recursion:

- There are two types of cases in recursion i.e. recursive case and a base case.

- The base case is used to terminate the recursive function when the case turns out to be true.

- Each recursive call makes a new copy of that method in the stack memory.

- Infinite recursion may lead to running out of stack memory.

- Examples of Recursive algorithms: Merge Sort, Quick Sort, Tower of Hanoi, Fibonacci Series, Factorial Problem, etc.




