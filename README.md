# Assembler-Emulator
The aim of this project is to create a two pass assembler for a reduced simple Assembly instruction set, and then to write and test programs in this simple assembly language. The latter part of the project works on building an Emulator for this simple machine.

# The simple assembly language
This assembly language is for a machine with four registers,
	 Two registers, A & B, arranged as an internal stack.
	 A program counter, PC
	 A stack pointer, SP
These registers are 32 bits in size. Instructions have either no operands or a single operand. The operand is a signed 2's complement value. The encoding uses the bottom 8 bits for opcode and the upper 24 bits for operand. 

![image](https://github.com/user-attachments/assets/2a7082de-ff28-48b3-afb2-787cdaf918cc)
