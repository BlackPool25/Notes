- **Functions in C**:
    - Can be defined in our outside the class and can be called using function call.
        
        Example:
        
        ```C
        int sum(int x, int y)
        {
        return x+y;
        }
        ```
        
    - "Self-contained program segments that carry out some specific, well-defined task."
    - Returns a single value.
    - Can have multiple functions.
    - Helps making the code modular.
    - Increases re-usability.
- **Function Declaration and Definition:**
    - They are declared, defined and called.
    - **Function Declaration:**
    - **Syntax:**
        
        ![[Wn5NfeorT3qfGQDuNWaFVg_be624dd3f27449e9a7bf249b8d872aa1_image.png]]
        
        - Can be declared first and defined later.
        - A good practice to declare first.
        - 'void' does not return anything.
        - Ends with a semicolon
    - **Function Definition:**
        
        ![[56mxb11DT-6J-iP4IZ8yng_76eeaf87b4444ca9a2c39f967774b8a1_image.png]]
        
        - The input parameters (type-name pairs) are **compulsory** in the case of function definitions.
        - Must have same return type, number of parameters, same type of parameters and same function name.
    - **Calling a function:**
        
        ```C
        Syntax:
        function_name(argument values);
        ```
        
        - Names of the arguments need not match.
        - To use a function, it needs to be **called** or **invoked**.
    - **Function Name:**
        - The name of a function can be any but must be a valid identifier in C.
    - **Parameters:**
        
        ![[_SJNxeOUQJyWn2UTgbRTAw_eed3d06fff0941ce82b0305c1e0779f1_image.png]]
        
- **Importing Files:**
    
    ![[jZL_h0GiRt-XsYUtDhhMug_51184a770349400ea01cfd62b7b488a1_image.png]]
    
    ![[ugbk3I8pT2y7zSUvYuVT2g_8a9017ddbc1041c4b31a91c802cf81a1_image.png]]
    
    ![[Rxtr1UopQKGgaTxeRgNH4A_60f688201b8245e696857e379de129a1_image.png]]
    
    ![[I0pR_xF9TZCwaGgEghz4uw_1250ce567a304effaf489c4a0f4204a1_image.png]]
    
    ```C
    Compile using: gcc main.c 
    ```
    
- **Pros And Cons:**
    
    ![[Untitled.png]]
    
    ![[Untitled 1.png]]
    
- **Scope:**
    
    ![[Untitled 2.png]]
    
- **Auto and Global Variables:**
    
    ![[Untitled 3.png]]
    
![[Untitled 4.png]]
![[Untitled 5.png]]