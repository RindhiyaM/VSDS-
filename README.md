# VSDSquadron mini

The VSDSquadron Mini RISC-V is a development board based on the RISC-V architecture, which is an open-source instruction set architecture (ISA) known for its flexibility and extensibility. Here’s an overview of its features and significance:

## Key Features:

### RISC-V Core:

The board is powered by a RISC-V core, which is a modern and open-source processor architecture designed to be scalable and versatile.
Development and Learning:

It serves as an excellent platform for learning about RISC-V architecture, digital design, and embedded systems. It is widely used in educational settings to teach computer architecture and programming.
Hardware Specifications:

### Processor: 

A RISC-V core, possibly a simple core like RV32I (32-bit) or more advanced configurations depending on the specific model.

### Memory: 

Includes a certain amount of RAM and possibly flash storage for program and data storage.

### I/O Interfaces:

Likely to have GPIO pins, UART, SPI, I2C, and possibly other interfaces for connecting peripherals.

### Software Support:

Compatible with various development tools and environments that support RISC-V, including GCC, LLVM, and specialized RISC-V IDEs.
May come with pre-installed bootloader and basic software examples to help users get started quickly.

# Assignment 1 
## Write a C program to determine the sum of nubers from 1 to n

### Step 1:
The virtual box is installed and open the file in ubuntu with the help of virtual box inorder to compile the C code

![Virtual box ](https://github.com/RindhiyaM/VSDS-/assets/173605041/3d0c6ed5-3186-4a96-83f3-147a513304dd)

### Step 2:
With the help of the virtual box the Ubuntu is successfully installed

![Installation of Ubuntu](https://github.com/RindhiyaM/VSDS-/assets/173605041/a850dfa3-806f-4267-8036-11100041dff4)

### Step 3:
Inorder to write a C program the terminal window needs to opened

![TERMINAL](https://github.com/RindhiyaM/VSDS-/assets/173605041/56712e1d-1d3a-4f27-bec0-7ce4e0e0d566)

### Step 4:
leafpad is kind of text editor used to write c program and compile is installed with the command of "sudo snap install leafpad" . The command "leadfpad sum1ton.c" is used to open a file where the C code can be written.

![C Program - sum of numbers from 1 to N](https://github.com/RindhiyaM/VSDS-/assets/173605041/3ade1fb6-7f75-4cbd-be81-65fd23724707)

The C code is compiled in the leafpad by using the command "gcc sum1ton.c". To determine the output of the compiled code the command "./a.out" is used.

![Fast Instruction](https://github.com/RindhiyaM/VSDS-/assets/173605041/8acac3ed-40f2-44fb-8376-5cc557e41d87)

### Step 5:
The C code can be converted to RISCV instruction with the help of the command "riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c"

![Main Function](https://github.com/RindhiyaM/VSDS-/assets/173605041/4577f064-e252-4418-962d-df55866535f0)

### Step 6:

Now the calculation of RISC V processor is determined using the Calculator in the terminal

![Calculation of riscv ](https://github.com/RindhiyaM/VSDS-/assets/173605041/de4789f3-c62d-44e8-905d-909e11567f7c)













