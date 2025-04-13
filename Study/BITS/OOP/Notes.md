
**Subject:** _Week 1 – Introduction to Object-Oriented Programming (OOP) and Java Basics_

---

### **What Is Object-Oriented Programming (OOP)?**

- **OOP** is a programming paradigm based on the concept of **objects**, which encapsulate **attributes (data)** and **methods (functions)**.
    
- **Classes** act as **blueprints** for creating objects.
    
- In contrast to procedural programming, OOP combines data and behavior into a single unit.
    

---

### **Classes and Objects**

- **Class**: A template defining **structure (attributes)** and **behavior (methods)** of objects.
    
    - E.g., Class `Car` with attributes: `color`, `brand`, `speed`; methods: `start()`, `accelerate()`, `stop()`.
        
- **Object**: A specific instance of a class with unique attribute values.
    
    - Created using `new`, e.g., `Car myCar = new Car();`
        

---

### **Constructor**

- A **special method** with the same name as the class, used to **initialize objects**.
    
- **Called automatically** when an object is created.
    
- Can accept **parameters** to set initial values.
    

---

### **Four Pillars of OOP**

1. **Abstraction**
    
    - Simplifies complex systems by hiding non-essential details.
        
    - Achieved using **abstract classes** and **interfaces**.
        
    - **Abstract method**: Defined in abstract class without implementation.
        
    - **Interface**: A contract of method signatures that implementing classes must define.
        
2. **Encapsulation**
    
    - Combines **data and methods** into a **single unit (class)**.
        
    - **Private attributes** restrict direct access; use **getter/setter methods** for interaction.
        
3. **Inheritance**
    
    - Allows a **subclass** to acquire properties/methods from a **superclass** using `extends`.
        
    - Supports **code reuse** and **hierarchical relationships**.
        
4. **Polymorphism**
    
    - One interface, multiple implementations.
        
    - Achieved via:
        
        - **Method Overloading**: Same method name, different parameters (compile-time).
            
        - **Method Overriding**: Subclass redefines superclass method (runtime).
            

---

### **Types of Inheritance in Java**

1. **Single Inheritance** – One child inherits from one parent.
    
2. **Multilevel Inheritance** – A class inherits from a subclass of another class.
    
3. **Hierarchical Inheritance** – Multiple subclasses inherit from a single superclass.
    
4. **Multiple Inheritance** – Achieved using **interfaces** only, not classes.
    

---

### **super Keyword**

- Refers to the **parent class**.
    
- Used to access:
    
    - **Superclass constructor**.
        
    - **Superclass methods** (e.g., `super.sound()` in overridden method).
        

---

### **Java Programming Basics**

- Java program = **one or more classes** with methods.
    
- **main()** method: Entry point of a Java application.
    
- E.g., `System.out.println("Hello, World!");` outputs to console.
    

---

### **Primitive Data Types in Java**

- **int**: Integer values (e.g., `int age = 25;`)
    
- **double**: Floating-point numbers (e.g., `double pi = 3.14;`)
    
- **boolean**: Logical values `true` or `false`
    
- **char**: Single character (e.g., `char grade = 'A';`)
    
- Other numeric types: **byte**, **short**, **long**, **float**
    

---

### **Variables and Scope**

1. **Local Variables** – Declared inside methods; limited scope.
    
2. **Instance Variables** – Defined in a class; different for each object.
    
3. **Class (Static) Variables** – Shared across all instances; defined with `static`.
    

---

### **Type Promotion & Type Casting**

- **Type Promotion**: Automatic conversion to a larger type during operations.
    
- **Type Casting**: Manual conversion, e.g., casting double to int truncates decimals.
    

---

### **Operators in Java**

- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
    
- **Assignment**: `=`, `+=`, `-=`, etc.
    
- **Comparison**: `==`, `!=`, `<`, `>`, `<=`, `>=`
    
- **Logical**: `&&`, `||`, `!`
    
- **Increment/Decrement**: `++`, `--`
    
- **Bitwise**: `&`, `|`, `^`, `~`, `<<`, `>>`, `>>>`
    

---

### **Control Statements**

- **if**: Executes block if condition is true.
    
- **if-else**: Executes one of two blocks based on condition.
    
- **switch**: Chooses block based on value match.
    
- **Loops**:
    
    - **for**: Repeats block for a set number of times.
        
    - **while**: Repeats while condition is true (checked before loop).
        
    - **do-while**: Executes block at least once (condition checked after).
        

---

[End of Notes, Message #1]

**Subject:** _Week 2 – Java Classes, Objects, Variables, and User Input_

---

### **Java Classes and Objects**

- A **class** is a blueprint defining **attributes (instance variables)** and **behaviors (methods)** of objects.
    
- An **object** is an instance of a class with its own values for the attributes defined by the class.
    

---

### **Defining Classes in Java**

- **Syntax Elements:**
    
    - **Access Modifier**: Controls visibility (`public`, `protected`, `default`, `private`).
        
    - **class keyword**: Used to define a class.
        
    - **ClassName**: Must follow naming conventions (CamelCase, starts with uppercase).
        
    - **Instance Variables**: Represent the state of the object.
        
    - **Constructors**: Special methods to initialize objects.
        
    - **Methods**: Define actions the object can perform.
        

---

### **Access Modifiers**

1. **public** – Accessible from any class.
    
2. **private** – Accessible only within the same class.
    
3. **protected** – Accessible within the same package and subclasses.
    
4. **default (no modifier)** – Accessible only within the same package.
    

- **Purpose**: Controls access, enforces **encapsulation**, enhances **modularity** and **security**.
    

---

### **Constructors in Java**

- **Definition**: Special method, same name as class, no return type.
    
- **Automatic Invocation**: Called automatically when object is created using `new`.
    
- **Parameterization**: May accept parameters for custom initialization.
    

#### **Types of Constructors**

1. **Default Constructor**
    
    - No parameters.
        
    - Provided automatically by compiler if none is defined.
        
    - Performs default initialization.
        
2. **Parameterized Constructor**
    
    - Accepts parameters to assign custom values to instance variables.
        
3. **Copy Constructor**
    
    - Accepts another object of the same class.
        
    - Copies attribute values from the given object to a new one.
        

---

### **Instance Fields, Methods, and Variables**

- **Instance Fields**: Declared in a class (outside methods); each object gets its own copy.
    
- **Methods**: Define object behavior, can manipulate instance fields.
    
- **Variables**:
    
    - **Local Variables**: Declared inside methods or blocks, exist only within scope.
        

---

### **Accessing Instance Members**

- Use **dot notation** with the object reference:
    
    - `objectName.fieldName`
        
    - `objectName.methodName(arguments)`
        

---

### **Class vs. Instance Variables**

- **Class Variables (Static)**
    
    - Declared using `static`.
        
    - Belong to the class, shared by all objects.
        
    - Accessed via class name (e.g., `ClassName.variableName`).
        
- **Instance Variables**
    
    - Unique to each object.
        
    - Accessed using object references.
        

#### **Key Differences**

- **Memory**: Class – shared memory; Instance – separate memory per object.
    
- **Access**: Class – via class name; Instance – via object.
    
- **Scope**: Class – global to all instances; Instance – local to object.
    
- **Initialization**: Class – at declaration/static block; Instance – in constructors.
    

---

### **Mutable vs. Immutable Objects**

- **Mutable Objects**
    
    - State **can be modified** after creation.
        
    - May lead to **data inconsistency** in multithreaded environments.
        
- **Immutable Objects**
    
    - State **cannot be changed** once created.
        
    - Offer **data integrity**, **thread safety**, and **predictability**.
        
    - Preferred when immutability aligns with requirements (e.g., in collections).
        

---

### **User Input and Command-Line Arguments**

#### **Command-Line Arguments**

- Passed during program execution.
    
- Accessed using the **args[]** parameter in `main(String[] args)`.
    
- All arguments are treated as **Strings**.
    

#### **Scanner Class (from java.util package)**

- Reads input from sources like **console**, **files**, or **strings**.
    
- Requires creation of a `Scanner` object (e.g., `Scanner sc = new Scanner(System.in);`).
    
- **Common Methods**:
    
    - `nextLine()` – Reads a line of text as `String`
        
    - `nextInt()` – Reads an `int`
        
    - `nextDouble()` – Reads a `double`
        
    - `nextBoolean()` – Reads a `boolean`
        
- Always **close Scanner** after use: `scanner.close();`
    
- Handle **exceptions** (e.g., `InputMismatchException`) using try-catch.
    

---

[End of Notes, Message #2]

**Subject:** _Week 3 – Java Static, Final, Overloading, Object Passing, and Arrays_

---

### **Static Keyword**

- **static** associates members (variables/methods) with the **class** instead of instances.
    
- **Static elements** are initialized once and shared across all objects.
    
- **Access**: Can be accessed using the **class name**.
    

#### **Static Variables**

- Shared among all instances.
    
- Defined using the `static` keyword.
    
- Example: `Counter.count` is incremented each time an object is created → shared across objects.
    

#### **Static Methods**

- Belong to the class, not instances.
    
- Accessed using the class name.
    
- Can only access **static** members directly (not instance variables).
    
- Example: `Calculator.add()`.
    

---

### **Final Keyword**

- Used to prevent **modification** of variables, methods, or classes.
    

#### **Final Variables**

- Once assigned, their value **cannot change**.
    
- Must be initialized at declaration or in a constructor.
    
- Behave as **constants**.
    

#### **Final Methods**

- Cannot be **overridden** by subclasses.
    
- Preserve method behavior across inheritance.
    

#### **Final Classes**

- Cannot be **extended** (subclassed).
    
- Represents a **leaf class** in inheritance.
    

---

### **Method Overloading**

- Multiple methods with the **same name** but **different parameter lists**.
    
- Differ by:
    
    - **Number** of parameters.
        
    - **Type** of parameters.
        
- Allows flexibility in method usage.
    
- Example:
    
    ```java
    add(int, int)
    add(double, double)
    add(int, int, int)
    ```
    

---

### **Constructor Overloading**

- Multiple constructors with **different parameter lists** in the same class.
    
- Used to initialize objects with different sets of data.
    

#### Example – `Car` Class:

1. No-arg constructor → default values.
    
2. Two-arg constructor → brand, model.
    
3. Three-arg constructor → brand, model, year.
    

---

### **Objects as Parameters and Return Types**

#### **Passing Objects as Parameters**

- Passes a **reference** to the object.
    
- Allows method to **access and modify** object’s state.
    
- Promotes **modularity** and **reusability**.
    

#### Example:

- `RectangleUtils.calculateArea(Rectangle rect)` computes area using passed object.
    

#### **Returning Objects from Methods**

- A method can **return** an object as output.
    
- Enables encapsulation of data/behavior within returned object.
    
- Example:
    
    ```java
    RectangleUtils.createRectangle(length, width) → returns Rectangle object
    ```
    

---

### **Arrays in Java**

#### **1-D Arrays**

- Stores multiple elements of the same type in a **linear sequence**.
    
- **Declaration & Initialization**:
    
    ```java
    int[] numbers = new int[5];
    ```
    
- **Element Access**:
    
    ```java
    numbers[0] = 10;
    ```
    
- **Array Length**: `numbers.length`
    
- **Iteration**: Use a `for` loop to traverse.
    

#### **2-D Arrays**

- Matrix-like structure: **array of arrays**.
    
- **Declaration & Initialization**:
    
    ```java
    int[][] grid = new int[3][4];
    ```
    
- **Alternative**:
    
    ```java
    int[][] grid = {
      {1, 2, 3, 4},
      {5, 6, 7, 8},
      {9, 10, 11, 12}
    };
    ```
    
- **Access**: `grid[row][col]`
    
- **Iteration**: Use **nested loops** for row and column traversal.
    

---

### **java.util.Arrays Class – Utility Methods**

1. **sort(array)** – Sorts in ascending order.
    
2. **binarySearch(array, value)** – Returns index of element (must be sorted).
    
3. **fill(array, value)** – Fills all elements with specified value.
    
4. **copyOf(array, newLength)** – Copies array to a new array of specified length.
    
5. **equals(arr1, arr2)** – Compares two arrays for equality.
    
6. **toString(array)** – Converts array to a string representation.
    

---

[End of Notes, Message #3]