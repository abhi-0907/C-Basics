
## `C vs C++`

- C++ is an enhanced version of C which has Object oriented programming which enhanced the developer speed and productivity.
- MongoDB and Apache HTTP server had its design motivation from C++ alone.
- ##### Language Type:
- C is procedural programming and C++ is a Procedural + OOPs
- ##### Approach
- C uses top-down approach and C++ uses bottom up approach
- C has 32 keywords while C++ has over 95 keywords
- ##### Memory Allocation
- C use calloc() and malloc() functions for dynamic memory allocation and free() for de-allocation.
- C++ use new operator for dynamic memory allocation and delete operator for de-allocation.
- ##### Access Modifiers
- C structure does not have access modifiers.
- Access modifiers are used in C++ structures.
- ##### Virtual and friend functions
- No support for virtual and friend function in C
- C++ supports virtual and friend functions.
- ##### Support for error handling
- No support for error handling.
- try catch throw blocks help in error handling.
- ##### Namespace
- C Does not support namespace resulting in less effecient code and name collisions.
- C++ Supports namespace to prevent name collisions.
- ##### Function and Operator overloading
- C does not support function and operator overloading directly.
- C++ supports function and operator overloading.
- ##### Reference Variable
- No support for refrdence variables in C.
- C++ supports refrence variable.

#### **1: Object-Oriented Design**

- C++ has support for Class, object, inheritance, abstraction, etc as a result code reusability, data hiding, and memory management is possible
- C doesn’t have OOPs features, data is open everywhere and move freely through functions

### **2: Procedural v/s Hybrid Language**

- C is a procedural language i.e development of code in the form of a list of  instructions (functions) where each instruction conveys the compiler to do some action
- C++ is viewed as Hybrid language i.e it can be used as object-oriented or traditional C type Procedural Programming i.e using OOPS in C++ is optional whereas in java it is mandatory.

### **3: Namespace Feature**

- C has predefined function support only in the form of header files, as a result, you cannot duplicate the names within the file or program
- C++ has namespace feature which enables to have same names for functions or variables which  solves naming collision problem

#### With namespace in C++

```cpp
#include<iostream>
namespace Prep1  //first namespace
{
    int a = 1;
}
namespace Prep2  //2nd namespace
{
    int a = 2; //same name but different namespace
}
int main()
{
    cout << Prep1::a;
    cout << Prep2::a;
  
    return 0;
}
```

### **4: Reference Variables support**

- Reference variables enable the user to have multiple variables point a single memory address which is not possible in C
- C++ has only pointer support: When the reference variable is lost it can be accessed through another alias variable, but if the pointer is lost,  the whole security comes into question

### **5: Keywords**

- C supports 32 keywords whereas C++ has also the same 32 keywords and along with exclusive 20 keywords it has a count of 52 keywords in C++

### **6: Overloading of functions and operators**

- C++ can have  different functionalities for the same operator  
    ex: **+** can join a string and arithmetic addition of numbers ([using Operator Overloading](https://prepinsta.com/c-plus-plus-theory/operator-overloading/))
- C++ can have the same name for different functions where the only type of input is different [(using Function Overloading)](https://prepinsta.com/c-plus-plus-theory/function-overloading-in-cpp/)
- In C you have abs() labs() sabs() function here function code is the same only datatype is different but still, you need to have a different namer which  hampers readability.

### **7: Subset v/s Superset**

- C is a subset of C++ whereas C++ is a superset of C which means all the C codes can be clubbed or run alone in C++ compiler but vice-versa not possible.

### **8: Support for exception handling**

- C++ has direct support for exception handling in the form of try, throw, catch keywords which can avoid abnormal termination of the program due to runtime errors
- In C any runtime error occurs program shutdowns immediately  
    ex: the situation of divide by 0 can be handled in C++ but in C it results in compiler failure.

### **9: Designers and History**

- C was developed by Dennis Ritchie In 1970s at AT&T Bell Labs with the combined features  of BCPL and Basic Programming Languages
- Inspired from the class feature of Simula67 and block structured  
    programming of C, C++was developed by Bjarne Stroustrup in 1979 as an extension of C.

### **10: When C and When C++**

- C is the only option for embedded systems and System level code(operating System design)
- C++ gives High-end performance when used in device drivers, server-side applications, gaming, networking i.e super secure application design requires data-hiding from OOPS.



## `Keywords in C`

Keywords are predefined, reserved  words used in programming that have special meanings to compiler. Each keyword is meant to perform a specific function in a C program. Since keywords are referred name for compiler, they can not be used as variable name.

There are fixed number of **Keyword in C programming language** and every Keyword serve as a building block for program statements. 

There are total 32 keywords in C keywords are written in lowercase letters..

| auto     | else   | long     | switch   |
| -------- | ------ | -------- | -------- |
| break    | enum   | register | typedef  |
| case     | double | return   | union    |
| char     | float  | short    | unsigned |
| const    | for    | signed   | void     |
| continue | goto   | sizeof   | volatile |
| default  | if     | static   | while    |
| do       | int    | struct   | _Packed  |


## `Identifiers in C`

Each program elements in a C program are given a name called identifiers. Name given to identity variable, functions and arrays are examples for identifiers. 

identifiers must be unique. they are created to give  a unique name  to an entity to identify it during the execution of the program.

**for example**
 1 int square  
 2 double balance   
 3 function add()

Here, **square** , **balance** and **add()** are identifier. there are one thing that you should remember, identifier names must be different from keywords. you cannot use  int as an identifier because int is keyword.

### Rule for an identifier

- An identifier can only have alphanumeric characters (a-z, A-Z, 0-9) and underscore (_).
- The first character of an identifier can also contain alphabet (a-z, A-Z).
- Identifiers are also case sensitive in C. For example  name and Name are two different identifiers in C.
- Keywords are not allowed to be used as identifiers.
- No special character, such as semicolon, period, white spaces, slash or comma are permitted to be used in or as identifiers.

| Comparison      | Keyword                                        | Identifier                                                               |
| --------------- | ---------------------------------------------- | ------------------------------------------------------------------------ |
| Basic           | Keywords are the reversed words of a language. | Identifiers are the user defined names of variable, function and labels. |
| Use             | Specify the Type/kind of entity.               | Identify the name of particular entity.                                  |
| Format          | Consider only letters.                         | Consider letters, underscore, digits.                                    |
| Case            | Use only lower case.                           | Lower and upper case, both are allowed.                                  |
| Symbol          | No special Symbol, punctuation is used.        | No punctuation or special symbol except ‘underscore’ is used.            |
| Classifications | Keyword not further classified.                | Identifiers are classified into external name and internal name.         |
| Starting letter | It  always starts with a lowercase latter.     | First character can be a uppercase, lowercase letter or underscore.      |

## `Tokens in C`

Tokens are called building block of C programming, that means only with the help of tokens a C program can be created.

- every small part that is used in the program is called tokens.
- In C programming, some INDIVIDUAL words and characters are fixed, whose functions are fixed, called tokens.
- It is the smallest Lexial unit of C program.

There are some internal tokens we need to know while writing a program in C to understand the most basic to the syntax of the C language.

### Some internal tokens are:-

- Keywords
- Identifiers
- Constants
- Strings
- Special Symbols
- Operators

## `Constants`

Constant is a value, which does not change in program execution.

- constant value is fixed.
- it is also known as Literals.
- it does not matter where we use it in program, its meaning always fixed.
- it is also like normal variables.
#### Types of Constants:-

1.**Integer constant** 
       -The whole values used in the C program are called integer constant. Like: 1,53,677 etc.. 
2.**Character constant** 
    -The different characters used in the C program are called character constant. Like: f, v, s, w, # etc..        
    
3.**Float constant** 
    -In C program, such numeric value in which the digit after the decimal is called float constant. Like: 4.44444, 34.6634 etc. 
    
4.**String constant** 
    - many literal characters are placed under string literal. Like: “rat”, “prep”, etc..4


## `Strings`

The group of characters is known as strings. which are always enclosed in double quote. it is also said to be array of characters.it is used to stored data of class,mobile numbers , name etc. At the end of the string there is always a special character, which is known as null. its indicate the end of the string.

#### Declaration of Strings:-

char string[20] = {‘p’,’r’,’e’,’p’,’I’,’n’,’s’,’t’,’a’,’\\0′}; 
char string[20] = “prepInsta”; 
char string[] = “prepInsta”;


## `Special Symbols`

Some special symbols are used in C programming. symbols means alphabet, exclude the digits using some symbols in C programming.In C programming some special symbol are used in C having some special meaning and cannot be use in other purpose. The following symbols are:- 
**Braces {}:-** these curly braces are used to show the starting and ending of a block of code containing some executable statement. 
**Parentheses ()**:- Parentheses are used to specify the function call and function parameter. 
**Brackets []**:- this is the opening and closing brackets. it is used as array element reference. these stipulate the single and multidimensional subscripts. 
**Comma (,)** :- it is used to separate more then one statement. 
**Asterisk (\*)** :- used to create pointer variable. 
**Assignment variable**:- used to assign values. 
**Semicolon:-** In C program after every statement we have to put a semicolon (;) which tells the compiler the statement ends there .


## `Operators`

Operators is special symbol which is used to perform mathematical operation like, addition, subtraction, division, multiplication.Different types of symbols are used to perform different type of mathematical and logical operation in C programming is known as operators. that symbols.

#### types of operator:-

1. **Unary Operator:**– unary operators are those operators, which require only single operands is known as unary operator.
    Example:- increment and decrements operator.

2. **Binary Operator**:- Those operators, which require two operands is known as binary operator. **Binary operators are:**–
- Arithmetic operator
- Logical operator
- Bitwise operator
- Conditional operator
- Relational operator
- Assignment operator

3. **Ternary operator**:- These operators which require three operands are known as ternary operator.          
   Example:– Conditional operator (?:).




## `Variables in C`

-  The name of the memory location of the data which can be accessed with the help of that name and can be rewritten or used for calculations later on.
- Variable is a storage area. which is used to store the data
- Variable data is contained, which can be changed at any time during program execution. After declaring the variable it is given a value, this value is to be assigned in the many form. Like x = 5; or a=10;
-  Before using the variable it is necessary to declare in C. Values of variables are changeable. You can delete a value and enter another value.  You can also do this on compile time and dynamically(during program execution).

### Datatype of Variables:

A variable should be given a type in the C language,  which determines what kind of data the variable will hold. it can be:

- char : it can hold a character in it.
- int : it is used to hold an integer.
- double : it is used to hold a double value.
- float : it is used to hold a float value.

###### DECLARATION OF A VARIABLE

While programming you first need to tell the computer/compiler the variable’s name and it’s data type, when you do that the compiler creates an empty memory reserved for that data .

	`data_type single_variable_name;`

In other words, we can say that
- When we declare a variable , then it allocates memory according to the data type of variable.
- After declaration of the variable, it takes Garbage Value inside it.

### Variable Initialization

- When the variable is initialized, then it allocates the memory according to data type of variable.
- In variable initialization, a variable takes only a value.


## `Scope of variables`

By scope of a variable we mean which part of the code a variable is accessible (visible) to .A variable can have many scopes in c let’s discuss some of them .

According to Scope, variables is divided into two categories:-

Local Variables  
Global Variables

### **Local Variable**

Local variables are those variables that are defined in a small block of the program such as function, control statement block etc. Such variables are used only by the same block.

- A variable inside the function/block is a local variable .
- Local Variables is inside the function.
- The default value of the Local variables is ‘garbage value’.

**Example** :
```c
#include<stdio.h> 
int main()
{
     int a,b,c; // local variables
     a =10;
     b = 30;
     c = a + b;
     printf("%d",c);
}
```

### **Global variable**

As oppose to local variable a global variable is out side every function and is accessible to all the functions and the value of a global variable can be changed by any function.

Global variables are those variable whose scope is in whole program. These variables are defined at the beginning of the program.

- Global variables are out of the function.
- Global variables have visibility throughout the program.
- The default value of ‘Global Variables’ is ‘0’.

**Example :**
```c
#include<stdio.h>
int d=20; // global variable
int main()
{
      int a,b,c; // local variables
      a = 10;
      b = 30;
      d = d + 10;
      c = a + b + d;
      printf("%d",c);
      return c;
}
```

## `Scope`

region or block in which a variable is declared, defined, and utilised; the variable is removed automatically when the region or block expires. It can also be remembered as lifetime of a variable

```
int main() { --------1--------------------------------------------|
                                                                  |
    int a;           // scope of a                                |
                                                                  |
    func() {  -------2----------------|                           |
        int b;  //scope of b          |                           |
                                      |                           |
    } ---------------3----------------                            |
                       // scope of a                              |
    return 0;                                                     |
} ----------------4-----------------------------------------------|
```


### Types of variables

In the C programming language, variables can be defined in three different places.

- Local variables are variables found within a function or a block.
- Global variables are variables that exist outside of all functions.
- Formal parameters are used in the defining of function parameters.

###  Local Variables : 

Local variables are those that are defined within a function or block.Only statements included within that function or code block are permitted to use them. Outside of their own function, local variables are unknown.

Below example are representing the scope of local variables a and b.
```
#include<stdio.h>

int main() { -------------------------------1-----------------|
                                                              |
    int a, b;   // local variable                             |
    a = 20;                                                   |
    b= 10;                                                    |
                                                              |
    return 0;                                                 |
}-------------------------------------------2-----------------|
```

### Global variable :

Outside of a function, typically on top of the program, global variables are defined. Global variables can be accessed inside any of the functions created for the program and keep their values during its execution. Any function may access a global variable.  
In other words, once a global variable has been declared, it can be used throughout the entire program. 

Below example are representing the scope of global variables c and d.
```
#include <stdio.h> ----------------------------------------1--|
int c,d; // global variable
int main() { 

int a,b; //local variable |
c=20;                                                         |
d=10;                                                         |
                                                              | 
return 0;                                                     |
} -------------------------------------------------------2----|
```

### Formal Variable :

Formal parameters are prioritised over global variables and are handled as local variables within a function.

Below example are representing the functioning of formal variables.

```
#include<stdio.h>
 
int a = 30; // global variables
 
int main () {

  
  int a = 10;  //local variables
  int b = 15;
  int c = 0;

  printf ("value of a in main() = %d\n",  a);
  c = product( a, b);
  printf ("value of c in main() = %d\n",  c);

  return 0;
}

/* function  */
int product(int a, int b) {

   printf ("value of a in product() = %d\n",  a);
   printf ("value of b in product() = %d\n",  b);

   return a * b;
}

### Output :

value of a in main() = 10
value of a in product() = 10
value of b in product() = 15
value of c in main() = 150

```


## `Range of Data Types in C`

there are many different data types in C, and every data type has a pre-defined range of data, under which it works, so we need to be smart while choosing a datatype in our program, below is a table which represents the different data-type, and their data range.

| **Name Of The Datatype** | **Range of Datatype**                                |
| ------------------------ | ---------------------------------------------------- |
| Double                   | 2.3E-308 to 1.7E+308                                 |
| Long Double              | 3.4E-4932 to 1.1E+4932                               |
| Long                     | -9223372036854775808 to 9223372036854775807          |
| Unsigned Long            | 0 to 18446744073709551615                            |
| Float                    | .2E-38 to 3.4E+38                                    |
| int                      | -32,768 to 32,767 or -2,147,483,648 to 2,147,483,647 |
| unsigned int             | 0 to 65,535 or 0 to 4,294,967,295                    |
| short                    | -32,768 to 32,767                                    |
| unsigned short           | 0 to 65,535                                          |
| char                     | -128 to 127 or 0 to 255                              |
| signed char              | -128 to 127                                          |
| unsigned char            | 0 to 255                                             |

```c
#include<stdio.h> 
#include<stdlib.h> 
#include<limits.h> 
#include<float.h>
int main()
{

    printf("CHAR_BIT : %d\n", CHAR_BIT);
    printf("CHAR_MAX : %d\n", CHAR_MAX);
    printf("CHAR_MIN : %d\n", CHAR_MIN);
    printf("INT_MAX : %d\n", INT_MAX);
    printf("INT_MIN : %d\n", INT_MIN);
    printf("LONG_MAX : %ld\n", (long) LONG_MAX);
    printf("LONG_MIN : %ld\n", (long) LONG_MIN);
    printf("SCHAR_MAX : %d\n", SCHAR_MAX);
    printf("SCHAR_MIN : %d\n", SCHAR_MIN);
    printf("SHRT_MAX : %d\n", SHRT_MAX);
    printf("SHRT_MIN : %d\n", SHRT_MIN);
    printf("UCHAR_MAX : %d\n", UCHAR_MAX);
    printf("UINT_MAX : %u\n", (unsigned int) UINT_MAX);
    printf("ULONG_MAX : %lu\n", (unsigned long) ULONG_MAX);
    printf("USHRT_MAX : %d\n", (unsigned short) USHRT_MAX);

    return 0;
}
```

###### Output :

```
CHAR_BIT : 8
CHAR_MAX : 128 
CHAR_MIN : -127
INT_MAX : 2147483647
INT_MIN : -2147483648
LONG_MAX : 9223372036854775807
LONG_MIN : -9223372036854775808
SCHAR_MAX : 127
SCHAR_MIN : -128
SHRT_MAX : 32767
SHRT_MIN : -32768
UCHAR_MAX : 255
UINT_MAX : 4294967295
ULONG_MAX : 18446744073709551615
USHRT_MAX : 65535
```



## `Size of Data Type`

In C, each data type has a unique set of operations that can be done on it and varied memory requirements. The type of data that the variable can store, such as character, integer, float etc.
##### Classification of Data Types in C:

| **Types**              | **Illustration**                                                                                                                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Primitive Data Type    | Primitive data type are used as a most fundamental data type in programming languages. Examples of primitive data type are as byte, character, sort, int, boolean, long, float and double. |
| User Defined Data Type | A user defined data type is a data type that can be derived from an existing data type.Examples of user derived data types are as array, pointer, structure and union.                     |
| Void Data Type         | A void data type is a data type that hasn’t any value or operator and it doesn’t give any response to its caller. A void data type comes from primitive data type.                         |
| Derived Data Type      | A derived data type is a data type that derived from built-in or primitive data types.                                                                                                     |

##### Size of Data Types

|**Data Types**|**Size (in bytes)**|
|---|---|
|Int|4|
|Char|1|
|Float|4|
|long|4|
|Short|2|
|Double|8|

`sizeof(data_type)` used to find the size of a dataype

```
#include<stdio.h>
int main()
{
	int size_of_int=sizeof(int);
	printf("The size of int data type = %d\n",size_of_int );
return 0;
}
```


## `Const Keyword`

Constant are those Whose value can not be change during program execution. whenever you declare the constant its value remain fixed during execution of the program.If there is an attempt to change its value then there is an error in the progam.
## About Constant :

- A value or a keyword that has a definite set value is called a constant.
- Value of Constant is fixed.
- Constant can be any data types.
- Constant is also known as Literals.
- Constant is also the pointer.

`const data_type variable_name = value(optional);`

#### In C language there are two types of constant:-

- Constant Literals
- Constant variables
### Constant Literals

Constant Literals are values that you use directly in the program. for example,
y=x+2;
In this example, 2 is constant literal. It has been directly used in the program. it can not be changed during execution in the program.
### Constant Variables

you declare the constant variable like variables. The advantage of a constant variable is that if you have to change constant later then you do not need to change it many places, you only change the value of constant variable so that the value is automatically changed everywhere.


### **Types of Constant**

**There are 4 types of constant in C:-**

- Integral Constant
- Floating constant
- Character constant
- String constant
- Constant Keywords


### Integral constant

- The constant in the integer value is an integral constant.
- Integer constant works as a normal value.
- Integer constant can be either negative or positive.
- Range of integer constant -32768 to 32767.
	  `const int num =20;`

### Floating constant

- A floating constant is a decimal value is called a floating constant.
- The floating constant works as a normal float variable.
- It contains the decimal point.
- If the value of the floating constant is of integer type, it takes the decimal point.
		`const float num1 = 5;`

### Character Constant

- When character values to it then it is called a character constant.
- Character constant works as a normal variable.
- Character constant takes only a single character.
- The character constant is also used with escape sequences.

### String constant

- A string constant is a string array (coming up in later lessons) having fixed string values to it.
- String constant takes a single character and multiple characters.
- The value of the string constant is written within the double quotation mark (“”).
- a string constant is also used with escape sequences.

### Constant keyword

We can define a constant to a program using #define or const int or const float or const char whichever we want and that keyword (identifier) will have a fixed value and can not be changed later (remains a constant).


## `Type Casting`

The method of typecasting in C involves utilizing the casting operator during program design to change one data type to another.

Depending on what we want the program to perform, type casting causes the compiler to automatically switch from one data type to another.

#### **Types of TypeCasting in C:**

- Implicit typecasting
- Explicit typecasting

#### **Implicit Typecasting:**

In C, implicit type casting is used to change any variable’s data type without changing the value it stores.  
Without changing any of the values kept in the data variable, it executes the conversions.

#### **Explicit TypeCasting:**

- The user converts types explicitly by using the (type) operator.
- The destination type’s ability to store the source value is checked at runtime prior to the conversion being carried out.

#### Advantages of Typecasting:

- Programmers can change one data type to another by using type casting.
- The program is made lighter by typecasting.


```c
#include<stdio.h>
int main()
{
        int x= 19, y=2;
        float div;
        div=x/y;
        printf("The output : %f\n",div);
        return 0;
}
```

```c
#include<stdio.h>
int main()
{
	int x = 19, y = 2;
	char c = 'x';
	double div;
	div = (double)x / y;
	c = c + 2;
	printf("The output of Implicit typecasting : %c\n", c);
	printf("The output of Explicit typecasting: %f", div);
	return 0;
}
```


## `Storage Classes`

Storage Classes are used to describe the different features of variables and functions in C programming language.

These features mainly includes the points such as `scope` of variable,  `lifetime` of variable, the `location` where the variable will be stored, `initial value` of variable and  who can access the variable or where the variable is accessible.

### **Types of Storage Classes**

In C Programming Language there are four types of storage classes.

1. **Auto Storage Class**
    -  This is the default storage class for all the variables declared inside a function or a block
    - There is no need for writing auto keyword while writing the C program.
2. **Extern Storage Class**
    - Extern storage stands for external storage.
    - Extern means that variable is declared outside the block where it is used.
3. **Register Storage Class**
    - Register storage class is almost same as auto storage class.
    - Register storage basically stores variable into CPU register rather than RAM for faster access.
4. **Static Storage Class**
    - This storage class is used to declare static variables which are popularly used while writing programs in C language.
    - Static variables have a property of preserving their value even after they are out of their scope


### Auto Storage Class

- The automatic storage class includes variables defined within functions or blocks with the auto specifier.
- If no storage class is specified, all variables defined within a function or block are automatically stored under that class.
- The block in which they are defined is local to variables with automatic storage classes.
- On leaving the block where they are defined, variables are destroyed.
- Any garbage value is the default value for the variables in the automatic storage class.
- The default storage class is called auto.

### **Working of the Code**

- In this code auto int i is defined at different stages with different scopes.
- Each time auto int i is defined, it’s value will be printed only in that particular scope only.
- First of all auto int i = 3 will be printed, then it’s scope will end.
- Then auto int i = 2 will be printed, and then it’s scope will end.
- At the end auto int i = 1 will be printed.
```c
#include<stdio.h>
int main()
{
    auto int i = 1;
    {
        auto int i = 2;
        {
            auto int i = 3;
            {
                printf("%d ",i);
            }
        }
        printf("%d ",i);
    }
    printf("%d ",i);
    return 0;
}
```

even with out auto keyword the code works same as the default storage class for every variable declared in a block or function

### Extern Storage Class

Extern is mostly used to indicate that a variable has been defined with external linking in another part of the program.

When we have global variables or methods that are shared by two or more files, we use an external storage class.

No storage is allocated to a variable when the extern specifier is used with a variable declaration since it is presumed that the variable has already been created elsewhere in the program.

##### Use of Extern Storage Class

- We can construct the self-customized header file “external.h” for using extern variables, and there we have stored int a and int b.
- The syntax for importing “external.h” into our main “prepinsta.c” code is as follows: `#include <external.h>`
- The variables declared in the external.h file can then be used after being initialised once more in the prepinsta.c file.
- Here sum = a + b will show the following output

###### File name: external.h
```
int a = 100;
int b = 200;
```
###### File name: prepinsta.c

```
#include<stdio.h> 
#include<external.h>
int main()
{
  extern int a,b;
  int sum = a + b;
  printf("%d + %d = %d ", a, b, sum);
  return 0;
}
```

output:
```
100 + 200 = 300
```


### Register Storage Class

Variables belonging to register storage class are local to the block in which they are are defined in, and get destroyed on exit from the block.

A register declaration is equivalent to an an auto declaration, but hints that the declared variable will be accessed frequently. If a variable is declared register, then unary & address of operator may not be applied to it, explicitly or implicitly. Register variables are also given no initial value by the compiler.

##### Why do we need Register Storage Class

- Whenever we declare any variable inside C Program then memory will be randomly allocated at particular memory location.
- We have to keep track of that memory location. We need to access value of that memory location using ampersand operator i.e (&).
- If we store same variable in the register memory then we can access that memory location directly without using the Address operator.
- Register variable will be accessed faster than the normal variable thus increasing the operation and program execution.

##### Working & Understanding of Program

- Int number1 and number2 belongs to automatic storage class.
- So they will be stored in memory.
- Register int sum belongs to register storage class, it will be stored in register memory
- There will not be any change in calculation or working of program.
- Program will simply add the two numbers and print their sum.
- If we use sum variable in any other part of program then it will be easily accessible rather then int number1 and number2.

```
#include <stdio.h>
int main()
{
    int number1, number2;
    register int sum;
    printf("\nEnter the Number 1 : ");
    scanf("%d",&number1);
    printf("\nEnter the Number 2 : ");
    scanf("%d",&number2);
    sum = number1 + number2;
    printf("\nSum of Numbers : %d",sum);
    return(0);
}
```

#### Static Storage Class

Static variables can be used within function or file. Unlike global variables, static variables are not variables outside their fucntions or file, but they maintain their values between calls. The static specifier has different effects upon local and global variables.

###### Local Implementation of Static Storage Class

- When a static Specifier is applied to function or block the compiler create permanent storage for it.
- Static Local variable remains visible only to the function or block in which it is defined.
- A Static Local variables is a local variable that retains its value between functions calls.

```
#include <stdio.h>

void countCalls() {
    static int callCount = 0; // Initialized only once
    callCount++;
    printf("This function has been called %d times\n", callCount);
}

int main() {
    countCalls(); // Output: This function has been called 1 times
    countCalls(); // Output: This function has been called 2 times
    countCalls(); // Output: This function has been called 3 times
    return 0;
}

```

###### Global Implementation of Static Storage Class

- When static specifier is applied to a global variable or a function then compiler makes that variable or function known only to the file in which it is defined.
- A static global variable is a global variable with internal linkage.
- That means even the variable is global but other files are not having any knowledge of it.
- Other file cannot access or alter it’s content directly.

```
#include <stdio.h>

static int globalCount = 0; // Accessible only within this file

void incrementCount() {
    globalCount++;
    printf("Global count is now %d\n", globalCount);
}

int main() {
    incrementCount(); // Output: Global count is now 1
    incrementCount(); // Output: Global count is now 2
    return 0;
}
```

- The `globalCount` variable is a file-local global variable, meaning it is accessible only within the file in which it is declared.
- It has internal linkage, meaning it cannot be accessed from other files even if declared using `extern`.
- Use when you want a global variable to be restricted to a single file, to maintain encapsulation and avoid naming conflicts.



# Storage Classes in Simple

Storage classes in C define the scope (visibility) and lifetime of variables and functions within a C program. They determine where the variable is stored, the default initial value, and the duration the variable persists in memory. There are four storage classes in C: `auto`, `register`, `static`, and `extern`. Let's explore each one in detail.

### 1. `auto` Storage Class
- **Scope**: Local to the block in which the variable is defined.
- **Lifetime**: The variable exists only during the execution of the block in which it is defined.
- **Default Initial Value**: Garbage value (undefined).
- **Storage**: RAM.

#### Usage:
The `auto` keyword is used to declare automatic variables, but since it's the default for local variables, it is rarely used explicitly.

```c
void example() {
    auto int x = 10; // `auto` keyword is optional
    int y = 20; // Equivalent to `auto int y = 20;`
}
```

### 2. `register` Storage Class
- **Scope**: Local to the block in which the variable is defined.
- **Lifetime**: The variable exists only during the execution of the block in which it is defined.
- **Default Initial Value**: Garbage value (undefined).
- **Storage**: CPU registers (if available), otherwise treated as `auto`.

#### Usage:
The `register` keyword suggests that the variable be stored in a CPU register for faster access. It is generally used for variables that are heavily used, like loop counters.

```c
void example() {
    register int i;
    for (i = 0; i < 1000; i++) {
        // Loop counter `i` is suggested to be stored in a register.
    }
}
```

#### Note:
- The `register` keyword is a suggestion to the compiler; it is not a command.
- You cannot take the address of a register variable (i.e., `&variable` is not allowed).

### 3. `static` Storage Class
- **Scope**: 
  - Local static: Local to the block in which the variable is defined, but retains its value across function calls.
  - Global static: Local to the file in which the variable or function is defined.
- **Lifetime**: The variable exists for the entire duration of the program.
- **Default Initial Value**: Zero (0) for scalar types.
- **Storage**: RAM.

#### Local Static:
A local static variable retains its value between function calls.

```c
void example() {
    static int count = 0; // Initialized only once
    count++;
    printf("%d\n", count); // Will print incremented value on each call
}
```

#### Global Static:
A global static variable or function is only accessible within the file it is defined in.

```c
static int globalVar = 0; // Not accessible outside this file

static void example() { // Function not accessible outside this file
    globalVar++;
}
```

### 4. `extern` Storage Class
- **Scope**: Global.
- **Lifetime**: The variable exists for the entire duration of the program.
- **Default Initial Value**: Zero (0) for scalar types.
- **Storage**: RAM.

#### Usage:
The `extern` keyword is used to declare a global variable or function in another file.

##### File1.c
```c
int globalVar = 0; // Definition of the global variable

void increment() {
    globalVar++;
}
```

##### File2.c
```c
extern int globalVar; // Declaration of the global variable

void print() {
    printf("%d\n", globalVar);
}
```

### Summary of Key Points
- **auto**: Default for local variables. Limited scope and lifetime.
- **register**: Suggests storage in CPU registers for quick access.
- **static**: 
  - Local static: Retains value between function calls within the block.
  - Global static: Restricts access to the file where defined.
- **extern**: Used to declare global variables or functions defined in another file.

Understanding these storage classes helps in managing the memory, scope, and lifetime of variables effectively, which is crucial for writing efficient and maintainable C programs.



## `Volatile Storage Class`

The volatile storage class in C is used to specify that a variable’s value can be changed by external factors such as hardware devices or other parts of the operating system. This tells the compiler to avoid certain optimization techniques that might be applied to non-volatile variables, because the value of a volatile variable could change at any time.
#### Volatile Storage class in C
Here is an example of how you can use the `volatile` storage class:
`volatile int flag;`
This declares a variable flag of type int that is marked as **volatile.**

The volatile storage class is often used in situations where a variable is accessed by multiple threads of execution or is being modified by hardware devices. In these cases, the compiler cannot assume that the value of the variable will remain constant and must generate code to re-read the value from memory each time it is accessed.
##### Why Use `volatile`?
In optimizing code, compilers often assume that if a variable is not modified within a given scope, its value does not change. This allows the compiler to optimize the code by, for example, storing the value in a register and not re-reading it from memory every time it is accessed. However, if a variable can change unexpectedly, this assumption is incorrect.
##### Example Use Cases:
1. **Hardware Registers in Embedded Systems**: When programming hardware, certain variables correspond to registers in the hardware. These registers can change independently of the program flow.
2. **Interrupt Service Routines (ISRs)**: Variables modified by an ISR need to be marked as `volatile` to ensure the main program reads their updated values.
3. **Multi-threaded Applications**: Variables shared between threads may change at any time due to the actions of another thread.

Consider an embedded system where `STATUS_REGISTER` is a hardware register that can change independently of the program:

```
volatile int STATUS_REGISTER;

void checkStatus() {
    while (STATUS_REGISTER == 0) {
        // Wait for status to change
    }
    // STATUS_REGISTER has changed, proceed with the next steps
}

```
In this example, `STATUS_REGISTER` is declared as `volatile` because its value can change due to hardware events outside the control of the program.
### Without `volatile`
If the `volatile` keyword were omitted, the compiler might optimize the code in such a way that it reads `STATUS_REGISTER` once, stores it in a register, and keeps checking the register value in the loop. This would lead to an infinite loop if `STATUS_REGISTER` were to change due to an external event.




## `Control Statements`

Control statements in C are used to dictate the flow of execution in a program. They enable the programmer to specify conditions for executing statements, looping through statements multiple times, and making decisions based on certain conditions. Here is a detailed explanation of the various control statements in C:

### 1. Conditional Statements

Conditional statements are used to perform different actions based on different conditions.

#### `if` Statement

The `if` statement executes a block of code if the specified condition is true.

```c
if (condition) {
    // Code to execute if condition is true
}
```

Example:

```c
int a = 10;
if (a > 5) {
    printf("a is greater than 5\n");
}
```

#### `if-else` Statement

The `if-else` statement executes one block of code if the condition is true, and another block of code if the condition is false.

```c
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```

Example:

```c
int a = 10;
if (a > 15) {
    printf("a is greater than 15\n");
} else {
    printf("a is not greater than 15\n");
}
```

#### `else if` Ladder

The `else if` ladder is used to check multiple conditions.

```c
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true
} else {
    // Code to execute if none of the above conditions are true
}
```

Example:

```c
int a = 10;
if (a > 15) {
    printf("a is greater than 15\n");
} else if (a > 5) {
    printf("a is greater than 5 but less than or equal to 15\n");
} else {
    printf("a is 5 or less\n");
}
```

#### `switch` Statement

The `switch` statement is used to execute one block of code among many blocks, based on the value of a variable or expression.

```c
switch (expression) {
    case value1:
        // Code to execute if expression equals value1
        break;
    case value2:
        // Code to execute if expression equals value2
        break;
    // More cases...
    default:
        // Code to execute if none of the cases match
}
```

Example:

```c
int a = 2;
switch (a) {
    case 1:
        printf("a is 1\n");
        break;
    case 2:
        printf("a is 2\n");
        break;
    default:
        printf("a is not 1 or 2\n");
}
```

### 2. Looping Statements

Looping statements are used to execute a block of code repeatedly as long as a specified condition is true.

#### `while` Loop

The `while` loop executes a block of code as long as the specified condition is true.

```c
while (condition) {
    // Code to execute as long as condition is true
}
```

Example:

```c
int i = 0;
while (i < 5) {
    printf("%d\n", i);
    i++;
}
```

#### `do-while` Loop

The `do-while` loop is similar to the `while` loop, but it guarantees that the code block is executed at least once because the condition is checked after the code block is executed.

```c
do {
    // Code to execute
} while (condition);
```

Example:

```c
int i = 0;
do {
    printf("%d\n", i);
    i++;
} while (i < 5);
```

#### `for` Loop

The `for` loop is used to execute a block of code a specific number of times. It consists of three parts: initialization, condition, and increment/decrement.

```c
for (initialization; condition; increment/decrement) {
    // Code to execute
}
```

Example:

```c
for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
```

### 3. Jump Statements

Jump statements are used to alter the flow of control unconditionally.

#### `break` Statement

The `break` statement terminates the nearest enclosing loop or `switch` statement.

```c
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break;
    }
    printf("%d\n", i);
}
```

#### `continue` Statement

The `continue` statement skips the remaining code inside the loop for the current iteration and proceeds with the next iteration.

```c
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        continue;
    }
    printf("%d\n", i);
}
```

#### `goto` Statement

The `goto` statement transfers control to the labeled statement.

```c
int main() {
    printf("Hello\n");
    goto label;
    printf("This will be skipped\n");
    label:
    printf("World\n");
    return 0;
}
```

#### `return` Statement

The `return` statement terminates the execution of a function and returns control to the calling function. Optionally, it can return a value.

```c
int sum(int a, int b) {
    return a + b;
}

int main() {
    int result = sum(5, 3);
    printf("Sum is %d\n", result);
    return 0;
}
```

### Summary

Control statements are essential for directing the flow of execution in a C program. By using conditional statements (`if`, `if-else`, `else if`, `switch`), looping statements (`while`, `do-while`, `for`), and jump statements (`break`, `continue`, `goto`, `return`), you can create complex and flexible programs. Understanding how to effectively use these control statements is fundamental to programming in C.


## `Precedence and Associativity`

In C, **precedence** and **associativity** are rules that determine the order in which different operators in an expression are evaluated. Understanding these rules is crucial for writing correct and predictable C code.

### Operator Precedence

Operator precedence determines the order in which different operators are evaluated in an expression. Operators with higher precedence are evaluated before operators with lower precedence.

For example, in the expression `3 + 4 * 5`, the multiplication (`*`) operator has a higher precedence than the addition (`+`) operator, so the expression is evaluated as `3 + (4 * 5)`, which results in `3 + 20` and thus `23`.

Here is a simplified list of C operators in order of precedence (from highest to lowest):

1. **Primary Operators**: `()`, `[]`, `->`, `.`, `++`, `--`
2. **Unary Operators**: `+`, `-`, `!`, `~`, `++`, `--`, `*`, `&`, `sizeof`, `_Alignof`
3. **Binary Multiplicative Operators**: `*`, `/`, `%`
4. **Binary Additive Operators**: `+`, `-`
5. **Shift Operators**: `<<`, `>>`
6. **Relational Operators**: `<`, `<=`, `>`, `>=`
7. **Equality Operators**: `==`, `!=`
8. **Bitwise AND**: `&`
9. **Bitwise XOR**: `^`
10. **Bitwise OR**: `|`
11. **Logical AND**: `&&`
12. **Logical OR**: `||`
13. **Conditional Operator**: `?:`
14. **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `<<=`, `>>=`, `&=`, `^=`, `|=`
15. **Comma Operator**: `,`

### Associativity

Associativity determines the order in which operators of the same precedence are evaluated. Associativity can be either left-to-right or right-to-left.

#### Left-to-Right Associativity

Most binary operators (such as `+`, `-`, `*`, `/`, `%`, `==`, `!=`, `<`, `<=`, `>`, `>=`, `&&`, `||`, `,`) have left-to-right associativity. This means that in an expression with multiple operators of the same precedence, evaluation proceeds from left to right.

For example, in the expression `a - b + c`, both `-` and `+` have the same precedence and left-to-right associativity, so the expression is evaluated as `(a - b) + c`.

#### Right-to-Left Associativity

Some operators (such as assignment `=`, compound assignment `+=`, `-=`, `*=`, `/=`, `%=`, `<<=`, `>>=`, `&=`, `^=`, `|=`, and the conditional operator `?:`) have right-to-left associativity. This means that in an expression with multiple operators of the same precedence, evaluation proceeds from right to left.

For example, in the expression `a = b = c`, the assignment operator `=` has right-to-left associativity, so the expression is evaluated as `a = (b = c)`.

### Examples

#### Example 1: Operator Precedence

```c
int result = 3 + 4 * 5;
```

Here, multiplication (`*`) has higher precedence than addition (`+`), so `4 * 5` is evaluated first, resulting in `20`. Then `3 + 20` is evaluated, resulting in `23`. Therefore, `result` will be `23`.

#### Example 2: Left-to-Right Associativity

```c
int result = 10 - 3 + 5;
```

Subtraction (`-`) and addition (`+`) have the same precedence and left-to-right associativity. Therefore, the expression is evaluated from left to right: `10 - 3` results in `7`, and `7 + 5` results in `12`. Therefore, `result` will be `12`.

#### Example 3: Right-to-Left Associativity

```c
int a, b, c;
a = b = c = 5;
```

The assignment operator (`=`) has right-to-left associativity. Therefore, the expression is evaluated from right to left: `c = 5` is evaluated first, assigning `5` to `c`. Then `b = 5` assigns `5` to `b`, and finally `a = 5` assigns `5` to `a`. Therefore, `a`, `b`, and `c` will all be `5`.

### Summary

- **Operator Precedence**: Determines the order in which different types of operators in an expression are evaluated. Operators with higher precedence are evaluated before operators with lower precedence.
- **Associativity**: Determines the order in which operators of the same precedence are evaluated. Associativity can be either left-to-right or right-to-left.

Understanding these rules helps in writing clear and correct expressions in C and avoids the need for excessive use of parentheses to enforce the desired order of operations.


### `Escape sequences`

Escape sequences in C are used to represent special characters within string literals and character constants. They provide a way to include characters that are not easily typed or are invisible (like a newline) in your code. Each escape sequence starts with a backslash (`\`) followed by one or more characters.

### Common Escape Sequences

Here is a list of commonly used escape sequences in C:

1. **Newline (`\n`)**: Moves the cursor to the beginning of the next line.
   ```c
   printf("Hello\nWorld");
   // Output:
   // Hello
   // World
   ```

2. **Horizontal Tab (`\t`)**: Moves the cursor to the next tab stop.
   ```c
   printf("Hello\tWorld");
   // Output:
   // Hello   World
   ```

3. **Backspace (`\b`)**: Moves the cursor one position back, removing the previous character.
   ```c
   printf("Hello\bWorld");
   // Output:
   // HellWorld
   ```

4. **Form Feed (`\f`)**: Moves the cursor to the beginning of the next logical page. It is rarely used in modern applications.
   ```c
   printf("Hello\fWorld");
   // Output depends on the device and environment
   ```

5. **Carriage Return (`\r`)**: Moves the cursor to the beginning of the current line.
   ```c
   printf("Hello\rWorld");
   // Output:
   // World
   ```

6. **Backslash (`\\`)**: Represents a backslash character.
   ```c
   printf("Hello\\World");
   // Output:
   // Hello\World
   ```

7. **Single Quote (`\'`)**: Represents a single quote character.
   ```c
   printf("It\'s a test");
   // Output:
   // It's a test
   ```

8. **Double Quote (`\"`)**: Represents a double quote character.
   ```c
   printf("Hello \"World\"");
   // Output:
   // Hello "World"
   ```

9. **Question Mark (`\?`)**: Represents a question mark character. It is used to avoid trigraph sequences.
   ```c
   printf("What\?!");
   // Output:
   // What?!
   ```

10. **Octal Number (`\ooo`)**: Represents a character using its octal value.
    ```c
    printf("\101");
    // Output:
    // A (Octal 101 is 65 in decimal, which is 'A' in ASCII)
    ```

11. **Hexadecimal Number (`\xhh`)**: Represents a character using its hexadecimal value.
    ```c
    printf("\x41");
    // Output:
    // A (Hexadecimal 41 is 65 in decimal, which is 'A' in ASCII)
    ```

12. **Null Character (`\0`)**: Represents the null character, used to terminate strings.
    ```c
    char str[] = "Hello\0World";
    printf("%s", str);
    // Output:
    // Hello (the null character terminates the string)
    ```

### Practical Examples

#### Example 1: Using Newline and Tab

```c
#include <stdio.h>

int main() {
    printf("Name\tAge\nJohn\t25\nJane\t30\n");
    return 0;
}
```
**Output**:
```
Name    Age
John    25
Jane    30
```

#### Example 2: Using Backslash and Quotes

```c
#include <stdio.h>

int main() {
    printf("She said, \"Hello, World!\"\n");
    printf("C:\\Program Files\\MyApp\n");
    return 0;
}
```
**Output**:
```
She said, "Hello, World!"
C:\Program Files\MyApp
```

### Summary

Escape sequences in C allow for the inclusion of special characters in strings and character constants. They enhance the readability and maintainability of code by enabling the representation of characters that are otherwise difficult or impossible to include directly. By mastering escape sequences, you can handle strings and characters more effectively in your C programs.



## `void* in C vs C++`

The `void*` is a type of pointer that points to an area of memory holding data of an unknown type. It is often used as a genetic type for passing pointers around in a code, since it can hold the address of any type of object

The **`void*`** type behaves similarly in both C and C++, as it is used to represent a pointer to an area of memory that holds data of an unknown type. However, there are a few key differences between the way **`void*`** is used in these two languages:

1. In C++, **`void*`** can be used as the type of a function parameter or return value, while in C it cannot. In C, you must use a specific pointer type instead.
2. In C++, **`void*`** can be explicitly converted to and from any other pointer type using the static_cast operator. In C, you must use a type cast to perform this conversion.
3. In C++, **`void*`** cannot be dereferenced directly. You must first cast it to a pointer of a specific type before you can use it to access the data it points to. In C, you can dereference a **`void*`** pointer using a type cast.

Note:Overall, void* is a more powerful and flexible construct in C++ than in C, but it is also more prone to error if used improperly. It is generally recommended to use specific pointer types or templates in C++ instead of void* wherever possible.


```
void *p;
int *int_ptr = (int *) p;
int *arr_ptr = (int *) malloc(sizeof(int) * 10);
```

**In C:**
```
#include <stdio.h>

// Function that takes a void* argument and prints the value it points to
void print_value(void* p) {
  
  // Must cast void* to a pointer of a specific type before dereferencing
  int* q = (int*)p;
  printf("%d\n", *q);
}

int main() {
    
  int x = 10;
  // Assign address of x to a void* pointer
  
  void* p = &x;
  // Pass void* pointer to function as argument
  
  print_value(p);  
  return 0;
}
```
In the C example, the print_value function does the same thing, but uses a type cast instead of the static_cast operator to convert the **`void*`** to an **`int*`**.

**In C++:**
```
#include <iostream>
using namespace std;

// Function that takes a void* argument and prints the value it points to
void print_value(void* p) {
    
  // Must cast void* to a pointer of a specific type before dereferencing
  int* q = static_cast(p);
  
  cout << *q << endl;
}

int main() {
    
  int x = 10;
  
  // Assign address of x to a void* pointer
  void* p = &x;
  
  // Pass void* pointer to function as argument
  print_value(p);  
  
  return 0;
}
```

In the C++ example, the print_value function takes a `**void***` argument and prints the value it points to by first casting the pointer to an **`int*`** and then dereferencing it.


### `scanf` and `printf`

`scanf` and `printf` are standard input and output functions in the C programming language, provided by the `stdio.h` library. They are fundamental for interacting with the user, taking input, and displaying output. Let's dive deeper into both functions.

### `printf` Function

The `printf` function is used for output. It sends formatted output to the standard output (usually the terminal).

#### Syntax:
```c
int printf(const char *format, ...);
```

- `format` is a string that specifies how subsequent arguments are converted for output.
- The `...` indicates a variable number of arguments that will be formatted and printed according to the `format` string.

#### Format Specifiers:
Format specifiers are placeholders within the `format` string. They are replaced by the values of the corresponding arguments. Common format specifiers include:

- `%d` or `%i`: Integer (signed)
- `%u`: Unsigned integer
- `%f`: Floating-point number
- `%lf`: Double-precision floating-point number
- `%c`: Single character
- `%s`: String
- `%p`: Pointer address
- `%x` or `%X`: Unsigned hexadecimal integer

#### Example:
```c
int main() {
    int age = 25;
    float height = 5.9;
    char initial = 'A';
    printf("Age: %d, Height: %.1f, Initial: %c\n", age, height, initial);
    return 0;
}
```

- Here, `printf` prints the age as an integer, the height as a floating-point number with one decimal place, and the initial as a character.

#### Return Value:
`printf` returns the total number of characters written, excluding the null byte used to end output to strings. If an output error occurs, it returns a negative value.

### `scanf` Function

The `scanf` function is used for input. It reads formatted input from the standard input (usually the keyboard).

#### Syntax:
```c
int scanf(const char *format, ...);
```

- `format` is a string that specifies how the input should be interpreted.
- The `...` indicates a variable number of arguments where the input values will be stored.

#### Format Specifiers:
Similar to `printf`, `scanf` uses format specifiers to determine the type of data to read and store. Common format specifiers include:

- `%d` or `%i`: Reads an integer
- `%u`: Reads an unsigned integer
- `%f`: Reads a floating-point number
- `%lf`: Reads a double-precision floating-point number
- `%c`: Reads a single character
- `%s`: Reads a string (up to the first whitespace character)

#### Example:
```c
int main() {
    int age;
    float height;
    char initial;
    printf("Enter age, height, and initial: ");
    scanf("%d %f %c", &age, &height, &initial);
    printf("Age: %d, Height: %.1f, Initial: %c\n", age, height, initial);
    return 0;
}
```

- Here, `scanf` reads an integer, a floating-point number, and a character from the user and stores them in `age`, `height`, and `initial`, respectively.

#### Return Value:
`scanf` returns the number of input items successfully matched and assigned. This can be used to check for input errors. If an error occurs or the end of the file is reached before any items are matched, `scanf` returns `EOF`.

#### Notes on Usage:

1. **Address of Variables**: When using `scanf`, you must provide the address of the variables where the input values should be stored. This is done using the `&` operator.
2. **Buffer Overflows**: Be careful with `%s` format specifier, as it does not check the length of the input string, which can lead to buffer overflows. Use field width specifiers or `fgets` to mitigate this risk.
3. **White Space Handling**: `scanf` skips white space automatically for most format specifiers, except `%c`. To skip leading white spaces when reading a character, use a space before `%c` like this: `" %c"`.

### Example Program

Combining both `printf` and `scanf` in a simple program:

```c
#include <stdio.h>

int main() {
    int age;
    float height;
    char name[50];

    printf("Enter your name: ");
    scanf("%49s", name); // Limiting input to avoid buffer overflow

    printf("Enter your age: ");
    scanf("%d", &age);

    printf("Enter your height in meters: ");
    scanf("%f", &height);

    printf("Name: %s, Age: %d, Height: %.2f meters\n", name, age, height);

    return 0;
}
```

In this example, the user is prompted to enter their name, age, and height. `scanf` reads these values and stores them in the respective variables, and `printf` then prints these values in a formatted manner. The `%49s` in the `scanf` function limits the input string length to 49 characters, providing a simple measure against buffer overflow.

By understanding and using `scanf` and `printf` effectively, you can manage user input and output in your C programs efficiently.



## `Operators`

The operators is a symbol that tells the computer to perform some mathematical or logical operation.

- In the programming, operators are used to manipulate data and variables.
- The combination of operands and operators is called expression.
- Operands are variables that perform some operations in conjunction with the operators.
### Types of operators

- **Unary operator:-** These types of operators are used only with one operand.
- **Binary operator:-** These types of operators are used with two operands.

### Arithmetic operator

- The arithmetic operators is used to perform mathematical operations like addition, subtraction division and multiplication etc.
- Below is a list for the type and function of these operators. Assume A=5 and B=10

|Operator|Function performed by operator|Example|
|---|---|---|
|+|Adds two operands(float, integer etc.)|A + B = 15|
|−|Subtracts  2nd operand from the 1st one.|A − B = -5|
|*|Multiplies the operands.|A * B = 50|
|/|Divides numerator by denominator.|B / A = 2|
|%|Returns remainder after dividing 1st operand with second one.|B % A = 0|
|++|Increment operator increases the integer value by one.|++A = 6|
|—|Decrement operator decreases the integer value by one.|A– = 4|
### Relational operator

- Relational operators are used to compare values of two variables.
- As you can use these operators, you can find out, whether the values of any two variables are equal or not.
- If not equal, then the value of which variable is big and which variable’s value is small.
- Such operators are used with conditional statements.
- These operators are used to check the condition.
- when the condition is true, the value becomes true and the values becomes false when the condition is false.
- All the relational operators that are being used in C language are given below. Assume 

|Operator|Function performed by operator|Example|
|---|---|---|
|==|Compares if the values of two operands are equal or not. If yes, then the condition becomes true, false otherwise.|(A == B) is not true.|
|!=|Compares if the values of two operands are equal or not. If the values are not equal, then the condition becomes true, false otherwise.|(A != B) is true.|
|>|Compares if the value of left operand is greater than the value of right operand. If yes, then the condition becomes true, false otherwise.|(A > B) is not true.|
|<|Compares if the value of left operand is less than the value of right operand. If yes, then the condition becomes true, false otherwise.|(A < B) is true.|
|>=|Compares if the value of left operand is greater than or equal to the value of right operand. If yes, then the condition becomes true, false otherwise.|(A >= B) is not true.|
|<=|Compares if the value of left operand is less than or equal to the value of right operand. If yes, then the condition becomes true, false otherwise.|(A <= B) is true.|

### Logical operator

- The logic gate can be applied (finds application in mathematical operations too) with these operator.
- Logical operators are used with decision making statements.
- These operators are used to check two condition together in control statements.
- The table about logical operators is being given. Assume A=5, B=10.

| Operator | Function performed by operator                                                                                                                      | Example                   |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| &&       | Logical AND operator. If both the conditions are satisfied then the condition becomes true .                                                        | (A>8 && B==10) is false.  |
| \|\|     | Logical OR Operator. If any of the conditions are satisfied, then the condition becomes true.                                                       | (A>8 \| B==10) is true.   |
| !        | Logical NOT Operator. It is used to reverse the logical state of its operand. If a condition is true, then Logical NOT operator will make it false. | !(A>8 \| B==10) is false. |


### Bitwise operator

- The Bitwise operators work on bits of a integer value.
- Bitwise operators are used to perform bit level operations on given variables.
- The decimal values of the variables are converted to bits.
- After this the operations are performed on those bits, to understand it lets recall some basics :-

|p|q|p & q|p \| q|
|---|---|---|---|
|0|0|0|0|
|0|1|0|1|
|1|1|1|1|
|1|0|0|1|

- Assume A = 50 and B = 10 in binary, they can be written as:
- A = 0011 0010 B = 0000 1010
- And bitwise comparison A&B= 0000 0010
- OR bitwise comparison A|B=0011 1010
- And then assume A=50, B=10

|Operator|Function performed by operator|Example|
|---|---|---|
|&|Binary AND Operator copies a bit to the result if it exists in both operands else copies zero.|(A & B) = 2|
|\||Binary OR Operator copies a bit if it exists in either operand.|(A \| B) = 58|
|^|Bitwise exclusive OR Operator. If the corresponding bit of any of the operand is 1 then the output would be 1, otherwise 0.|(A ^ B) = 56|
|~|Binary compliment operator i.e.- 0 changes to 1 and 1 to 0|(~A ) = -51|
|<<|Binary Left shift Operator which rotates the number of bits to the left by specified positions as mentioned on the right.|A << 2 = 200|
|>>|Binary Right Rotation Operator which rotates the number of bits to right by specified positions as mentioned on the right.|A >> 2 = 12|

### Assignment operator

- Assignment operators are used to assign values of variables to each other.
- The operator which changes the value of the operands themselves, here is how they work.

|Operator|Function performed by operator|Example|
|---|---|---|
|=|Simple assignment operator. Assigns values from right side operands to left side operand|C = A + B will assign the value of A + B to C|
|+=|Add AND assignment operator. It adds the right operand to the left operand and assign the result to the left operand.|C += A is equivalent to C = C + A|
|-=|Subtract AND assignment operator. It subtracts the right operand from the left operand and assigns the result to the left operand.|C -= A is equivalent to C = C – A|
|*=|Multiply AND assignment operator. It multiplies the right operand with the left operand and assigns the result to the left operand.|C *= A is equivalent to C = C * A|
|/=|Divide AND assignment operator. It divides the left operand with the right operand and assigns the result to the left operand.|C /= A is equivalent to C = C / A|
|%=|Modulus AND assignment operator. It takes modulus using two operands and assigns the result to the left operand.|C %= A is equivalent to C = C % A|
|<<=|Left shift AND assignment operator.|C <<= 2 is same as C = C << 2|
|>>=|Right shift AND assignment operator.|C >>= 2 is same as C = C >> 2|
|&=|Bitwise AND assignment operator.|C &= 2 is same as C = C & 2|
|^=|Bitwise exclusive OR and assignment operator.|C ^= 2 is same as C = C ^ 2|
|\|=|Bitwise inclusive OR and assignment operator.|C \|= 2 is same as C = C \| 2|

###  Misc operator

- There are a few more miscellaneous operator worth mentioning

|Operator|Function performed by operator|Example|
|---|---|---|
|sizeof()|Returns the size of a variable.|sizeof(a), for an integer value, it returns 4.|
|&|Returns the address of a variable.|&a; returns the address of the memory location of variable.|
|*|Pointer to a variable.|*a;|
|? :|Conditional Expression.|If Condition is true ? then value X : otherwise value Y|


### `Comma operator`

- Comma Operator has Lowest Precedence i.e it is having lowest priority so it is evaluated at last.
- The comma operator (also called  token, ) is a binary operator that works on first operand and discards the result, it then evaluates the second operand and returns their value (and type)
- First of all we know already Comma operator can be used as a “separator” .
eg; int a=3, b=4, c=7 is nothing but multiple definition a in single line. we can  also write,
	int a=3;
	int b=4;
	int c=7;
but is in that combination.

- Comma operator can be used as a operator, 
eg; 
	int a =(3,4,8);
	printf(“%d”,a);
- Comma operator returns the right most operand in the expression and it simple evaluates the rest of the operands and finally reject them.
- Comma operator is having least precedence among all the operators available in C language.
- Symbol of Comma Operator is **(,) .**

##### Implementation of Comma operator

- Comma Operator has Lowest Precedence i.e it is having lowest priority so it is evaluated at last.
- So Firstly ‘=’ operator priority is high,then initially var =15 was evaluated and the second operand becomes var+35 == 15+35
- which results 50. now 50 will be printed.

```
#include <stdio.h>  // header files

int main()
{
int var;
int num;

num= (var=15, var+35);
printf("%d",num);
}

// output:
// 50
```



## `Macros`

Macro is a preprocessor which comes under `#define` directive.
Macro is small part of code which replaces the variable of macro to the value of macro where that macro is used in the program.
Macro is very helpful when user wants to change the value of value of a variable at multiple positions. There are different type of macros.

#### Macros in C and Types of Macros

Macro is segment of code or in simple words a small part of code which replaces the name of macro to the value of macro.
Macros are defined by the `#define` directive.
It is a preprocessor. Preprocessor is software program that processes the source file prior to sending it to actual compilation.

#### Types of Macros

- Object-Like Macros
- Function-Like Macros

##### Object-Like Macros in C:

Its is widely used to represent numeric constant. Basic syntax of object-like macro is “#define a 10 “.Where `#define` is a preprocessor directive a is macro name and 10 is macro value.

```
#include <stdio.h>
#define DATE 25	  // Object-Like Macro
int main ()
{

  printf ("Christmas is celebrated world wide on %d-DEC", DATE);

  return 0;
}
```

o/p:\
```
Christmas is celebrated world wide on 25-DEC
```


##### Function-Like Macros in C:

Its replaces the value of macro name with macro function.It looks like a function call.It substitute the entire code in place of function name.

For Example: `#define` min(a,b) (((a)< (b)) ? (a) : (b) ).Here min(a,b) is function name which replaces with the code given everywhere in the program.

```
#include<stdio.h> 

//object like macro
#define PI 3.14

// function like macro
#define Ar(r) (PI*(r*r))

void main ()
{

  float rad = 4.5;
  float area = Ar (rad);

  printf ("Area of circle is %f\n", area);

  int radInt = 7;
  printf ("Area of circle is %f", Ar (radInt));

}
```
o/p:
```
Area of circle is 63.584999
Area of circle is 153.860000
```

##### Predefined Macros
Here some of the macros which are predefined in C language.

| Macro      | Value                                                            |
| ---------- | ---------------------------------------------------------------- |
| `__DATE__` | A string containing the current date.                            |
| `__FILE__` | A string containing the file name.                               |
| `__LINE__` | An integer representing the current line number.                 |
| `__STDC__` | If follows ANSI standard C, then the value is a nonzero integer. |
| `__TIME__` | A string containing the current time.                            |

Macros in C are a powerful feature provided by the preprocessor, which allow you to define constants and functions for use throughout your code. They are handled by the preprocessor before the actual compilation of the code begins. Macros can simplify code, make it more readable, and allow for more flexible and reusable code constructs.

### Types of Macros

There are two primary types of macros in C:

1. **Object-like Macros**: These are simple text replacements.
2. **Function-like Macros**: These take arguments and can be used to create inline code.

### Defining and Using Macros

#### Object-like Macros

Object-like macros are the simplest type of macros. They are defined using the `#define` directive and are typically used to create named constants or to simplify repetitive code.

#### Syntax:
```c
#define NAME replacement_text
```

#### Example:
```c
#define PI 3.14159
#define MAX_BUFFER_SIZE 1024

int main() {
    float radius = 5.0;
    float area = PI * radius * radius;
    char buffer[MAX_BUFFER_SIZE];

    // Your code here...

    return 0;
}
```

- In this example, `PI` and `MAX_BUFFER_SIZE` are object-like macros. Whenever `PI` or `MAX_BUFFER_SIZE` appears in the code, they are replaced with `3.14159` and `1024`, respectively.

#### Function-like Macros

Function-like macros are more complex and can take arguments, making them more flexible and powerful.

#### Syntax:
```c
#define NAME(arg1, arg2, ...) replacement_text_with_args
```

#### Example:
```c
#define SQUARE(x) ((x) * (x))
#define MAX(a, b) ((a) > (b) ? (a) : (b))

int main() {
    int num = 5;
    int max_num = MAX(10, 20);
    int square_num = SQUARE(num);

    printf("Max: %d, Square: %d\n", max_num, square_num);

    return 0;
}
```

- Here, `SQUARE(x)` and `MAX(a, b)` are function-like macros. When used, `SQUARE(num)` expands to `((num) * (num))` and `MAX(10, 20)` expands to `((10) > (20) ? (10) : (20))`.

### Advantages and Disadvantages

#### Advantages:
1. **Code Reusability and Simplification**: Macros can make code shorter and easier to read by eliminating repetitive code.
2. **Performance**: Since macros are replaced by their definitions before compilation, they can be faster than function calls because they avoid the overhead of a function call.
3. **Flexibility**: Macros can be used to define constants, inline functions, and conditional compilation.

#### Disadvantages:
1. **Debugging Difficulty**: Errors in macros can be harder to track down because they are replaced by the preprocessor before compilation.
2. **Lack of Type Safety**: Macros do not provide type checking, which can lead to unexpected behavior if not used carefully.
3. **Maintenance**: Overuse of macros can make code harder to read and maintain, especially for larger projects.

### Conditional Compilation

Macros can also be used for conditional compilation, allowing different parts of the code to be compiled based on certain conditions.

#### Example:
```c
#define DEBUG

int main() {
    int x = 10;

#ifdef DEBUG
    printf("Debug: x = %d\n", x);
#endif

    // Your code here...

    return 0;
}
```

- In this example, the `DEBUG` macro controls whether the debug print statement is included in the compilation. If `DEBUG` is defined, the print statement is included; otherwise, it is excluded.

### Common Predefined Macros

The C preprocessor provides several predefined macros that can be useful in various situations:

- `__FILE__`: Expands to the current file name.
- `__LINE__`: Expands to the current line number.
- `__DATE__`: Expands to the current date as a string.
- `__TIME__`: Expands to the current time as a string.
- `__STDC__`: Defined as `1` when the compiler complies with the ANSI standard.

#### Example:
```c
#include <stdio.h>

int main() {
    printf("File: %s, Line: %d\n", __FILE__, __LINE__);
    printf("Compiled on: %s at %s\n", __DATE__, __TIME__);

    return 0;
}
```

- This example demonstrates how to use predefined macros to print the current file name, line number, compilation date, and time.

### Macro Pitfalls and Best Practices

While macros are powerful, they can lead to issues if not used carefully. Here are some best practices to avoid common pitfalls:

1. **Use Parentheses**: Enclose macro arguments in parentheses to ensure correct evaluation order.
   ```c
   #define SQUARE(x) ((x) * (x))
   ```

2. **Avoid Side Effects**: Be cautious of macros that evaluate their arguments multiple times, which can lead to side effects.
   ```c
   #define BAD_SQUARE(x) (x * x)
   int y = 3;
   int z = BAD_SQUARE(y++); // This will increment y twice, leading to unexpected results
   ```

3. **Use Inline Functions**: For complex macros, consider using `inline` functions instead, which provide type safety and avoid some pitfalls of macros.
   ```c
   inline int square(int x) {
       return x * x;
   }
   ```

4. **Documentation and Naming**: Use clear and descriptive names for macros and document their usage to improve code readability and maintainability.

By understanding and using macros effectively, you can leverage their power to simplify your C code and enhance its flexibility.

## Types of Garbage Value :

There are four types of garbage value in C :

- Uninitialized variables
- Out of bound array access.
- Unused Memory
- Global Variables

Garbage value refers to the value stored in the memory of the variable without being initialized or declared a proper value. 

Using Garbage value in the program can lead to unpredictable and unwanted output of the program. For proper functioning of the code, garbage value should be managed properly.

## `Type Conversion in C`

#### C – Type Conversion

Type conversion is a procedure by which a data type can be converted into any other possible data types.The task of type conversion in C is to be performed by the compiler at the time of compilation. In this process, the data type in which the existing data type wants to be converted should be higher than the existing data type.  

#### There are two types of Type Conversions:

- **Implicit Type Conversion**   This type of conversion is done by the compiler on its own without any external command or code and thus, also known as automatic type conversion. All the data types are converted to the highest data type of any given expression .
- **Explicit Type Conversion** This type of conversion is to be done from the user end by writing code for the same and thus, also known as type casting. By using the syntax for type casting, a data type can be converted into any specified data type..

Note: There is one major drawback of data loss in implicit type conversion as some data could be lost forever while being converted to a higher data type.

##### Syntax of Explicit conversion:

```
(data_type)expression;
```


#### Example of Implicit Conversion:

```
#include<stdio.h>
int main()
{
    int x = 10;
    char y = 'a'; 
    x = x + y;
    float z = x + 1.0;
    printf("x = %d, z = %f", x, z);
    return 0;
}
```
Output:
```
x = 107, z = 108.000000
```

#### Example of Explicit Conversion:

```
#include<stdio.h>
int main()
{
    double x = 1.2;
    int sum = (int)x + 4;
    printf("sum = %d", sum);
    return 0;
}
```
Output:
```
sum = 5
```



