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

# Assignment 5
## RISC-V core in Verilog along with a testbench for functional simulation, you need to go through the following steps:

"git clone http://github.com/vinayrayapati/rv32i.git my_ticket_rv32i" , " cd my_ticket_rv32i " are the commands used 

Cloning is the process of creating a local copy of a remote repository. This allows you to have a complete copy of the repo

![3rd image](https://github.com/RindhiyaM/VSDS-/assets/173605041/9af4fc9f-133a-4d33-8e27-edae12cb4afa)

This will download the project into a local directory

![1st image](https://github.com/RindhiyaM/VSDS-/assets/173605041/48a26cd8-ed53-4fb2-adcb-9d48ea88a5c5)

"sudo apt update" , "sudo apt install inverilog gtkwave" are the commands used

![2nd image](https://github.com/RindhiyaM/VSDS-/assets/173605041/3f12fb36-1123-406c-98ca-f83059dcffd3)

![4th image](https://github.com/RindhiyaM/VSDS-/assets/173605041/835e58c5-e1a7-4736-938b-32cf18913296)

# Output:

## ADD

![op 1](https://github.com/RindhiyaM/VSDS-/assets/173605041/c7bc3423-53ac-491d-bd63-28dc75f857e7)

## SUB

![op 2](https://github.com/RindhiyaM/VSDS-/assets/173605041/b8488fca-6d4b-4cb4-afec-789553333380)

## AND

![op 3](https://github.com/RindhiyaM/VSDS-/assets/173605041/0986c78a-5835-49fa-bbf8-78b1a7ab2d16)

## SLT

![op 4](https://github.com/RindhiyaM/VSDS-/assets/173605041/e49d5780-4e8c-49b3-bc08-5148a4f8a15f)

## OR

![op 7](https://github.com/RindhiyaM/VSDS-/assets/173605041/cca4380c-b36f-4864-b3ee-231d10447246)

## XOR

![op 8](https://github.com/RindhiyaM/VSDS-/assets/173605041/418121a9-7868-4978-8cc0-dbb29f7f9fe8)

## BEQ

![op 10](https://github.com/RindhiyaM/VSDS-/assets/173605041/472aab09-64b1-4622-bcf3-ff32ef9346e1)

## BNE

![op 9](https://github.com/RindhiyaM/VSDS-/assets/173605041/60c3b5e8-efd3-48a7-85fd-6e22fc9bd902)

# Assignment 6

## Overview

The Automated Parking Ticket Vending Machine is designed to facilitate easy and efficient ticket dispensing in parking lots. Using the VSDSquadron Mini, a versatile microcontroller board, the system will automate the process of ticket issuing, payment processing, and entry/exit management.

## Components

### 1.VSDSquadron Mini Microcontroller Board

* Central control unit
* Interfaces with all other components

### 2.LCD Display

* Displays instructions and information to users
* Shows the status of the transaction

### 3.Keypad

* Allows users to input information such as license plate numbers, parking duration, etc.

### 4.Ticket Printer

* Prints parking tickets with relevant information
* Could be a thermal printer for durability and ease of use

### 5.Card Reader/Payment Terminal

* Facilitates payment via credit/debit cards or NFC payments
* Integrates with a payment gateway

### 6.Sensors

* Entry/Exit Sensors: Detects vehicle entry and exit
* Presence Sensor: Ensures the vehicle is properly positioned before issuing a ticket

### 7.Barrier Gate

* Controls vehicle entry and exit
* Interfaces with the microcontroller for automated control

### 8.Network Module

* Facilitates communication with a central server for data logging, remote monitoring, and maintenance

### 9.Power Supply

* Provides necessary power to all components
* Includes backup battery for uninterrupted operation

## Pin Diagram

Below is a conceptual pin diagram for the Automated Parking Ticket Vending Machine using the VSDSquadron Mini:

### VSDSquadron Mini Microcontroller

#### Power (VCC, GND)

#### LCD Display
   * Data Pins: D4-D7 (Digital Pins 4-7)
  
   * Control Pins: RS (Digital Pin 2), E (Digital Pin 3)
   
   * Power Pins: VCC, GND

#### Keypad
  
   * Row Pins: R1-R4 (Digital Pins 8-11)
  
   * Column Pins: C1-C3 (Digital Pins 12-14)
  
   * Ticket Printer
  
   * Data Pin: Tx (Digital Pin 15)
   
   * Control Pin: Print (Digital Pin 16)
  
   * Power Pins: VCC, GND
     
#### Card Reader/Payment Terminal

   * Data Pins: Rx, Tx (Digital Pins 17, 18)
     
   * Power Pins: VCC, GND
     
#### Sensors

   * Entry/Exit Sensor: Digital Pins 19, 20
     
   * Presence Sensor: Digital Pin 21
     
   * Power Pins: VCC, GND
     
#### Barrier Gate Control

   * Control Pin: Digital Pin 22
     
   * Power Pins: VCC, GND
     
#### Network Module

   * Data Pins: SPI or I2C Pins (depends on module type)
     
   * Power Pins: VCC, GND
     
#### Power Supply

   * VCC, GND Pins

## Operation to be performed

  * Vehicle Detection: Entry sensor detects the vehicle.
    
  * User Interaction: User inputs information via the keypad and views instructions on the LCD display.
    
  * Ticket Issuing: Microcontroller processes the input and prints a ticket using the ticket printer.

  * Payment: User makes payment via the card reader/payment terminal.
    
  * Gate Operation: Upon successful payment, the barrier gate opens to allow vehicle entry.
    
  * Data Logging: All transaction data is logged and communicated to a central server via the network module for monitoring and management.
    
  * This design ensures a streamlined and user-friendly experience for automated parking ticket vending, utilizing the capabilities of the VSDSquadron Mini microcontroller.

# Illustration of the  desired Project :

https://drive.google.com/file/d/12BmLKFu9hcAQtrLfAxfRT7QlEjkdFsHg/view?usp=drive_link

X_____X_____X_____X_____X_____X
























