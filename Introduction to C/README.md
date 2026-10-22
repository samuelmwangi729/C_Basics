# Introduction to C Programming language & its significance in Cyber Security.


C is a compiled language where a toolchain is used to convert it to machine language.It gives you direct control of the memory and that is what the <b>Operating System</b> requires a reason why the operating system is written using it.

### Why in Cyber Security?
---
1. Worlds most vulnerable code is as a result of poorly written C
2. Understanding the Ins of a compiled binary allows you to reverse engineer and elf binary

#### How to compile a C program
Given the code below, compilation is done under a series of steps as indicated. In this case, we will be using a simple hello world program in C as included here.
```C
#include<stdio.h>
int main(void){
    printf("hello world\n");
    return 0;
}
```

The stages include.

#### 1. Preprocess
This allows the inclusion of the pre processor files that tell the program what files are required for the program to run. Under this, few lines of codes becomes hundreds or more as many other files codes will be included in your code.
The command used in this case is 
```bash
gcc -E hello.c -o hello.i
 ```
 meaning that its going to stop at the preprocessing stage and that you can view your program and note of any change.
#### 2. Compiling
#### 3. Assembling
#### 4. Linking