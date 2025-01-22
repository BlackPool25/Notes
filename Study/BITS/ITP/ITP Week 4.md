**Summary: Functions in C Programming**

### What Are Functions?

Functions in C programming are self-contained program segments that carry out specific tasks. They process information passed to them from the calling portion of a program and return a single value.

### Key Characteristics of Functions

* A named body of code
* Can accept arguments (inputs) and/or return values
* Can be called multiple times with different inputs

### Role of Functions in C Programs

Functions are useful for making code modular, reusable, and maintainable. They allow tasks to be assigned to separate functions, reducing repetition and increasing efficiency.

### Advantages of Using Functions

* Code reusability: the same function can be called multiple times with different inputs
* Modularity: tasks are separated into smaller, manageable pieces
* Easier maintenance: changes made to a function do not affect other parts of the program

**Example**

A simple example of using functions is demonstrated in the video. Two functions, `sum` and `main`, are shown:

```c
// sum() function takes two integer values as parameters,
// computes their sum, stores it in 'total', and returns 'total'
int sum(int x, int y) {
    return x + y;
}

// main() function calls the sum() function twice with different inputs
int main() {
    int set = sum(10, 50);
    // ...
}
```

In this example, the `sum` function is reusable and can be called multiple times with different inputs. The `main` function benefits from modularity and reusability, making it easier to maintain the program.

**Function Declaration and Definition in C**

### Introduction

Functions are an essential part of any programming language, including C. In this section, we will discuss two crucial concepts: function declaration and function definition.

### Function Declaration

A **function declaration** is a statement that declares the existence of a function without providing its implementation details. It provides information about the return type, name, and parameters of the function to the compiler.

#### Syntax
```c
return_type function_name(type1 arg1, type2 arg2 ...);
```
Here:

*   `return_type` is the data type of the value returned by the function.
*   `function_name` is a valid identifier for the function.
*   `type1`, `type2`, etc., are the types and names of the parameters (optional).

#### Key Points

*   Function declarations must appear before their definitions in a program.
*   They do not necessarily specify variable names for the parameters, although this is allowed.

### Function Definition

A **function definition** provides the implementation details of a function, including its body. It defines how to compute or manipulate data using input values (parameters).

#### Syntax
```c
return_type function_name(parameters) {
    // function body
}
```
Here:

*   `return_type` is the same as in the declaration.
*   `function_name` has a valid identifier name, unlike declarations which are optional.
*   `parameters` list contains comma-separated type and name pairs for each parameter (compulsory).
*   The function body is where actual computations or manipulations take place.

### Matching Function Declaration and Definition

When creating functions in C, it's essential to ensure that the **function declaration** matches the **function definition**. Specifically:

1.  The `name` of both declarations and definitions must be identical.
2.  The number of parameters (`type1 arg1`, ..., `typeN an`) in both should match exactly.
3.  For each parameter, its type (`typeX`) in both should also be the same.
4.  In function definition, variable names (not types) for parameters are optional but must exist.

Mis-matching any of these details can result in compilation errors or runtime issues.

**Function Invocation in C**

This section provides an overview of calling functions in C, including syntax, parameters, and return types.

### Function Syntax

To call a function, follow these steps:

1.  **Match the name**: Ensure that the name of the function matches between its declaration and definition.
2.  **Number of arguments**: The number of arguments passed to the function must match with the number of parameters in its definition.
3.  **Type matching**: The types of each argument must match with their corresponding parameter types.

### Example Function Calls

Here are three examples:

*   `sum(a, b)`: Passes variables `a` and `b` as arguments to the function `sum`.
*   `sum((a + b), (c + d))`: Passes expressions `(a + b)` and `(c + d)` as arguments.
*   `sum(10, 20)`: Calls the function with integer literals.

### Function Definition

A complete definition of a function includes:

1.  **Name**: Matches between declaration and definition.
2.  **Return type**: Should match the return type used in function calls (e.g., `int`).
3.  **Parameter list**: Number of parameters should be consistent with function calls.

### Program Execution Flow

Here's an overview of how program execution proceeds when a function is called:

1.  **Main function starts**: The execution begins at the main function.
2.  **Variable declarations**: Variable `x`, `y`, and `z` are declared before calling `sum(x, y)`.
3.  **Function call executes**: Execution shifts to the function definition for `sum(x, y)` and assigns values to variables `a` and `b`.
4.  **Return value captures**: The return value of the function is captured into variable `total`, which is then returned.
5.  **Main program resumes execution**: After returning from the function call, execution continues at the next line in the main function.

### Flowchart:

Here's a simplified flowchart illustrating how functions are called and executed:

```markdown
      +-------------------+
      |    Main Function   |
      +-------------------+
                  |
                  |
+-----------------------------+
|          sum(x, y)         |
|  (1. Declare variables:  x, y, z)|
|  (2. Assign values to x and y)|
|  (3. Call function sum())     |
|--------------------------------->|
      +-------------------+       +---------------+
      |                     |       |             |
+---------------------------->|Sum Function]|[a = x;    |
                              |         b = y;    |
                             |             total = a+b  |
                            +---------------+       ++ Return to
                                                    main program
                                    ^                        execution point

```

By following these guidelines, you can ensure that function calls are correctly matched with their definitions and execute as intended.

**Pros and Cons of Using Functions in C**

This section highlights the benefits and drawbacks associated with employing functions in a C program.

### Pros:

*   **Modularity**: Increases code organization, separating tasks into distinct sub-functions.
*   **Reusability**: Allows for reusing code snippets across different parts of the program, reducing duplication.
*   **Time-saving**: Speeds up coding by avoiding redundant code writing and enables easier modification.
*   **Usability**: Enhances readability and maintainability through a more structured approach to programming.

### Cons:

*   **Performance overhead**: Functions require memory allocation for their local variables, adding an extra layer of complexity and potentially decreasing execution speed.

**Benefits of Using Functions**

1.  Encourages modular code organization
2.  Fosters reusability by allowing duplicate code blocks to be avoided

**Drawbacks of Using Functions**

*   Introduces additional overhead due to memory allocation for local variables

**Memory Allocation for Functions**

When a C program executes, its components, including functions and variables, occupy specific regions of **main memory (RAM)**.

### Main Memory Structure

*   The main memory is divided into smaller segments called **segments**, which contain executable code or data.
*   Each segment has multiple sections:
    *   Text Segment: Contains the machine-readable instructions for the program.
    *   Data Segment: Holds initialized global and static variables, as well as constant values.

### Function Memory Allocation

When a function is defined in C:

1.  The compiler allocates memory for the entire function's local variables, including parameters, stack space, and local storage.
2.  However, **stack allocation** is used to store these variables within each segment of RAM that holds executable code or data.

### Example: `main()` and `sum()`

Consider a C program with two functions:

```c
int sum(int a, int b) {
    return a + b;
}

void main() {
    int x = 5;
    int y = 10;

    int result = sum(x, y);
}
```

*   In the `main()` function:
    *   The compiler allocates separate memory segments for variables `x` and `y`.
        *   These are stored in the **Data Segment**, which is allocated from main memory.
        + Within each segment (e.g., Data Segment), individual allocations occur, such as storage for variable values or local stack space.
    *   The `sum()` function:
        *   The compiler allocates a new segment of code containing instructions to calculate and return the sum result.
	### Visual Representation

Imagine viewing these segments in memory like this:

*   **Data Segment** (Segment 1): +---------------------------+ | x = 5 | +--------+---------| y = 10 | +--------+---------+ |
    *   Within each segment:
        - Variable storage and local stack space
*   **Code Segment** (Segment 2) for `sum()` function: 
    ```assembly code```
    ```
int sum(int a, int b)
{
return a + b;
}
```

By examining this memory allocation diagram:

1.  Understand how functions occupy specific regions in main memory.
2.  Recognize the separate segments allocated to executable code (text) and variables/data.

**Understanding Function Memory Allocation Enhances Code Development**

A deeper grasp of these fundamental concepts helps you:

*   Optimize your program's performance by managing data allocation effectively
*   Troubleshoot issues related to function calls or variable access in different memory regions
```


**Computing Factorial Using Functions**

The following C code demonstrates how to write a program to calculate the factorial of a given number `n` using two separate functions: `fact()` and `main()`. The code is well-structured, easy to follow, and utilizes standard input/output operations.

### Code Overview

1.  **Function Declaration**: The first step was declaring the function `int fact(int n)` with its parameters.
2.  **Function Definition**: This function has a body that computes the factorial of `n` using a while loop and returns it as an integer value.
3.  **Main Function**: Inside the `main()` function, user input is captured in variable `n`. The program calls the previously declared `fact()` function with parameter `n`, stores its return value (factorial) in another variable, and prints the factorial.

### Compilation and Execution

The C code was successfully compiled using GCC without any errors. This resulted in a new executable file named "a.out". When executed, it prompted users to enter their desired input for `n`. The output would be displayed as expected:

*   For example, when given an input of `-5`, the program correctly computed and printed the factorial value as `120`.
*   Similarly, with an input of `10`, the program produced and presented the correct result (`3628800`).

### Key Points

1.  **Function Declaration**: The first step in defining a function is to declare its name along with its return type and parameter list.
2.  **Variable Initialization**: A variable like `temp` should be initialized before use, ensuring that it holds an initial value (in this case, one) for the computation of factorial.
3.  **Main Function Structure**:
    *   User input is captured using standard I/O functions (`scanf()`).
    *   The computed result is stored in a separate variable to return from the main function.

Overall, the provided C code demonstrates efficient and effective ways to implement a program that computes factorials for given inputs.

Here's the code written in C based on the provided specification:

```c
#include <stdio.h>

void isPrime(int n) {
    int i;
    int notPrimeFlag = 0;

    for (i = 2; i <= n - 1; i++) {
        if (n % i == 0) {
            notPrimeFlag = 1;
            break;
        }
    }

    if (notPrimeFlag == 1) {
        printf("%d is not a prime number\n", n);
    } else {
        printf("%d is a prime number\n", n);
    }
}

int main() {
    int n;

    printf("Enter a number for primality testing: ");
    scanf("%d", &n);

    isPrime(n);

    return 0;
}
```

This code implements the `isPrime` function and the `main` function as described in the specification. It checks whether a given input number is prime or not, using a simple trial division method to test for divisibility by numbers from 2 up to but not including `n`. If any divisor is found, it prints that the number is not prime; otherwise, it prints that the number is prime. The program then returns 0 from the `main` function without returning anything else.

Here's an explanation of the code you provided:

**What is Storage Class of Variables?**

In C programming language, the storage class of a variable determines its scope, lifetime, default value, and memory location.

The four main storage classes are:
1.  **Auto**: These variables have automatic storage duration that ends when they go out of scope.
2.  **Static**: These variables have static storage duration throughout their entire execution in the program.
3.  **Global**: Global or External Variables store data across different source files and can be accessed from anywhere within a program using their declared name.
4.  The Storage class also determines the way compiler allocates memory for that variable.

**Variables Scope**

In your code snippet, we see four variables:

1.  `x` and `c`: They have limited scope to function `f1`.
2.  `b`: It has a limited scope within two braces.
3.  The main global Variable (`y`): This has the widest accessibility.

**Printing Statement Error**

When you try to print variable `b`, it leads to an error because `b` is only accessible in its local scope and not outside those scopes, unless declared as global or static (depending on storage class).

```c
int main() {
    int b; // declare here

    printf("%d", b);  // valid since 'b' has been initialized before use.

    return 0;
}
```

In the function `f1`:

```cpp
void f1(int a) {   // function parameter is declared first
    static int x = 10; // global/static variable declaration, not within local scope.
    printf("%d", b);     // valid since 'b' has been initialized before use.

}
```

**Memory Allocation**

Variables with the storage class of auto or register are allocated memory on the stack. Global variables and those declared static have their own space in the program.

```c
int main() {
    int a = 5;      // local variable declaration, which is only accessible within main.
                 // Memory allocation happens when 'a' gets initialized to value=5 (on the Stack).

    void f1(int b) { // function parameter is declared first
        static x = 10;   // global/static variable declaration, not within local scope.

    }

}
```

Let me know if you need any further clarification.


**Memory Layout of a C Program**

A C program consists of multiple segments stored in memory when executed.

### Segments Present in Memory Allocated to a Specific Program

There are four main segments:

1.  **Stack Segment**
    *   Stores memory allocated for functions and variables declared inside functions.
2.  **Heap Segment**
    *   Stores dynamically allocated memory (not covered in this video).
3.  **Data Segment**
    *   Holds global variables and static variables.
4.  **Text Segment** or Code Segment
    *   Contains the machine code that makes up the program's instructions.

### Purpose of Each Segment

*   The stack segment is used for local storage, allowing functions to store their own data without affecting other parts of the program.
*   The heap segment provides memory allocation at runtime, enabling programs to grow or shrink dynamically as needed.
*   The data segment stores initialized global and static variables.
*   The text segment contains the compiled code that makes up the program's instructions.

**Key Takeaways**

*   Each segment in a C program has its own specific use case:
    *   Stack: Local storage for functions
    *   Heap: Dynamic memory allocation at runtime
    *   Data: Global and static variables
    *   Text/Code Segment: Compiled machine code

**Summary: Auto and Global Variables in C**

### **Auto Variables**

*   Declared within a code block, also known as local variables
*   Have scope limited to the block where they are declared
*   Stored on the stack segment, specific to each function where they are declared
*   Lifetime is until the execution of the block finishes
*   Initial value before instantiation is a garbage value

### **Global Variables**

*   Declared outside all blocks and functions
*   Have scope accessible to all functions
*   Stored in data segment portion of memory
*   Lifetime is throughout program execution
*   Initial value before initialization is zero, unlike local variables which are garbage values

**Key Takeaways:**

|  | Auto Variables | Global Variables |
| --- | --- | --- |
| **Scope** | Limited to the block where declared | Accessible to all functions |
| **Storage** | Stack segment, specific function scope | Data segment portion of memory |
| **Lifetime** | Until execution finishes within that block (stack) or program completion (data)  | Throughout program execution (data) |

### Example Program Output:

*   The global variable `a` with value 0 is accessed first in the main function when calling f1.
*   Then, a local variable `a` with value 2 is declared and used inside f1.
*   After that, another local variable `a` with value 5 is defined and used in the main function.

**Memory Allocation:**

*   Stack segment: Space allocated for each frame (stack frame) of functions like main and f1. Local variables are stored here.
*   Data segment portion of memory: Global variables reside here, including those declared outside all blocks and functions.

This summary highlights the key differences between auto and global variables in C programming, covering their scope, storage locations, lifetime, initial values, and how they interact with each other during program execution.

**Summary of Static Variables in C**

### What are Static Variables?

* **Definition**: A variable declared using the keyword `static`.
* **Scope**: Visible only to the function or block where it is defined.
* **Initial Value**: Always initialized to zero.

### Characteristics of Static Variables

* Stored in the data segment portion of memory.
* Lifetime extends until program termination, retaining assigned values.
* All static variables are initialized only once.
* Can retain values between function calls and iterations.

### Example Use Cases

1. **Initializing Variables**: Assigning a value to `static` variable within a loop ensures that it retains its value across iterations.
2. **Retaining Values Between Function Calls**: Using `static` variables in functions can preserve their values between subsequent function calls, unlike local variables which are reinitialized on each call.

### Memory Storage

* Static variables reside in the data segment of memory, even though defined within a function or block.
* Local variables and other stack-based storage elements (like `auto` variable) occupy space in the stack frames allocated to functions.

**Summary of Module**

In this module, we covered several key topics related to Functions in C:

*   **Modular Programming**: We learned how functions enable modular programming by allowing us to break down a complex task into smaller, independent modules.
*   **Function Declaration and Definition**: We discussed the syntax for declaring and defining functions, including parameter handling, return values, and function scope.
*   **Parameter Handling**: We explored how functions can accept data as parameters and how they can return computed values.
*   **Storage Classes of Variables**: We examined different storage classes in C (auto, static, extern, register) to understand where variables are stored in program memory.

By mastering these concepts, you should be able to write more efficient, reusable, and maintainable code using functions in C.