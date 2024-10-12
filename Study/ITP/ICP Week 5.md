- **Arrays:**
    
    - Arrays are a fixed-size collection of data of the same data type, stored sequentially or contiguously in memory, enabling access and modification through an index.
    - Arrays are zero-indexed.
    
    ```C
    Syntax:
    data_type array_name[Size];
    ```
    
    - We cannot assign one array to another; that would lead to a compile-time error.
    - Arrays are stored contiguously in memory, quantized by the size of each individual element.
        
        ![[cGwjF3j2TTix5Zd3dUehsg_b724803fa0974578bef5ff291a4546a1_image.png]]
        
    - The name of an array refers to the starting address of the array (1001010 in this case).
    - **sizeof()** is a compile-time operator in C that returns the total number of bytes occupied by a variable.
    - We have bound checking for arrays while writing to them but not while reading from them.
    - Arrays in C are **passed by reference instead of being passed by value.** This means that any modifications performed to the array within the called function will be reflected to the actual array present in the calling function.
- **Linear Search:**
    - Run through every single element, sequentially, and check if it matches the element we are looking for. This is, in essence, linear search.
- **Sorting:**
    - Sorting reduces time taken to index the variables.
- **Selection Sort:**
    
    - We maintain two parts of the array, the sorted part (on the left) and the unsorted part (on the right). Initially, the sorted part is empty, and the entire array is the unsorted part. In each iteration, the smallest element from the unsorted part of the array is added to the sorted part. This process is repeated until we no longer have an unsorted part, i.e., our sorted part has completely enveloped the array.
    
    ![[Untitled 6.png|Untitled 6.png]]
    
- **Character Arrays:**
    
    - Strings in C are defined as an array of characters that terminate with a '\0'.
    - There are two functions in C that come built-in to the stdio.h header, namely **getchar() and putchar()**. These functions are respectively used for **“getting”** a character as an input from the user (through the keyboard) and for **“putting”** a character from a variable to the output device (monitor).
    - **toupper() function** which returns the uppercase equivalent of the character it takes in as an input.