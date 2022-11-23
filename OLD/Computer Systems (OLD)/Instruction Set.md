# Instruction Set

#compsci

## Introduction

Computer [[Processor|processors]] have different ways of expressing instructions
an instruction set describes the commands a [[Processor]] can perform
different types of processors have their own [[Instruction Set|instruction sets]] but they may perform similar or identical operations

An instruction may have the following types of instruction:
- Data transfer such as LOAD, STORE
- Arithmetic operations such as ADD, SUBTRACT
- Comparison operations to compare two values
- Logical operations such as AND, OR, NOT
- Branch - conditional and unconditional
- Shift operations - shifts bits left or right in a register

## Machine Code

Machine code is a instruction set that are combinations of binary 1s and 0s, the number of bits used depends on the word length of the processor. This instruction set is the only one a processor can natively understand.

## Instruction Components

An instruction typically includes two parts:
- Operation code (opcode) which includes
	- the actual command the processor needs to carry out
	- the addressing mode - specifies whether the [[Instruction Set#Instruction set#Operands and addressing modes|operand]] is the actual data, the memory address where the data is held, or a register
- Operand(s) - one or more items of data (which can be values, memory addresses or registers) that are to be used in the instruction

### Instruction Format

The number of bits allocated to the opcode and operand will vary according to the processor used
![](https://i.imgur.com/8nN5dOz.png)

## Operands and Addressing Modes

The operand contains a reference to the data that is to be used in the instruction, this data may be either:
- An actual value that can be used as presented
- The address in memory where the data to be used is held
- The register where the data is held
The addressing mode (typically two bits) specifies which of the above describes the data

## Immediate Addressing

The operand is the actual value to be used in the instruction
![](https://i.imgur.com/GzN8EeB.png)

## Direct Addressing

The operand in this case is the address of the location in memory of the data to be used.
![](https://i.imgur.com/dqRMEhd.png)

## High and Low Level Languages

Machine code uses pure binary instructions, [[Assembly language]] uses [[Hardware and Software#Mnemonics|mnemomics]] for instructions both of these are low level languages.
[[Assembly language]] is much easier for programmers to code, but still much harder than a high level language

### Mnemonics

A mnemonic, also known as a memory aid, is a tool that helps you remember an idea or phrase with a pattern of letters, numbers, or relatable associations.

## Other

The format of instructions is determined by the processor
instruction set. This defines what the machine code instructions
mean and how the processor should execute them.
Instructions are made up of two parts: opcode, (which includes
the addressing mode) and operand.
The address mode determines how data used by the instruction
can be found. Immediate addressing means the operand is the
actual value to be used in the instruction.

Direct addressing indicates that operand is the address of the
data to be used.