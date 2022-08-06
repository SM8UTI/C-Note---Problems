# Variables

</br>

**C** is ***static typed language***.

 > Note : A statically-typed language is a language (such as Java, C, or C++) where variable types are known at compile time.


</br>

- variables are some names.

- Variables are containers for storing data values.

</br>

## Declaring Variables

Declaration announcing the properties of variable to the compiler

    - Size of the Variable
    - Name of the Variable 

Declaration :  `DataType variableName;`

Initialization : `DataType variableName = value;`

Where Datatype is one of C types (such as int), and variableName is the name of the variable (such as x or myName). The equal sign is used to assign a value to the variable.

</br>

```c

// Example : 

`int a;` // Declaration

a = 10; // initialization


```

</br>

```c
// Syntax :

// DataType variableName = value;

// Ex : 

int a = 10;
float b = 1.5;
char c = 'c';


```

</br>

## Variable Naming Conventions

</br>

Variable name : composed of letters or combination of letters ( both uppercase and lowecase ) and digits.
</br>

### Rule-1

    - don't start variable name with digit.

### Rule-2

    - degining with underscore is valid but not recommended.

### Rule-3

    - c langauge is case sensitive. uppercase letters are different from lowercase letters.

### Rule-4

    - Special characters ( @,#,%,^,...) not allowed in the name of variable 

### Rule-5

    - blanks or white spaces are not allowed.

### Rule-6

    - Don't use keywords to name your variables.


</br>

## Types Of Variables 

</br>

There are many types of variable : 
</br>

1.  Local Variable 
2. Global Variable 
3. static Variable 
4. Automatic Variable 
5. external variable 

</br>

### Local Variable 

</br>

A variable that is declared inside the `function or block` is called a **local variable**.

It must be declared at the start of the block.

```c

void func(){  
    int x=10;//local variable  
}  

```
</br>

### Global Variable

</br>

A variable that is declared `outside the function or block` is called a **global variable**. Any function `can change the value of the global variable`. It is available to all the functions.

It must be declared at the start of the block.

```c

int value=20;//global variable  

void function1(){  

    int x=10;//local variable  

}  
```

</br>

### Static Variable
</br>

A variable that is declared with the `static keyword` is called **static variable**.

It retains its value between multiple function calls.
</br>

```c

void function1(){  

    int x=10;//local variable  
    static int y=10;//static variable  
    x=x+1;  
    y=y+1;  
    printf("%d,%d",x,y);  
}  

```

>If you call this function many times, the local variable will print the same value for each function call, e.g, 11,11,11 and so on. But the ***static variable will print the incremented value in each function call***, e.g. 11, 12, 13 and so on.
</br>

### Automatic Variable

All variables in C that are declared inside the block, are automatic variables by default. We can explicitly declare an automatic variable using `auto keyword`.
</br>

```c

void main(){  

    int x=10;//local variable (also automatic)  
    auto int y=20;//automatic variable  
}  

```
</br>


### External Variable

</br>
We can share a variable in multiple C source files by using an external variable. To declare an external variable, you need to  `use extern keyword`.
</br>

myfile.h 

```c
extern int x=10;//external variable (also global)  
```
</br>

pr1.c
```c
#include "myfile.h"  
#include <stdio.h>  
void printValue(){  
    printf("Global variable: %d", global_variable);  
}  
```

</br>
