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

### Code to implement "Automated Parking Ticket vending Machine" :

#include <stdio.h>
#include <stdlib.h>

int current_ticket = 0;

void issue_ticket() {
    current_ticket++;
    printf("Ticket issued: %d\n", current_ticket);
   
    //This function increments the current_ticket variable by 1.It then prints the new ticket number.

}

void pay_ticket(int ticket_number) {
    if (ticket_number <= current_ticket && ticket_number > 0) {
        printf("Ticket %d has been paid.\n", ticket_number);
    } else {
        printf("Invalid ticket number.\n");
    }
 
    //  This function takes an integer ticket_number as a parameter.It checks if the ticket_number is valid (i.e., it is greater than 0 and less than or equal to the current_ticket).If valid, it prints a confirmation message.If invalid, it prints an error message.
}

void show_menu() {
    printf("1. Issue Ticket\n");
    printf("2. Pay Ticket\n");
    printf("3. Exit\n");
    
    //This function prints the menu options to the user.
}

int main() {
    int choice, ticket_number;
while (1) {
        show_menu();
        printf("Enter your choice: ");
        scanf("%d", &choice);
 switch (choice) {
  case 1:
                issue_ticket();
                break;

                   //Calls the issue_ticket function to issue a new ticket.
  case 2:
                printf("Enter ticket number to pay: ");
                scanf("%d", &ticket_number);
                pay_ticket(ticket_number);
                break;

                //Prompts the user to enter the ticket number to pay.Calls the pay_ticket function with the entered ticket number.  

   case 3:
                exit(0);

                
  default:
                printf("Invalid choice. Please try again.\n");
        }
    }

return 0;
}


The give above is the C program  for a simple automated parking ticket vending machine. 



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















