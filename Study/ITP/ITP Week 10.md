**Summary of Files Handling in C Programs**

### What Are Files?

* A file is a named container of information stored on secondary storage (hard disk or solid-state drive)
* Administered by the operating system
* Store data for applications to access and manipulate

### Accessing Files in C Programs

1. **Opening a File**: Must be opened before reading from or writing to it using `fopen` function.
2. **File Stream**: Operating system associates a stream with the file when opened, allowing programs to access the file through this stream.
3. **Common Buffer and Position Indicator**: A common buffer and position indicator are maintained in memory for each function accessing the file, tracking how much of the file has been read.

### Key Steps

1. Open a file using `fopen`
2. Read from or write to the file
3. Close the file when no longer needed (optional but recommended)

**Takeaways**

* Files are essential for storing and managing data in C programs.
* Understanding how files are accessed, manipulated, and closed is crucial for effective programming practices.

This summary provides a concise overview of key concepts related to files handling in C programs, highlighting the importance of opening, accessing, and closing files in a program.

**Summary of File Handling in C Programs**

### Opening a File

* Create a pointer known as `file pointer` (e.g., `fp`) using the type `FILE`
* Use the function `fopen()` to open the file, specifying the filename and mode
	+ Modes:
		- `r`: Read only mode
		- `w`: Write only mode
		- `a`: Append only mode
	+ Compound modes (e.g., `r+`, `w+`, `a+`): Support both reading and writing

### Reading from a File

* Use the following functions to read data from files:
	+ `fgetc()`: Read character by character
	+ `fgets()`: Read line by line
	+ `fscanf()`: Read formatted input (similar to `scanf()`)

### Writing to a File

* Use the following functions to write data to files:
	+ `fputc()`: Write character by character
	+ `fputs()`: Write line by line
	+ `fprintf()`: Write formatted output (similar to `printf()`)

### Closing a File

* Use the function `fclose(fp)` to close the file, where `fp` is the file pointer
* Good practice to open, read/write, and immediately close files to avoid issues with other programs accessing the same files.

**Key Takeaways**

1. Understand how to open a file using `fopen()` and specify mode.
2. Use various functions (`fgetc()`, `fgets()`, etc.) to read from and write to files.
3. Close a file using `fclose(fp)` after reading or writing data.
4. Familiarize yourself with the different modes for opening files (e.g., `r`, `w`, `a`)

**Summary**

The meeting notes describe creating a C program called `frog1.c` that reads data from a file named `data1.txt`. The program uses the `fgets()` function to read one line at a time and stores it in an array `toRead`.

*   The program includes necessary headers: `<stdio.h>` for input/output operations, and `<string.h>` for string manipulation functions.
*   A file pointer `fp` is created using `fopen()`, which opens the file in reading mode (`"r"`).
*   Data is read from the file into the array `toRead`.
*   The program closes the file pointer using `fclose(fp)` to prevent resource leaks.

**Key Takeaways**

1.  Creating a C program that reads data from a file.
2.  Using `fgets()` to read one line at a time and storing it in an array.
3.  Including necessary headers for input/output operations (`<stdio.h>`) and string manipulation functions (`<string.h>`).
4.  Opening the file using `fopen()` and closing it with `fclose(fp)`.

**Code Snippets**

```c
#include <stdio.h>
#include <string.h>

int main() {
    FILE *fp;
    char toRead[100];
    
    // Open the file in reading mode ("r")
    fp = fopen("data1.txt", "r");
    
    // Read one line from the file into array toRead using fgets()
    fgets(toRead, 100, fp);
    
    fclose(fp);  // Close the file pointer
    
    char s_temp[] = "How";
    char *p;
    
    // Use strstr() to find if s_temp is a substring of toRead
    p = strstr(toRead, s_temp);
    
    if (p != NULL) {
        printf("String found: %s\n", toRead);
        printf("First occurrence of '%s' in '%s':\n", s_temp, toRead);
        // Print the first occurrence of s_temp in toRead
        while (*toRead == *s_temp && *toRead != '\0') {
            printf("%c", *toRead++);
        }
    } else {
        printf("String not found\n");
    }
    
    return 0;
}
```

**Summary**

The meeting notes describe a C program that reads numbers from a file `data2.txt` and displays them to the user. The program also writes the last number to another new file named `output_file.txt`.

*   The program includes necessary headers: `<stdio.h>` for input/output operations.
*   A file pointer `fp` is created using `fopen()`, which opens the file in reading mode (`"r"`).
*   Data is read from the file into an array `toRead` using a loop with repeated calls to `fgets()`.

**Key Takeaways**

1.  Reading data from a file line by line using `fgets()`.
2.  Using loops and conditional statements (NULL) for iterative operations.
3.  Writing data to a new file using `fputs()` and closing the file pointer using `fclose(fp)`.

**Code Snippets**

```c
#include <stdio.h>

int main(void){
    FILE *fp, *fp2;
    char toRead[100];
    
    fp = fopen("data2.txt", "r");
    
    if (fp == NULL) {
        printf("Error: Could not open file data2.txt\n");
        return 0;
    }
    
    while(fgets(toRead, sizeof(toRead), fp)!=NULL){
        printf("%s\n", toRead);
        
        // Writing the last number to a new file
        if (fp == NULL) {
            break;  
        } 
    }

    fclose(fp);

    fp2 = fopen("output_file.txt", "w");
    
    fprintf(fp2, "%d\n", 56);  // Write the last element to output_file.txt
    
    fputs("\nJust printed the last element read from the above list.\n", fp2);
    
    fclose(fp2);
}
```

This code snippet demonstrates how to use `fgets()` and `fputs()` functions in C programming.

**Summary**

The problem statement involves creating a C program that stores a list of grocery items with details such as name, price, quantity, etc. The tasks include:

*   Creating four functions:
    *   `readItems()`: Reads the details of a list of items from the user and stores them in an array of structures dynamically allocated.
    *   `printList()`: Prints the list of items previously read using `readItems()` function.
    *   `findItem()`: Searches for an item by choice from the above list.
    *   `maxPriceItem()`: Finds out the item with maximum price among all items stored in the list.
*   Creating a main function to call and demonstrate the usage of these functions.

**Key Takeaways**

1.  Dynamically allocating memory using `malloc()` for storing grocery items.
2.  Defining a structure (`struct item`) to store each grocery item's details (ID, name, price, quantity).
3.  Implementing four custom functions: `readItems()`, `printList()`, `findItem()`, and `maxPriceItem()`.

**Code Snippet**

```c
#include <stdio.h>
#include <stdlib.h>

struct item {
    int ID;
    char name[50];
    float price;
    int quantity;
};
```

This code snippet defines a structure (`struct item`) to store each grocery item's details, which will be used in the subsequent functions.

**Summary**

The problem statement involves creating a function `readGroceryList` to read details of grocery items from the user and return them as an array of structures.

**Key Takeaways**

1.  **Function signature**: The function takes two parameters: `count` (the number of items to read) and returns an array of structures (`struct item *`).
2.  **Dynamic memory allocation**: Memory is allocated for an array of size `count`, where each element is a structure of type `struct item`.
3.  **Loop to read details**: A loop iterates over the range `[0, count)` to read details (ID, name, price, quantity) from the user and store them in the dynamically created array.
4.  **Unique ID assignment**: The variable `uniquNum` is incremented for each item and assigned as its unique ID.
5.  **Return statement**: The function returns a pointer to the dynamically allocated array of structures.

**Example Usage**

1.  In the main function, create a variable `num_q` to capture the number of grocery items from the user.
2.  Call the `readGroceryList` function with `num_q` as input and assign its return value (a pointer) to another variable (`gItems_main`) in the main function.

**Code Snippet**

```c
struct item * readGroceryList(int count) {
    struct item * gItems = malloc(sizeof(struct item) * count);
    
    int uniquNum = 1;
    for (int i = 0; i < count; i++) {
        gItems[i].ID = uniquNum++;
        
        printf("Enter details for item %d: \n", i + 1);
        
        scanf("%s", gItems[i].name);
        scanf("%f", &gItems[i].price);
        scanf("%d", &gItems[i].quantity);
    }
    
    return gItems;
}
```

Note that the `main` function should handle memory deallocation for the dynamically allocated array when it is no longer needed.

**Summary**

The problem statement involves creating two functions: `readGroceryList` to read details of grocery items from the user and store them in an array, and `printGroceryList` to print the list of grocery items.

**Key Takeaways**

1.  **Function signature**: The function `readGroceryList` takes one parameter (`count`) and returns a dynamically allocated array of structures (`struct item *`).
2.  **Dynamic memory allocation**: Memory is allocated for an array of size `count`, where each element is a structure of type `struct item`.
3.  **Loop to read details**: A loop iterates over the range `[0, count)` to read details (ID, name, price, quantity) from the user and store them in the dynamically created array.
4.  **Unique ID assignment**: The variable `uniquNum` is incremented for each item and assigned as its unique ID.
5.  **Return statement**: The function returns a pointer to the dynamically allocated array of structures.

**Function: printGroceryList**

1.  **Signature**: Takes two parameters (`gItems`, `count`) and prints the list of grocery items.
2.  **Printing loop**: A loop iterates over the range `[0, count)` to print the details (ID, name, price, quantity) of each item in the array.

**Example Usage**

1.  In the main function, create a variable `num_q` to capture the number of grocery items from the user.
2.  Call the `readGroceryList` function with `num_q` as input and assign its return value (a pointer) to another variable (`gItems_main`) in the main function.
3.  Call the `printGroceryList` function by passing the array (`gItems_main`) and count of items (`num_q`) as arguments.

**Code Snippet**

```c
struct item * readGroceryList(int count) {
    struct item * gItems = malloc(sizeof(struct item) * count);
    
    int uniquNum = 1;
    for (int i = 0; i < count; i++) {
        gItems[i].ID = uniquNum++;
        
        printf("Enter details for item %d: \n", i + 1);
        
        scanf("%s", gItems[i].name);
        scanf("%f", &gItems[i].price);
        scanf("%d", &gItems[i].quantity);
    }
    
    return gItems;
}

void printGroceryList(struct item * gItems, int count) {
    for (int i = 0; i < count; i++) {
        printf("Item ID: %d\n", gItems[i].ID);
        printf("Name: %s\n", gItems[i].name);
        printf("Price: $%.2f\n", gItems[i].price);
        printf("Quantity: %d units\n", gItems[i].quantity);
    }
}

int main() {
    int num_q;
    
    scanf("%d", &num_q);
    
    struct item *gItems_main = readGroceryList(num_q);
    
    printGroceryList(gItems_main, num_q);
    
    return 0;
}
```

Note: In the `readGroceryList` function, I added some extra code to handle reading the input for name, price and quantity using scanf statements.

Here is a concise summary of the meeting notes:

**Implementation of findItem Function**

The `findItem` function was implemented to search for an item in the grocery list with a specified quantity.

**Function Signature and Logic**

* The function takes as input: a struct item `fItem`, an integer `qVal` representing the desired quantity, and the array of grocery items `gItems`.
* The function iterates through the array of grocery items to find an item with the matching quantity.
* If found, it returns the corresponding struct item. Otherwise, it creates a dummy item with ID = -1 and returns that.

**Main Function Call**

The main function calls `findItem` by:
	+ Prompting the user for input: enter the quantity of the item you wish to find (`%d`, &qVal).
	+ Calling `findItem` with the specified quantity, array of grocery items, and number of items in the array.
	+ Printing either a "item not found" message or details about the item if it was found.

**Compilation and Execution**

* The program is compiled without errors using `gcc`.
* Upon execution:
	- The user inputs 3 unique grocery items with different quantities.
	- When searching for an existing quantity (e.g., 2), the program prints detailed information about that item.
	- When searching for a non-existent quantity (e.g., 10), it displays "item not found".

This summary captures the essence of implementing and testing the `findItem` function.

Here is a concise summary of the meeting notes:

**Implementing `findMaxPriceItem` Function**

* A function called `findMaxPriceItem` was implemented to find an item in the grocery list with the maximum price.
* The function takes as input: a struct item pointer `gItems`, which is an array of grocery items, and the count of items in the array.

**Function Logic**

* Initialize variables: `maxIndex = -1` and `maxPrice = -1`.
* Iterate through the array using a while loop (`i < count`).
* Check if the current item's price (`gItems[i].price`) is greater than `maxPrice`. If true, update:
	+ `maxPrice = gItems[i].price`
	+ `maxIndex = i`
* Increment the loop counter (`i++`).

**Returning Maximum Price Item**

* After the loop exits, return the item with maximum price: `gItems[maxIndex]`.

**Calling Function in Main**

* In the main function, call `findMaxPriceItem` by passing:
	+ The array of grocery items (`gItems`)
	+ The count of items in the array

**Printing Maximum Price Item**

* Print details about the item with maximum price using a printf statement.

**Compilation and Execution**

* Compile the program without errors.
* Run the executable and enter 3 as the number of grocery items in the store.
* Input item details: ABC (price = 10.23, quantity = 4), XYZ (price = 23.34, quantity = 2), PQR (price = 104.34, quantity = 3).
* The program prints all items and the item with maximum price is printed as ID=3, Name=PQR, Price=104.33996, Quantity=3.

This summary captures the key points of implementing a function to find an item in a list with the maximum price, calling this function in the main code, and compiling/executing the program with sample input values.

Here is a concise summary of this segment:

**Summary**

* This module focuses on file handling in C, covering:
	+ Opening files
	+ Reading data from files
	+ Writing data to files
	+ Closing files
* A comprehensive case was implemented to manage a list of grocery items for a store.
* The case demonstrated how to approach and solve real-life problems using C language elements and constructs.

Note: This summary is very brief as it's just a wrap-up statement at the end of the module, so there isn't much detail to capture.