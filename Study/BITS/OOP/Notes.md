
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