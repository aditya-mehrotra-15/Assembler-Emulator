# Assembler-Emulator
The aim of this project is to create a two pass assembler for a reduced simple Assembly instruction set, and then to write and test programs in this simple assembly language. The latter part of the project works on building an Emulator for this simple machine.

***

# The simple assembly language and its instruction set
## Assembly Language
This assembly language is for a machine with four registers,

* Two registers, A & B, arranged as an internal stack.
* A program counter, PC
* A stack pointer, SP
  
These registers are 32 bits in size. Instructions have either no operands or a single operand. The operand is a signed 2's complement value. The encoding uses the bottom 8 bits for opcode and the upper 24 bits for operand.

As with most assembly languages, this is line based (one statement per line). Comments begin with a ';' and anything on the line after the ';' is ignored. Blank lines and lines containing only a comment are permitted (and ignored).

Label definitions consist of the label name followed by a ':', and an optional statement. A valid label name is an alphanumeric string beginning with a letter . An operand is either a label or a number, which can be decimal, hex or octal.

## The Simple Instruction-Set
![image](https://github.com/user-attachments/assets/8c68b20c-ef67-4f77-a151-9d5351e48e3e)

***
# Files Generated and Compilation+Run Instructions
The Assembler generates 3 files:

* .log file for error, warning info.
* .lst listing file.
* .o object file for machine code object.

**The .lst and .o files only generate if no errors are found in the .log file.** The .o object file generated will be used as an input to the Emulator.

## Compilation instructions

To Compile Assembler code and create executable file:
```
g++ Assembler.cpp
```
To Compile Emulator code and create executable file:
```
g++ Emulator.cpp
```
To run a created executable file:

(Windows)
```
./a.exe
```
(Linux)
```
./a.out
```

