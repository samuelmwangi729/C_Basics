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
meaning that its going to stop at the preprocessing stage and that you can view your program and note of any change. When the required libraries are included in your basic program, you file looks like  [this one here](./codes/hello.i)
#### 2. Compiling
In this stage, the assembly code is produced by the compiler using the command 
```bash
gcc -S hello.c -o hello.asm
```
The resulting file is visible [here](./codes/hello.asm) and you can see different sections of the assembly file. Running the file command gives the output as `hello.asm: assembler source, ASCII text`
#### 3. Assembling
This converts the assembly file produced into an object code(machine readable). The command to view the object code will be 
```bash 
gcc -c hello.c -o hello.o
```
you can view the resulting file [here](./codes/hello.o)
Running the file command against the file gives you the output `hello.o: ELF 64-bit LSB relocatable, x86-64, version 1 (SYSV), not stripped` meaning the binary is not stripped
#### 4. Linking
This is done to bind or connect the object code with the required libraries so that they can execute seamlessly. This is done using the command 
```bash 
gcc hello.o -o hello
```
the file command gives the file as an executable with the output as 
`hello: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=8213af3beff17a44635782ef5e0a1ce52cdc1732, for GNU/Linux 3.2.0, not stripped`

_finally, the file produced is an executable that can be executed and run in any environment._