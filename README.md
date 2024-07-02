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

# Assigment 2

## Ticket Terminal Designer : Developing an Automated Parking Ticket Vending Machine

### Code:

    #include <stdio.h>
    #include <stdlib.h>

    int current_ticket = 0;

     void issue_ticket() 
     {
          current_ticket++;
          printf("Ticket issued: %d\n", current_ticket);
     }

     void pay_ticket(int ticket_number)
     {
          if (ticket_number <= current_ticket && ticket_number > 0)
          {
          printf("Ticket %d has been paid.\n", ticket_number);
          } 
          else 
          {
        printf("Invalid ticket number.\n");
         }
    }

    void show_menu()
    {
       printf("1. Issue Ticket\n");
       printf("2. Pay Ticket\n");
       printf("3. Exit\n");
    }

    int main()
    {
    int choice, ticket_number;

    while (1) {
        show_menu();
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                issue_ticket();
                break;
            case 2:
                printf("Enter ticket number to pay: ");
                scanf("%d", &ticket_number);
                pay_ticket(ticket_number);
                break;
            case 3:
                exit(0);
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

       return 0;
    }

The give above is the C program  for a simple automated parking ticket vending machine. 

### Code explanation :

1.void issue_ticket() {
    current_ticket++;
    printf("Ticket issued: %d\n", current_ticket);
    }
   
    //This function increments the current_ticket variable by 1.It then prints the new ticket number.
    
2.void pay_ticket(int ticket_number) {
    if (ticket_number <= current_ticket && ticket_number > 0) {
        printf("Ticket %d has been paid.\n", ticket_number);
    } else {
        printf("Invalid ticket number.\n");
    }
 
    //  This function takes an integer ticket_number as a parameter.It checks if the ticket_number is valid (i.e., it is greater than 0 and less than or equal to the current_ticket).If valid, it prints a confirmation message.If invalid, it prints an error message.

3.void show_menu() {
    printf("1. Issue Ticket\n");
    printf("2. Pay Ticket\n");
    printf("3. Exit\n");
    
    //This function prints the menu options to the user
    
4.case 1:
   issue_ticket();
   break;

    //Calls the issue_ticket function to issue a new ticket.
    
  5.case 2:
     printf("Enter ticket number to pay: ");
     scanf("%d", &ticket_number);
     pay_ticket(ticket_number);
     break;
             
    //Prompts the user to enter the ticket number to pay.Calls the pay_ticket function with the entered ticket number. 
    
  6. case 3:
       exit(0);

          //Exits the program

7.default:
     printf("Invalid choice. Please try again.\n");

     //Prints an error message if the user enters an invalid choice.
    
### Functions :

1.It includes functions to issue and pay for tickets, and a menu for user interaction.
2.The program maintains a simple ticketing system.
3.Users can issue tickets, pay for tickets, or exit the program.
4.The current_ticket variable tracks the number of issued tickets.
5.The program runs in an infinite loop until the user decides to exit.

## Compilation of the C code 

### Step 1:

The C code  for automated parking ticket machine is compiled in the leafpad terminal.It verifies the ticket validation , payment processing by various dynamic data algorithms.

![WhatsApp Image 2024-06-25 at 16 18 08_30df8bb7](https://github.com/RindhiyaM/VSDS-/assets/173605041/e28afed1-d3bb-487a-b4b7-c427b7489a5d)

![WhatsApp Image 2024-06-25 at 16 18 08_b6320f25](https://github.com/RindhiyaM/VSDS-/assets/173605041/7e08e62a-406d-455f-b11a-d589f8f89d0b)

### Step 2:

The output of the given code is determined after compilation in the terminal.

![WhatsApp Image 2024-06-25 at 16 37 39_1b920b08](https://github.com/RindhiyaM/VSDS-/assets/173605041/063dbd54-9a8f-4a6d-9fbd-02e47ef740c8)

running this program, we will see a menu with three options. You can issue tickets, pay for tickets, or exit the program. The program will keep running until you choose the exit option.

### Step 3:

In this step the C program is converted to the RISC V instruction and this is detrmined using the command "riscv64-unknown-elf-gcc -o1 -mabi=lp64 -march=rv64i -o ticketterminal.o ticketterminal.c" . The main function are to be determined using the given command "riscv64-unknown-elf-objdump -d ticketterminal.o |less"

![WhatsApp Image 2024-06-25 at 16 37 39_036c12a0](https://github.com/RindhiyaM/VSDS-/assets/173605041/185cc72f-fae6-45c2-ae86-df6c1be2871e)

This above command focus the main function

![less fnc](https://github.com/RindhiyaM/VSDS-/assets/173605041/f9c84228-40d7-4498-8190-0bc43a83514f)

The main function 

![main fnc](https://github.com/RindhiyaM/VSDS-/assets/173605041/1b5c9054-4225-454a-9782-03237a93de6b)

### Step 4:

After determining the main function the calculations are performed under the same command of "riscv64-unknown-elf-objdump -d ticketterminal.o |les" . First instruction gets calculated

![using o1](https://github.com/RindhiyaM/VSDS-/assets/173605041/a30fa912-6a79-4ede-aaaa-1901a43de459)

### Step 5:

The same function is get excuted inorder to determine the difference in the function using a particular function called "OFast" which is determined by the command "riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o ticketterminal.o ticketterminal.c"

![fnc o1 to o1fact](https://github.com/RindhiyaM/VSDS-/assets/173605041/5b3b58aa-df9f-4f57-8113-a2714f3eff2c)

Hence the calculation after the "OFast" function

![last image](https://github.com/RindhiyaM/VSDS-/assets/173605041/dd0b1f19-1d61-4c7c-931d-b218ef7ffede)

After determining the difference from executing the same function , the code can be optimized further.Hence the Automated parking ticket vending machine is also determined in RISC V instructions using certain calculations 

# Assignment 3
## SPIKE simulation and verification :
Perform SPIKE simulation and verification with -O1 and -OFast optimizations, and run the RISC-V objdump.
### Compile the program :

1.Compile the program with different optimization levels:

![j271](https://github.com/RindhiyaM/VSDS-/assets/173605041/22921d5c-0cfa-41c6-a3f1-b2ae999c8a55)

2.DeBUG command : riscv64-unknown-elf-objdump -d ticketterminal.o |less

![j273](https://github.com/RindhiyaM/VSDS-/assets/173605041/e3b8ffdf-3a2b-4f50-96e3-1e3b5a4d0173)

3.spike simulation : spike pk ticketterminal.o

![j272](https://github.com/RindhiyaM/VSDS-/assets/173605041/f19c0acd-2076-4064-ba12-f42f8a7256f2)

4.Disassemble the binaries with objdump:

![j274](https://github.com/RindhiyaM/VSDS-/assets/173605041/e3e0608b-5f5a-4333-83c7-4d8e6f4dca7a)

# Assignment 4

Let's break down each instruction into its respective RISC-V instruction format and then encode them into their 32-bit binary representations.

## Instruction Formats

### R-type: 
Used for register-register operations
#### Format: 
opcode | rd | funct3 | rs1 | rs2 | funct7
#### Instructions: 
ADD, SUB, AND, OR, XOR, SLT, SRL, SLL

### I-type: 
Used for immediate operations and loads
#### Format:
opcode | rd | funct3 | rs1 | imm
#### Instructions:
ADDI, LW

### S-type: 
Used for stores
#### Format: 
opcode | imm[11:5] | rs2 | rs1 | funct3 | imm[4:0]
#### Instructions:
SW

### B-type: 
Used for branches
#### Format:
opcode | imm[12] | imm[10:5] | rs2 | rs1 | funct3 | imm[4:1] | imm[11]
#### Instructions: 
BNE, BEQ

## Binary Encoding

### R-type Instructions

#### ADD r1, r2, r3

opcode: 0110011
funct3: 000
funct7: 0000000
rd: 00001 (r1)
rs1: 00010 (r2)
rs2: 00011 (r3)
Binary: 0000000 00011 00010 000 00001 0110011
Hex: 0x002080b3

#### SUB r3, r1, r2

opcode: 0110011
funct3: 000
funct7: 0100000
rd: 00011 (r3)
rs1: 00001 (r1)
rs2: 00010 (r2)
Binary: 0100000 00010 00001 000 00011 0110011
Hex: 0x402100b3

#### AND r2, r1, r3

opcode: 0110011
funct3: 111
funct7: 0000000
rd: 00010 (r2)
rs1: 00001 (r1)
rs2: 00011 (r3)
Binary: 0000000 00011 00001 111 00010 0110011
Hex: 0x003100b3

#### OR r8, r2, r5

opcode: 0110011
funct3: 110
funct7: 0000000
rd: 01000 (r8)
rs1: 00010 (r2)
rs2: 00101 (r5)
Binary: 0000000 00101 00010 110 01000 0110011
Hex: 0x005140b3

#### XOR r8, r1, r4

opcode: 0110011
funct3: 100
funct7: 0000000
rd: 01000 (r8)
rs1: 00001 (r1)
rs2: 00100 (r4)
Binary: 0000000 00100 00001 100 01000 0110011
Hex: 0x004080b3

#### SLT r10, r2, r4 

opcode: 0110011
funct3: 010
funct7: 0000000
rd: 01010 (r10)
rs1: 00010 (r2)
rs2: 00100 (r4)
Binary: 0000000 00100 00010 010 01010 0110011
Hex: 0x004140b3

#### SRL r16, r11, r2

opcode: 0110011
funct3: 101
funct7: 0000000
rd: 10000 (r16)
rs1: 01011 (r11)
rs2: 00010 (r2)
Binary: 0000000 00010 01011 101 10000 0110011
Hex: 0x002580b3

#### SLL r15, r11, r2

opcode: 0110011
funct3: 001
funct7: 0000000
rd: 01111 (r15)
rs1: 01011 (r11)
rs2: 00010 (r2)
Binary: 0000000 00010 01011 001 01111 0110011
Hex: 0x0025c0b3

### I-type Instructions

#### ADDI r12, r3, 5

opcode: 0010011
funct3: 000
rd: 01100 (r12)
rs1: 00011 (r3)
imm: 000000000101
Binary: 000000000101 00011 000 01100 0010011
Hex: 0x00518193

#### LW r13, r11, 2

opcode: 0000011
funct3: 010
rd: 01101 (r13)
rs1: 01011 (r11)
imm: 000000000010
Binary: 000000000010 01011 010 01101 0000011
Hex: 0x00258603

### S-type Instructions

#### SW r3, r1, 4

opcode: 0100011
funct3: 010
rs1: 00001 (r1)
rs2: 00011 (r3)
imm: 000000000100
Binary: 0000000 00011 00001 010 00010 0100011
Hex: 0x00310223

### B-type Instructions

#### BNE r0, r1, 20

opcode: 1100011
funct3: 001
rs1: 00000 (r0)
rs2: 00001 (r1)
imm: 00000000010100 (splits into multiple parts)
Binary: 0000000 00001 00000 001 00101 1100011
Hex: 0x00102863

#### BEQ r0, r0, 15

opcode: 1100011
funct3: 000
rs1: 00000 (r0)
rs2: 00000 (r0)
imm: 00000000001111 (splits into multiple parts)
Binary: 0000000 00000 00000 000 01111 1100011
Hex: 0x00002663

### Here's a sample content for the file:

ADD r1, r2, r3: 0x002080b3
SUB r3, r1, r2: 0x402100b3
AND r2, r1, r3: 0x003100b3
OR r8, r2, r5: 0x005140b3
XOR r8, r1, r4: 0x004080b3
SLT r10, r2, r4: 0x004140b3
SRL r16, r11, r2: 0x002580b3
SLL r15, r11, r2: 0x0025c0b3
ADDI r12, r3, 5: 0x00518193
SW r3, r1, 4: 0x00310223
BNE r0, r1, 20: 0x00102863
BEQ r0, r0, 15: 0x00002663
LW r13, r11, 2: 0x00258603

















