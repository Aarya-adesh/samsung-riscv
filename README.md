# samsung-riscv
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

# Basic Details

Name: AARYAADESH

College: Vidyavardhaka College of Engineering

Email ID: rajuaarya30@gmail.com

GitHub Profile: Aarya-adesh

LinkedIN Profile: Aarya adesh

<details>
<summary><b>Task 1:</b> Task 1: Review videos on C programming and RISC-V architecture, and compile C code using GCC and RISC-V compilers to demonstrate understanding of each process.simulator</summary>   
<br>

# C Programming and RISC-V Architecture Lab

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

## C Language-Based Lab

### Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   gedit sum_1ton.c
   ```
3. Compile and run the program:
   ```sh
   gcc sum_1ton.c
   ./a.out
   ```

## RISC-V Based Lab

### Steps to Compile Using RISC-V GCC Compiler:
1. Ensure the RISC-V GCC compiler is installed and accessible on your system.
2. Verify the .c file contents using the cat command:
   ```sh
   cat sum_1ton.c
   ```
3. Compile the C program for RISC-V architecture:
   ```sh
   riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
   ```
4. Disassemble the object file to view its assembly code:
   ```sh
   riscv64-unknown-elf-objdump -d sum_1ton.o
   ```
5. Use /main in the terminal to locate the main function in the assembly output.

### Explanation of Key Commands and Options:
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types
2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture
3. -O1: Enables basic optimization for better performance
4. riscv64-unknown-elf-objdump: Tool for disassembling RISC-V binaries
</details>

<details>
<summary><b>Task 2:</b> Task 2: The task involves reviewing C and RISC-V lab videos and compiling C code using both the GCC and RISC-V compilers.simulator</summary>   
<br>

# RISC-V ISA Simulation with SPIKE

## What is SPIKE?
SPIKE is an open-source RISC-V ISA simulator written in C++. It emulates a RISC-V core and cache system, enabling developers to test RISC-V programs without hardware.

## Testing the SPIKE Simulator
To validate the setup, compile and execute a sample program using both compilers:

### Using GCC Compiler:
```sh
gcc product.c  
./a.out
```

### Using RISC-V Compiler with SPIKE:
```sh
spike pk product.o
```

## Analyzing the Assembly Code

### Objdump Analysis:
Generate the assembly code:
```sh
riscv64-unknown-elf-objdump -d sum_1ton.o | less
```

### Debugging with SPIKE:
1. Open the debugger:
   ```sh
   spike -d pk product.o
   ```
2. Use debugging commands in the terminal to analyze program execution.

## Optimization Levels
The RISC-V compiler supports different optimization levels:

1. Basic Optimization (-O1):
   ```sh
   riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o program.o program.c
   ```

2. Maximum Performance (-Ofast):
   ```sh
   riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o program.o program.c
   ```
</details>
