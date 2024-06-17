


# `Structures`

- A structure is a very user friendly data type which lets the user define the types of different data which can be stored in the structure, i.e we can store integer, float, character, and string in one place(under one identifier). 
- The elements saved in a structure are called it’s members. 
- It is widely used to store student information like name, age, marks and other such data in one structure. 
- Structure is the same as an array. The difference is that, In array we can store same type of data but in structure  we can store different type of data.

### Defining the Structure

Struct keyword is used to define the structure. After this keyword the structure is given the unique name. After this, variables are created in curly braces and semicolon is applied after the ending curly bracket.

```
struct struct_Name
{
   Structure member 1;
   Structure member 2;
    ...
  Structure member N;
};
```

```
struct Student
{
   int stu_id;
   char stu_name[10];
   int stu_age;
   char stu_branch;
};
```


### Structure Variable Declaration

Structure variables can be declared in two ways:-
1. Structure variable is written even when the definition of structure is written.
2. The variable of the structure is also done inside the main() function.

### Syntax  for  Structure  variable outside of structure definition

```
struct structure_name
{
   data_type member 1;
   data_type member 2;
      ......
   data_type member n;
}structure_variable(s);
```

example:
```
struct structure_name
{
   data_type member 1;
   data_type member 2;
      ......
   data_type member n;
}structure_variable(s);
```

#### Syntax for structure variable in main() function.

```
struct structure_name
{
   data_type member 1;
   data_type member 2;
            ......
   data_type member n;
}structure_variable(s);
int main()
{
struct structure_name structure_variable_name;
}
```

example:

```
struct Student
{
   int stu_id;
   int stu_age;
   char stu_name[10];
   char stu_branch[10];
};
int main()
{
struct Student info;
}
```

### Accessing Structure members

It can be assigned to values in many ways. Without the structure the members of the structure have no personal meaning. To provide a value to a member of any structure, the member name must be connected with the structure variables using dot(.). The operator is also called the term or member access operator.

### Syntax for Accessing Structure Members

`structure_variable_name.member_of _structure =value(optional);`

```
#include<stdio.h>
#include<conio.h>
struct Student
{
    char  stu_name[10];
    int  stu_age;
    char stu_branch;
    int stu_id;
};
int main()
{
    struct Student s1;    // s1 is a variable of Student type and
    s1. stu_age=17; //age is a member of student
    strcpy(s1.stu_name,"Somya"); // using string function to add name
    printf("Name of student 1:%s\n", s1. stu_name);
    printf("Age of student 1:%d\n", s1.stu_age);
    return 0;
}
```

### Structure Initialization

- The  structure initialization is of two type.
- we can also initialize the structure variable at compile time.

**TYPE 1:-**

```
struct Student
{
  float height;
  int weight;
  int age;
};
struct Student s1 = { 180.75 , 73, 23 }; //initialization 
```

**TYPE 2:-**

```
struct Student s1;
s1.height = 182.5 ; //initialization of each member separately
s1.weight = 65;
s1.age = 20;
```

### Array of Structure

We can create an array of structure like other primitive data types. In which each element of array will represent a structure variable.

### Example

`struct student stu[5];`

```
#include<stdio.h>
struct Student
{
  char name[10];
  int id;
};
struct Student stu[5];
int i, j;
void ask ()
{
  for (i = 0; i < 3; i++)
    {
      printf ("enter %d Student record:\n", i + 1);
      printf ("Student name: \t");
      scanf ("%s", stu[i].name);
      printf ("\nenter  id:\t");
      scanf ("%d", &stu[i].id);
    }
  printf ("\ndisplaying Student record:");
  for (i = 0; i < 3; i++)
    {
      printf ("Student name is %s", stu[i].name);
      printf ("id is %d", stu[i].id);
    }
}

void main ()
{
  ask ();
}
```


# `Union`

C provides us a special data type and that data type is called Union. Union can store many data types in the same memory location. We can create variables of different data types inside a Union. Unions are similar to structures in C language. The difference between these is that every member of the structure occupies a separate memory location and the size of them all is different while in the Union the members occupy the same memory space and the size depends on the size of the largest member.


### Union

- Union is the collection of different data types
- If we want to use Union ,use of ‘union’ keyword is mandatory.
- Every declaration done inside a union is called member.
- A single memory location is shared among the members of the Union.
- The biggest in size among the members decides the size of the Union.

### Defining a union

To define a Union, ‘union’ keyword is used. It is same as defining a structure.

The basic **syntax of union** is as follows :

```
union union_name
{
    data_type var1;
    data_type var2;
    ..
    ..
    data_type varn;
};
```
First we define union keyword with a unique union name. After this we define variables of different data types in curly brackets.

```
union Employee
{
    int emp_id;
    char emp_name[30];
    float salary;
};
```

Now in the above example we can see that the name of the union is taken as ‘Employee’ and there are three members of the Union- emp_id, emp_name and salary. Now variables can be declared for the union and every variable will have three members which will have a shared memory location.



# `Static vs Dynamic`


In C programming, the terms "static" and "dynamic" generally refer to different methods of allocating memory for variables and data structures. Here’s a detailed comparison:

### Static Memory Allocation

1. **Definition**:
   - Static memory allocation refers to the process where memory for variables is allocated at compile-time.
   - The size and location of memory are fixed and known before the program runs.

2. **Lifetime**:
   - The memory allocated remains throughout the lifetime of the program.
   - Variables with static memory allocation are stored in the data segment of memory.

3. **Scope**:
   - Variables can be either local to a function or global to the program, but the memory is allocated when the program starts and deallocated when the program ends.
   - Static variables inside a function retain their value between function calls.

4. **Syntax**:
   ```c
   static int x; // Static local variable
   int y; // Static global variable (by default in C)
   ```

5. **Efficiency**:
   - Static allocation is generally faster as it doesn't require runtime allocation.
   - However, it is less flexible because the size must be known at compile-time and cannot change during execution.

6. **Usage**:
   - Useful for variables that need to retain their value across function calls or are used globally across the program.

### Dynamic Memory Allocation

1. **Definition**:
   - Dynamic memory allocation refers to the process where memory is allocated at runtime.
   - The size and location of memory can be determined during the execution of the program.

2. **Lifetime**:
   - The memory allocated dynamically exists until it is explicitly freed.
   - It is managed through the heap segment of memory.

3. **Scope**:
   - Memory is accessible via pointers.
   - It allows creating data structures whose size can change during the program's execution.

4. **Syntax**:
   ```c
   int *ptr = (int*)malloc(sizeof(int)); // Allocate memory
   free(ptr); // Deallocate memory
   ```

5. **Efficiency**:
   - More flexible, allowing programs to handle varying amounts of data.
   - However, it involves overhead due to the need for allocation and deallocation at runtime and can lead to fragmentation and potential memory leaks if not managed properly.

6. **Usage**:
   - Useful for data structures like linked lists, trees, and graphs where the size can vary dynamically.
   - Appropriate for large datasets or when the required size is not known at compile time.

### Summary

- **Static Memory Allocation**: Fixed size, compile-time allocation, remains for the program's lifetime, faster but less flexible.
- **Dynamic Memory Allocation**: Variable size, runtime allocation, exists until explicitly freed, more flexible but requires careful management.

In essence, choosing between static and dynamic memory allocation depends on the specific needs of your program. Static allocation is simpler and faster when the size is known and fixed, while dynamic allocation provides the flexibility needed for more complex, variable-sized data structures.



# `File handling in C`

File Handling is very useful while storing your data in the storage device permanently, File Handling in C is storing up of data in a file by the use of C programming.

Sometimes when data is very large it cannot be displayed, due to some console limitation. In these type of condition File handling is used in C programming to help you deal with these problems.

There are mainly 2 types of file that are there in C programming, they are as follows:

- Text File
- Binary File


**Text File:** These files are normal test file written in notepad and can be easy understood by a normal person who knows how to read. These files uses “.txt” extension to store in your memory. 

**Binary File:** These files are in the form of 0’s and 1’s. Text files are converted into Binary files so that it could be easily understood and accessed  by the computer. These files occupy lesser space in the memory and uses the extension of “.bin”.

### **Steps For using a File in your C program**

- Creating a new file pointer
- Using fopen() function to open a File
- Processing the file using various methods and functions.
- Using fclose() to close the file.

There are various modes in which a file can be accessed , they are mentioned below in the table:

| S.No | Mode | Description                                                                                                                                            |
| ---- | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1    | r    | Used to open a text file in READ mode. The file must exist.                                                                                            |
| 2    | w    | Used to open a text file in WRITING mode. Creates an empty file if it doesn't exist. If it exists, the contents are erased.                            |
| 3    | a    | Used to open a text file in APPEND mode. Creates the file if it doesn't exist. The data is added to the end of the file.                               |
| 4    | r+   | Used to open text file in both READ and WRITE mode and this mode cannot create a new file if it doesn’t exist.                                         |
| 5    | w+   | Used to open text file in both READ and WRITE mode and this mode can create a new file if it doesn’t exist. Existing data will be overwritten by this. |
| 6    | a+   | Used to open text file in both READ and WRITE mode and this mode can create a new file if it doesn’t exist. Existing data will not be overwritten.     |

### **Function used in File Handling in C programming**

There are various pre-defined functions that you can use in C library. They all have unique functions and can be used according to use. Some of the functions are mentioned bellow:

| S.No | Function  | Description                                                                             |
| ---- | --------- | --------------------------------------------------------------------------------------- |
| 1    | fopen()   | It is used to open a new file or edit an existing file.                                 |
| 2    | fprintf() | It is used to write a set of data into the file.                                        |
| 3    | fscanf()  | It is used to read strings from the file.                                               |
| 4    | putc()    | It is used to write a particular single character as per the requirement into the file. |
| 5    | getc()    | It is used to return(read) a single character from a specific available file.           |
| 6    | fseek()   | It is used in setting the file cursor to an intended given position.                    |
| 7    | fputw()   | It is used to insert a particular integer into an available file in write mode.         |
| 8    | fgetw()   | It is used to read a particular integer value from a given file.                        |
| 9    | fclose()  | It is used to close the open program file.                                              |
| 10   | rewind()  | It is used in setting the file cursor at the beginning of the intended file.            |

#### opening file 

```
#include<stdio.h>
int main(){
   FILE * nfile;
   if (nfile = fopen("hello.txt", "r")){
      printf("File opened successfully in read mode");
   }
   else
   printf("The file is not present! cannot create a new file using r mode");
   fclose(nfile);
   return 0;
}
```


```
#include<stdio.h>
int main(){
   FILE * nfile;
   char string[300];
   if (nfile = fopen("hello.txt", "a+")){
      while(fscanf(nfile,"%s", string)!=EOF){
         printf("%s", string);
      }
      fputs("Hello", nfile);
   }
   fclose(nfile);
   return 0;
}
```


### Working with files in C

To work with files in C, you need to use the file input and output functions provided in the C standard library through the stdio.h header file. These functions allow you to read from and write to files in your C program.

Here are the steps to follow when working with files in C:

1. Include the stdio.h header file at the top of your C program.
2. Declare a pointer to a FILE type. This pointer will be used to refer to the open file.
3. Use the `fopen()` function to open the file. This function takes the name of the file and the mode in which the file should be opened (such as “r” for reading or “w” for writing) as arguments, and returns a pointer to a FILE type.
4. Check if the file was successfully opened. If the `fopen()` function returns `NULL`, it means that the file could not be opened.
5. Use the file input and output functions to read from or write to the file. Some of the most commonly used functions are `fgetc()` for reading a single character, `fgets()` for reading a line of text, `fprintf()` for writing formatted output, and `fputc()` and `fputs()` for writing a single character or a string, respectively.
6. Use the `fclose()` function to close the file when you are done. This releases any resources that were allocated for the file.


```c
#include <stdio.h>

int main() {
   // Declare a file pointer
   FILE *fp;

   // Open the file for reading
   fp = fopen("input.txt", "r");

   // Check if the file was successfully opened
   if (fp == NULL) {
      printf("Error opening file\n");
      return 1;
   }

   // Declare a character array to store the contents of the file
   char buffer[100];

   // Read the contents of the file into the buffer
   fgets(buffer, 100, fp);

   // Print the contents of the buffer
   printf("%s", buffer);

   // Close the file
   fclose(fp);

   return 0;
}
```

## **fprintf() & fscanf() in C programming**

**fprintf()-** It is used to write content or string into a file instead of stdout console.

**fscanf()-** It is used to read content or string from a file pointed by a file pointer into the stream.


```
#include<stdio.h>
int main (void) 
{
   FILE *new;
   new = fopen("sample.txt","w");
   fprintf(fileName, "%s %s %d", "Welcome", "to",  2023);
   fclose(New);
   return 0;
}
```


```
#include<stdio.h>  
main(){  
   FILE *new;  
   char b[255];
   new = fopen("sample.txt", "r");  
   while(fscanf(new, "%s", b)!=EOF){  
   printf("%s ", b );  
   }  
   fclose(new);  
}
```

## **fputc() & fgetc() in C programming:**

- **fputc()-** It is used to write a single character into an already opened file, i.e. to a specified stream. Its writes a given character at the position given by the file pointer into a file.
- **fgetc()-** It is used to get a single character from the file into the output console. It returns the character present at the pointer and displays it.


```
#include<stdio.h>

int main () {
   FILE *new;
   int character;

   new = fopen("file.txt", "w+");
   for( character = 19 ; character <= 100; character++ ) {
      fputc(character, new);
   }
   fclose(new);

   return(0);
}
```



```
#include<stdio.h>
#include<conio.h>
void main()
{  
    FILE *new;  
    char character;  
    clrscr();  
    new=fopen("sample.txt","r");  
    while((character=fgetc(new))!=EOF)
    {  
        printf("%c",character);  
    }  
    fclose(new);  
    getch();  
}
```


```
#include<stdio.h>
int main()
{
    int i = 0;
    FILE *new = fopen("test.txt","w");
    if (new == NULL)
    {
        return 0;
    }
    char string[] = "good bye", rec_string[20];
    for (i = 0; string[i]!='\0'; i++)
    {
        fputc(string[i], new);
    }
    fclose(new);
    newf = fopen("test.txt","r");
    fgets(rec_string,20,new);
    printf("%s", rec_string);
    fclose(newf);
    return 0;
}
```

```
good bye
```


## fseek() function in C programming:

fseek() function of file handling in C language is used to change the file pointer from a specific file position to the requested location. This function helps in faster modification of file contents.After the file pointer has shifted to a specified offset, you can perform any operation like writing, reading from the file according to your requirement or wish. This helps to write data into file at requested location.

#### There are various parts of this syntax which are mentioned below:

- **Pointer-** It is used to point to the File object that helps to find the stream in which data is to be written.
- **Offset-** It represents the number of bytes to the offset from the specified position.
- **Position-** It specifies the position according to which the file pointer needs to be moved and from where the offset is to be added.There are 3 values which are

1. SEEK_END – It represents the end of file.
2. SEEK_SET – It represents the start of file.
3. SEEK_CUR – It represents the current position of the file pointer.



```
#include<stdio.h>
int main (void) 
{
   FILE *new;
   new = fopen("sample.txt","w");
   fseek( new , 7, SEEK_SET ); 
   fclose(new);
   return 0;
}
```

The above code sets the pointer of the file 7 places ahead from the start of the file using the SEEK_SET argument.


```
#include
int main (void) 
{
   FILE *new;
   new = fopen("sample.txt","w");
   fseek( new , 0, SEEK_END ); 
   fclose(new);
   return 0;
}
```

The above code sets the pointer of the file to the end location of the file using the SEEK_END argument.


## **rewind() in C programming**

**rewind() function**  is used to set the file pointer or indicator associated with the stream to the beginning of  the given stream or file.

```
#include<stdio.h>
int main()
{
    int i;
    FILE *rewi;
    rewi = fopen("file.txt", "r");
    if (rewi)
    {
        while ((i = getc(rewi)) != EOF)
        {
            putchar(i);
        }
        rewind(rewi);
        putchar('\n');
        while ((i = getc(rewi)) != EOF)
        {
            putchar(i);
        }
    }
    fclose(rewi);
    return 0;
}
```



# `Dynamic Memory Allocation`


### `Memory Layout of C Program`

In C after compiling a program, the compiler creates a binary executable file (.exe).
This executable file stores and loads in systematic manner in computer RAM.

## Memory Layout of C consists of following segments:

1. Text/code segment
2. Initialized data segment 
3. Uninitialized data segment 
4. Heap 
5. Stack 
6. Command-line arguments

![[Pasted image 20240617185758.png]]


## **Detailed explanation of each segment**

**1. Text/code segment :** In object file or memory text segment is one of the sections which contains executable instructions. Moving onwards we know that text segment is also known as Code segment or simply text.  
Text segment is used to prevent heaps and stack overflows and overwriting it by placing it below the heap or stack.

**2. Initialized data segment :** Initialized data segment also known as data segment is present in the virtual memory space of computer.It can store all global,static,constant and external variables.since the values of the variables can be altered at run time data segment is not read-only .  
All the variables come under read-write area except const variable where as const variable comes under the read-only area.


```
#include <stdio.h>
char a[] = "Anurag";		/* read-write area */
const char p[] = "PrepInsta";	/* read-only area */
int main ()
{
  static int j = 15;
  return 0;
}
```

**3. Uninitialized data segment :** Uninitialized data segment stores all the uninitialized global, local and external variables. Another name for the uninitialized data segment is “.bss segment.” The .bss segment stands for Block Started by symbol.  
Before the C program executes, the kernel initialized each and every data in bss segment to arithmetic 0 and pointers to null pointer. Static variable are also part of bss segment that are initialized to 0.


```
#include <stdio.h >
char p;				/*  variable(Uninitialized) stored in bss */
int main ()
{
  static int q;			/*  variable stored(Uninitialized static) in bss */
  return 0;
}
```

**4. Heap :** For dynamic memory allocation Heap memory segment is used.Memory allocation in Heap segment is done  using malloc, calloc , realloc and free  functions. The heap segment initiates at the end of the BSS segment and grows to larger addresses from there.

```
#include<stdio.h>
int main ()
{
  int *st = (int *) malloc (sizeof (int));	//heap memory is allocated.
}
```

**5. Stack :** Stack segment grows in opposite  to heap . It uses Last-In-First-Out (LIFO)  manner  to store local variables. All recursive functions uses stack for implementation.Recursive functions are those which calls itself again and  again. Stack plays an important role in the memory as a new stack frame is created every time a function is called as it is used for passing arguments to functions along with return address of instructions.



## `Malloc()`

A memory block of specified size is allocate at runtime by malloc. A pointer of void type is returned by malloc function which can be convert into pointer of any type.

**Array** is used to store the items of same data types at a contiguous memory location. But if we don’t know the amount of size we required there is chance of wastage of storage if the elements inserted in array are lesser than the size allocated.

So to avoid this problem  the concept of **dynamic memory** allocation comes in play. **malloc()** is a predefined function inside **stdlib. h** header file.
Malloc() allocate a large block of memory of specifies size at run time.
It returns a pointer of void type which can be converted to any type of pointer.

**Syntax**
```
ptr = (cast-type*) malloc(byte-size)
```

![[Pasted image 20240617190443.png]]

**Note**: Its is necessary to deallocate the return pointer with free() or realloc() to avoid memory leak.


```c
#include <stdio.h>
#include <stdlib.h>
int main ()
{
  int a, j, *ptr, s = 0;

  printf ("Enter number of elements: ");
  scanf ("%d", &a);

  ptr = (int *) malloc (a * sizeof (int));

  if (ptr == NULL)
    {
      printf ("Error! memory cannot be allocated.");
      return 0;
    }

  printf ("Enter the elements: ");
  for (j = 0; j < a; ++j)
    {
      scanf ("%d", ptr + j);
      s += *(ptr + j);
    }

  printf ("Sum of elements = %d ", s);

  free (ptr);			// deallocation of memory

  return 0;
}
```
**Output:**
```
Enter number of elements: 4
Enter elements: 10
12
8
6
Sum = 36
```


## `Calloc()`
 calloc( )  is used  contiguous block of memory at run time   those memory block are initialized to zero. calloc() return the base address of allocated memory on successful allocation. calloc function is similar as malloc function.

The calloc function  is used to allocate multiple memory block of same size in contiguous manner at run time .That is why calloc( ) is also know as contiguous allocation.The only difference between **calloc and malloc** is of intialization.In calloc the each memory block when allocated  is initialized with zero.  
The **calloc ( )** is predefined function which comes under stdlib.h .It returns a NULL pointer in case of failure of memory allocation. **Calloc function** has two parameter first is number of blocks and second is size of each block.  
On successful allocation of memory a pointer is returned containing the base address of allocated memory. Otherwise in case of failure of memory allocation **NULL pointer** is returned.

**Syntax:** 
```
ptr = (cast_type *) calloc (a, s);  
```
(where ‘a’ is number of blocks and s is size of each memory block.)

**Note**: To avoid memory leak we must deallocate the return pointer with free() or realloc().

```c
#include <stdio.h>
#include <stdlib.h>

int main ()
{

  int *ptr;			//pt to hold base address of memory block allocated
  int a, j;

  a = 5;			//number of elements in block
  printf ("Enter number of elements: %d\n", a);

  ptr = (int *) calloc (a, sizeof (int));	//syntax of calloc
  if (ptr == NULL)
    {
      printf ("Memory not allocated.\n");
      return 0;
    }

  printf ("Memory allocated successful.\n");

  for (j = 0; j < a; ++j)
    {
      ptr[j] = j + 1;
    }

  printf ("The elements of the array are: ");
  for (j = 0; j < a; ++j)
    {
      printf ("%d, ", ptr[j]);
    }

  return 0;
}
```

**Output:**
```
Enter number of elements: 5
Memory allocated successful.
The elements of the array are: 1, 2, 3, 4, 5
```


## `Realloc()`

Realloc function is also know as reallocation. As the name suggests realloc function is use to re-allocate the data from old memory  block to new memory block. Basically realloc function is used to add more memory to the previously allocated memory block.

**Realloc( )** function is used to change the size of the memory block without losing the old data. It is a built in function declared in stdlib.h . As the name itself suggests **realloc( )** means reallocation.

**Syntax:**
```
void*realloc(void*ptr, newsize);
```

As we can see from the synatx realloc( ) will return a void pointer.Apart from this,It requires two arguments.The first is a pointer to the previously allocated memory and the another one is new size.On failure, realloc( ) returns NULL pointer.

**Example:**

```
int *ptr=(int*)malloc(sizeof(int));
ptr=(int*)realloc(ptr,2*sizeof(int));
```
In the above example, let’s say we have malloc( ) function which allocates memory for one integer. If we use the realloc( ) function in this case the pointr to the previously allocated memory is required and second argument is new size.

**Some more Information:**
- This will allocate memory space of 2\*sizeof(int) (i.e twice of what previously allocated)
- Also this function moves the content of old block to a new memory block and the data of old block is not lost.
- We may lose the data when the new size is smaller than the old size.
- The bytes which are allocated newly by realloc function will not get initialized.

```c
#include <stdio.h>
#include <stdlib.h>

int main ()
{
  int *ptr;
  int a, j;
  a = 6;			//number of elements

  ptr = (int *) calloc (a, sizeof (int));	//run time allocation

  if (ptr == NULL)
    {
      printf ("Memory not allocated.\n");
      exit (0);
    }
  else
    {
      printf ("Memory successfully allocated using calloc.\n");
      for (j = 0; j < a; ++j)
	{
	  ptr[j] = j + 1;
	}
      printf ("The elements of the array are: ");
      for (j = 0; j < a; ++j)
	{
	  printf ("%d, ", ptr[j]);
	}
      a = 12;			//new size

      ptr = realloc (ptr, a * sizeof (int));	//reallocation using realloc()

      printf ("\nMemory successfully re-allocated using realloc.\n");

      for (j = 5; j < a; ++j)
	{
	  ptr[j] = j + 1;
	}
      printf ("The elements of the array are: ");
      for (j = 0; j < a; ++j)
	{
	  printf ("%d, ", ptr[j]);
	}

      free (ptr);		//deallocate the pointer
    }

  return 0;
}
```
**Output**
```
Memory successfully allocated using calloc.
The elements of the array are: 1, 2, 3, 4, 5, 6, 
Memory successfully re-allocated using realloc.
The elements of the array are: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12,
```

### **Malloc()**

- The memory allocation function, or malloc(), allocates a block of memory in a dynamic manner.
- It returns the null pointer, which corresponds to the memory address, and reserves the memory space for the provided size.
- A memory block of specified size is allocate at run time by malloc.
- A pointer of void type is returned by malloc function which can be convert into pointer of any type.

### **Calloc()**

- The dynamic memory allocation in C can be done by using the calloc function.
- The Calloc function makes it possible to allocate memory in many blocks of the same size.
- It is defined in the stdlib.h header file.
- Every memory block was initially set to zero by the calloc() function.

### **Realloc()**

- The C library’s realloc() function allows you to increase the size of memory blocks that have already been allocated.
- Realloc is a function in C that allows you to increase the size of existing memory blocks without changing their content.
- The realloc() function aids in shrinking memory that has previously been allocated using the malloc or calloc procedures.
- The block’s contents are unaltered up to the smaller of the two sizes.

### **Important Note :**

- Realloc( ) function is used to change the size of the memory block without losing the old data.
- It is a built in function declared in stdlib.h .As the name itself suggests realloc( ) means reallocation.



Dynamic memory allocation in C is a technique that allows programs to allocate memory at runtime, rather than at compile-time. This enables the creation of data structures whose size can change during the execution of a program, such as linked lists, trees, and dynamic arrays. The C standard library provides several functions for dynamic memory allocation, all of which are declared in the `stdlib.h` header file.

### Key Functions for Dynamic Memory Allocation

1. **`malloc`**
2. **`calloc`**
3. **`realloc`**
4. **`free`**

#### 1. `malloc` (Memory Allocation)
The `malloc` function allocates a specified number of bytes and returns a pointer to the first byte of the allocated memory block. The content of the allocated memory block is not initialized and may contain garbage values.

**Syntax:**
```c
void *malloc(size_t size);
```

- `size`: The number of bytes to allocate.

**Example:**
```c
int *ptr;
ptr = (int *)malloc(10 * sizeof(int)); // Allocate memory for 10 integers
if (ptr == NULL) {
    // Handle allocation failure
}
```

#### 2. `calloc` (Contiguous Allocation)
The `calloc` function allocates memory for an array of elements, initializes them to zero, and then returns a pointer to the first byte of the allocated memory block.

**Syntax:**
```c
void *calloc(size_t num, size_t size);
```

- `num`: The number of elements.
- `size`: The size of each element.

**Example:**
```c
int *ptr;
ptr = (int *)calloc(10, sizeof(int)); // Allocate and initialize memory for 10 integers
if (ptr == NULL) {
    // Handle allocation failure
}
```

#### 3. `realloc` (Reallocation)
The `realloc` function changes the size of a previously allocated memory block. It can expand or shrink the size of the block, and it may move the block to a new location if necessary.

**Syntax:**
```c
void *realloc(void *ptr, size_t size);
```

- `ptr`: A pointer to the previously allocated memory block. If `ptr` is `NULL`, `realloc` behaves like `malloc`.
- `size`: The new size in bytes.

**Example:**
```c
int *ptr;
ptr = (int *)malloc(10 * sizeof(int)); // Initial allocation
ptr = (int *)realloc(ptr, 20 * sizeof(int)); // Reallocate to a larger size
if (ptr == NULL) {
    // Handle reallocation failure
}
```

#### 4. `free` (Deallocation)
The `free` function deallocates the memory previously allocated by `malloc`, `calloc`, or `realloc`. It does not change the value of the pointer, but the memory pointed to by the pointer is no longer valid.

**Syntax:**
```c
void free(void *ptr);
```

- `ptr`: A pointer to the memory block to be deallocated.

**Example:**
```c
free(ptr); // Deallocate the memory
ptr = NULL; // Avoid dangling pointer
```

### Best Practices for Dynamic Memory Allocation

1. **Check for Allocation Failures:**
   Always check the return value of `malloc`, `calloc`, and `realloc` to ensure that memory allocation was successful.
   ```c
   int *ptr = (int *)malloc(10 * sizeof(int));
   if (ptr == NULL) {
       fprintf(stderr, "Memory allocation failed\n");
       exit(1);
   }
   ```

2. **Avoid Memory Leaks:**
   Always `free` dynamically allocated memory when it is no longer needed.
   ```c
   free(ptr);
   ptr = NULL; // Set the pointer to NULL to avoid dangling pointer
   ```

3. **Initialize Allocated Memory:**
   Use `calloc` to allocate and initialize memory to zero, or explicitly initialize memory after allocation with `malloc`.

4. **Realloc and Data Preservation:**
   When using `realloc`, ensure that if the reallocation fails, the original memory block is not lost.
   ```c
   int *new_ptr = (int *)realloc(ptr, 20 * sizeof(int));
   if (new_ptr == NULL) {
       // Handle reallocation failure, ptr is still valid
   } else {
       ptr = new_ptr; // Update the pointer if reallocation was successful
   }
   ```

5. **Use of `size_t`:**
   Always use `size_t` for sizes and counts to avoid issues with data types and portability.
   ```c
   size_t num_elements = 10;
   int *ptr = (int *)malloc(num_elements * sizeof(int));
   ```

### Common Use Cases for Dynamic Memory Allocation

1. **Dynamic Arrays:**
   Dynamic memory allocation allows the creation of arrays whose size can change during runtime.
   ```c
   int n;
   printf("Enter the number of elements: ");
   scanf("%d", &n);
   int *arr = (int *)malloc(n * sizeof(int));
   // Use the array
   free(arr);
   ```

2. **Data Structures:**
   Dynamic memory is essential for implementing data structures like linked lists, trees, and graphs.
   ```c
   struct Node {
       int data;
       struct Node *next;
   };
   
   struct Node *head = (struct Node *)malloc(sizeof(struct Node));
   head->data = 1;
   head->next = NULL;
   ```

3. **Buffers:**
   Dynamic allocation is useful for handling variable-sized data buffers, such as reading lines of unknown length from a file.
   ```c
   char *buffer = NULL;
   size_t bufsize = 0;
   getline(&buffer, &bufsize, stdin); // Allocate and read a line
   free(buffer);
   ```

By understanding and properly using dynamic memory allocation, you can write more flexible and efficient C programs that can handle a wide range of scenarios and data sizes.



In C programming, as in other programming languages, the terms "runtime" and "compile time" refer to different stages in the lifecycle of a program. Understanding these concepts is crucial for effective programming and debugging.

### Compile Time

**Compile time** is the phase during which the source code of a program is converted into executable code by a compiler. This phase occurs before the program is run. Several key activities and concepts are associated with compile time:

1. **Syntax Checking**:
   - The compiler checks the source code for syntax errors. Syntax errors are mistakes in the use of the programming language's rules.
   - Example: Missing semicolons, incorrect variable declarations, and mismatched parentheses.

2. **Semantic Analysis**:
   - The compiler checks for semantic errors, which are mistakes in the logical use of language constructs.
   - Example: Type mismatches, undeclared variables, and scope errors.

3. **Optimization**:
   - The compiler optimizes the code to improve performance and reduce the size of the executable. This may include loop unrolling, inlining functions, and removing dead code.

4. **Code Generation**:
   - The compiler generates the machine code or bytecode that can be executed by the computer.

5. **Linking**:
   - The linker combines object files (generated by the compiler) into a single executable file, resolving symbol references between them.
   - Example: Combining your code with library code.

6. **Error Detection**:
   - Errors detected during compile time prevent the program from compiling successfully and need to be fixed before the program can run.

### Example of Compile Time Error:
```c
int main() {
    int x = "hello"; // Type mismatch error
    return 0;
}
```
The compiler will generate an error because you cannot assign a string to an integer variable.

### Runtime

**Runtime** is the phase during which the compiled program is executed by the computer. This occurs after the program has been successfully compiled. Several key activities and concepts are associated with runtime:

1. **Execution**:
   - The program's instructions are executed on the CPU. This includes fetching instructions, decoding them, and executing them.

2. **Dynamic Memory Allocation**:
   - Memory is allocated during runtime using functions like `malloc`, `calloc`, and `realloc`. The program may also deallocate memory using `free`.

3. **I/O Operations**:
   - The program may perform input and output operations, such as reading from or writing to files, or interacting with the user via the console.

4. **Runtime Errors**:
   - Errors that occur during the execution of the program. These are typically not detectable at compile time.
   - Example: Division by zero, null pointer dereferencing, array index out of bounds, and invalid memory access.

5. **Program State**:
   - The program maintains its state, including variable values, stack frames, and heap usage, while it runs.

6. **Exception Handling**:
   - In languages that support exception handling, exceptions may be thrown and caught to handle unexpected situations.

### Example of Runtime Error:
```c
#include <stdio.h>

int main() {
    int arr[3] = {1, 2, 3};
    printf("%d\n", arr[4]); // Out of bounds access
    return 0;
}
```
The program will compile successfully, but when it runs, it may crash or produce unexpected output because it is accessing an array element out of bounds.

### Key Differences Between Compile Time and Runtime

1. **Error Detection**:
   - **Compile Time**: Errors are detected by the compiler. These include syntax errors, type mismatches, undeclared variables, etc.
   - **Runtime**: Errors are detected when the program is running. These include logical errors, invalid memory access, division by zero, etc.

2. **Memory Allocation**:
   - **Compile Time**: Memory allocation for static variables and constants is determined.
   - **Runtime**: Memory allocation for dynamic variables and structures occurs.

3. **Optimization**:
   - **Compile Time**: Code optimization by the compiler.
   - **Runtime**: Code execution; no further optimizations (though runtime environments or just-in-time compilers may perform some optimizations).

4. **Debugging**:
   - **Compile Time**: Easier to fix syntax and semantic errors since they are reported by the compiler.
   - **Runtime**: Harder to debug because errors occur during program execution and may depend on the specific inputs and program state.

Understanding the distinction between compile time and runtime is essential for writing robust and efficient programs, as well as for effective debugging and optimization.


The process of transforming C source code into an executable program involves several stages: compilation, linking, and execution. Here’s a detailed explanation of each step:

### Compilation Process

1. **Preprocessing**:
   - The source code is processed by the preprocessor.
   - This step handles directives like `#include`, `#define`, and conditional compilation.
   - The result is a modified source code with all macros expanded and file inclusions processed.

   **Example**:
   ```c
   #include <stdio.h>
   #define PI 3.14
   int main() {
       printf("Value of PI: %f\n", PI);
       return 0;
   }
   ```

   After preprocessing:
   ```c
   // stdio.h contents included here
   int main() {
       printf("Value of PI: %f\n", 3.14);
       return 0;
   }
   ```

2. **Compilation**:
   - The preprocessed code is converted into assembly code by the compiler.
   - This step checks for syntax and semantic errors.
   - The output is a file with a `.s` extension (assembly code).

   **Example**:
   ```asm
   _main:
       push rbp
       mov rbp, rsp
       ...
       call _printf
       ...
       pop rbp
       ret
   ```

3. **Assembly**:
   - The assembly code is translated into machine code (binary code) by the assembler.
   - The result is an object file with a `.o` or `.obj` extension.

   **Example**:
   ```binary
   48 89 e5 48 83 ec 20 48 8d 3d ...
   ```

4. **Linking**:
   - The object files and libraries are combined into a single executable file by the linker.
   - This step resolves references to external symbols and functions.
   - The result is an executable file (e.g., `a.out` on Unix-like systems, `a.exe` on Windows).

### Example of the Compilation Process
Assuming we have a simple program in `main.c`:

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

To compile and link this program using `gcc`:

```sh
gcc main.c -o main
```

The steps involved:
1. **Preprocessing**: `gcc -E main.c -o main.i` produces the preprocessed file `main.i`.
2. **Compilation**: `gcc -S main.i -o main.s` produces the assembly file `main.s`.
3. **Assembly**: `gcc -c main.s -o main.o` produces the object file `main.o`.
4. **Linking**: `gcc main.o -o main` produces the executable `main`.

### Execution Process

After the program is compiled and linked, the resulting executable can be run. This involves several stages:

1. **Loading**:
   - The operating system loads the executable into memory.
   - The loader sets up the memory space for the program, including the code, data, and stack segments.

2. **Execution**:
   - The CPU begins executing the program starting from the entry point, typically the `main` function in a C program.
   - The program runs, performing the tasks it was designed to do, such as reading inputs, processing data, and producing outputs.

3. **Runtime Environment**:
   - During execution, the runtime environment manages resources such as memory, file handles, and input/output operations.
   - Functions from standard libraries (e.g., `printf`, `malloc`) are used to interact with the operating system and hardware.

4. **Termination**:
   - The program terminates when the `main` function returns or an exit function (like `exit`) is called.
   - The operating system reclaims the resources used by the program.

### Example of Program Execution

For the compiled executable `main`:

```sh
./main
```

The steps involved during execution:
1. **Loading**: The operating system loads the `main` executable into memory.
2. **Execution**: The program starts running, and the `printf` function prints "Hello, World!" to the console.
3. **Termination**: The program returns 0, indicating successful completion, and the operating system cleans up.

### Summary of the Entire Process

1. **Source Code** (`main.c`):
   ```c
   #include <stdio.h>

   int main() {
       printf("Hello, World!\n");
       return 0;
   }
   ```

2. **Preprocessing**:
   - Processed by the preprocessor, expanding macros and including headers.

3. **Compilation**:
   - Translated to assembly code, checking for syntax and semantic errors.

4. **Assembly**:
   - Assembly code converted to machine code in an object file.

5. **Linking**:
   - Object file(s) combined into an executable, resolving external references.

6. **Execution**:
   - Executable loaded into memory, run by the CPU, performing tasks and producing outputs.

7. **Termination**:
   - Program completes, returning control and resources to the operating system.

Understanding these steps helps in debugging, optimizing, and effectively managing the lifecycle of a C program.




The basic structure of a C program consists of several components that together form a complete, executable piece of software. Here’s an overview of the fundamental elements typically found in a C program:

### Basic Structure of a C Program

1. **Header Files Inclusion**
2. **Macro Definitions**
3. **Global Variable Declarations**
4. **Function Declarations**
5. **Main Function**
6. **Other Functions**

### 1. Header Files Inclusion
Header files contain declarations for functions and macros provided by the C standard library or other libraries. Including header files allows the program to use these pre-defined functions and macros.

**Example:**
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
```

### 2. Macro Definitions
Macros are defined using the `#define` preprocessor directive. They allow the definition of constants or macro functions.

**Example:**
```c
#define PI 3.14159
#define SQUARE(x) ((x) * (x))
```

### 3. Global Variable Declarations
Global variables are declared outside of any function and are accessible to all functions within the program.

**Example:**
```c
int globalVar = 10;
```

### 4. Function Declarations
Function declarations (also known as function prototypes) provide the compiler with information about the functions used in the program. This includes the return type, the function name, and the parameters.

**Example:**
```c
void myFunction(int a, float b);
int add(int x, int y);
```

### 5. Main Function
The `main` function is the entry point of every C program. Execution starts from the `main` function. It typically has a return type of `int` and returns a status code to the operating system.

**Example:**
```c
int main() {
    // Code to be executed
    printf("Hello, World!\n");
    return 0; // Indicates successful completion
}
```

### 6. Other Functions
Other functions are defined to perform specific tasks. These functions are called from the `main` function or from other functions.

**Example:**
```c
void myFunction(int a, float b) {
    // Function implementation
    printf("a: %d, b: %.2f\n", a, b);
}

int add(int x, int y) {
    return x + y;
}
```

### Complete Example
Here is a complete example that includes all the basic elements of a C program:

```c
#include <stdio.h>  // Header file for standard input and output functions
#include <math.h>   // Header file for math functions

#define PI 3.14159      // Macro definition for PI
#define SQUARE(x) ((x) * (x))  // Macro definition for calculating the square of a number

// Global variable declaration
int globalVar = 10;

// Function declarations
void printCircleArea(float radius);
int add(int x, int y);

int main() {
    // Local variable declaration
    int num1 = 5, num2 = 7;
    
    // Calling a function to add two numbers
    int sum = add(num1, num2);
    printf("Sum: %d\n", sum);

    // Calling a function to print the area of a circle
    float radius = 3.5;
    printCircleArea(radius);

    return 0;  // Return 0 to indicate successful completion
}

// Function definitions

// Function to print the area of a circle
void printCircleArea(float radius) {
    float area = PI * SQUARE(radius);
    printf("Area of the circle with radius %.2f is %.2f\n", radius, area);
}

// Function to add two integers
int add(int x, int y) {
    return x + y;
}
```

### Explanation of the Example

1. **Header Files Inclusion**:
   - `#include <stdio.h>`: Includes the Standard Input Output library.
   - `#include <math.h>`: Includes the Math library for mathematical functions.

2. **Macro Definitions**:
   - `#define PI 3.14159`: Defines a macro for the value of π.
   - `#define SQUARE(x) ((x) * (x))`: Defines a macro for calculating the square of a number.

3. **Global Variable Declarations**:
   - `int globalVar = 10;`: Declares a global variable `globalVar`.

4. **Function Declarations**:
   - `void printCircleArea(float radius);`: Declares the function `printCircleArea`.
   - `int add(int x, int y);`: Declares the function `add`.

5. **Main Function**:
   - The `main` function is where the program execution begins.
   - It declares local variables `num1`, `num2`, and `radius`.
   - Calls the `add` function to compute the sum of `num1` and `num2`.
   - Calls the `printCircleArea` function to print the area of a circle with the given `radius`.
   - Returns 0 to indicate successful completion.

6. **Other Functions**:
   - `printCircleArea(float radius)`: Computes and prints the area of a circle given its radius.
   - `add(int x, int y)`: Returns the sum of two integers.

This example illustrates a simple but complete C program, showing how the basic components fit together.


In C programming, `#include`, `#`, and preprocessor directives are integral parts of the preprocessing stage, which occurs before the actual compilation of the code. Let's delve into what these elements are and how they function.

### Preprocessor and Preprocessor Directives

The preprocessor is a tool that processes your source code before it is passed to the compiler. Preprocessor directives are commands given to the preprocessor to perform specific operations on the source code. They all start with the `#` symbol. 

### Common Preprocessor Directives

1. **`#include`**
2. **`#define`**
3. **Conditional Compilation (`#if`, `#ifdef`, `#ifndef`, `#else`, `#elif`, `#endif`)**
4. **`#undef`**
5. **`#pragma`**

#### 1. `#include`

The `#include` directive is used to include the contents of a file (typically a header file) into the source file at the point where the directive appears. This allows for code modularity and reuse. There are two types of `#include` directives:

- **Standard Library Header Files**:
  - Syntax: `#include <header.h>`
  - Example: `#include <stdio.h>`
  - The angle brackets (`< >`) indicate that the file is located in the system's standard library directory.

- **User-defined Header Files**:
  - Syntax: `#include "header.h"`
  - Example: `#include "myheader.h"`
  - The double quotes (`" "`) indicate that the file is located in the current directory or the directories specified by the compiler's include path.

**Example:**
```c
#include <stdio.h> // Includes the standard input-output library
#include "myheader.h" // Includes a user-defined header file
```

#### 2. `#define`

The `#define` directive is used to define macros, which are constants or macro functions that the preprocessor replaces with their corresponding values or code.

- **Constant Macros**:
  - Syntax: `#define name value`
  - Example: `#define PI 3.14159`

- **Function-like Macros**:
  - Syntax: `#define name(parameters) code`
  - Example: `#define SQUARE(x) ((x) * (x))`

**Example:**
```c
#define PI 3.14159
#define SQUARE(x) ((x) * (x))
```

#### 3. Conditional Compilation

Conditional compilation directives control the compilation process based on specified conditions. These are useful for including or excluding parts of code, typically for debugging or platform-specific code.

- `#if`, `#else`, `#elif`, `#endif`:
  - Example:
    ```c
    #if defined(DEBUG)
    printf("Debug mode\n");
    #else
    printf("Release mode\n");
    #endif
    ```

- `#ifdef`, `#ifndef`:
  - Example:
    ```c
    #ifdef DEBUG
    printf("Debug mode\n");
    #endif

    #ifndef RELEASE
    printf("Not in release mode\n");
    #endif
    ```

#### 4. `#undef`

The `#undef` directive is used to undefine a macro, effectively removing its definition.

**Example:**
```c
#define PI 3.14159
#undef PI // PI is now undefined
```

#### 5. `#pragma`

The `#pragma` directive provides machine-specific or operating system-specific features. The behavior of `#pragma` varies between different compilers.

**Example:**
```c
#pragma once // Ensures the header file is included only once during compilation
```

### The `#` Symbol

The `#` symbol at the beginning of a line indicates that the line is a preprocessor directive. This symbol tells the preprocessor to perform a specific operation before the actual compilation of the code.

### Example of Preprocessor Directives in a C Program

Here is a complete example illustrating the use of various preprocessor directives:

```c
#include <stdio.h>    // Standard library header file inclusion
#include "myheader.h" // User-defined header file inclusion

#define PI 3.14159        // Macro definition for a constant
#define SQUARE(x) ((x) * (x)) // Macro definition for a function-like macro

int main() {
    printf("Value of PI: %f\n", PI);
    printf("Square of 5: %d\n", SQUARE(5));

    #ifdef DEBUG
    printf("Debug mode is enabled\n");
    #endif

    return 0;
}
```

### Explanation:

1. **`#include <stdio.h>`**: Includes the standard I/O library functions.
2. **`#include "myheader.h"`**: Includes a user-defined header file.
3. **`#define PI 3.14159`**: Defines a constant macro for PI.
4. **`#define SQUARE(x) ((x) * (x))`**: Defines a function-like macro to calculate the square of a number.
5. **`#ifdef DEBUG`**: Conditionally includes the code within the block if `DEBUG` is defined.

These elements are fundamental to writing C programs, enabling modular code, code reuse, and conditional compilation for various build configurations.