#Remake

Computers can only process instructions that are written in [[Instruction Set#Machine code|Machine Code]], Assembly language uses [[OLD/Computer Systems (OLD)/Hardware and Software#Mnemonics|mnemomics]] to represent operation codes and addresses.

## Registers and Accumulator

In a simple computer all calculations may be carried out in the [[Processor#General purpose registers|Accumulator]], other computers may hold up to 16 general purpose registers that perform the same purpose.

## Language

| Syntax                | Meaning                                                                                                   |
| --------------------- | --------------------------------------------------------------------------------------------------------- |
| LDR Rd (memory ref)   | Load the value stored in (memory ref) into register D                                                     |
| STR Rd (memory ref)   | Store the value in register D into the memory location specified by (memory ref)                          |
| ADD Rd, Rn (operand)  | Add the value specified in (operand) to the value in register n and store it in register D                |
| SUB Rd, Rn, (operand) | Subtract the value specified by (operand) from the value in register n and store the result in register d |
| MOV Rd, (operand)     | Copy the value specified by (operand) into register d                                                     |

An operand could be

	- An actual value, specified by # ([[Instruction Set#Immediate addressing|Immediate addressing]])

	- A value stored in another register specified by R ([[Instruction Set#Direct addressing|direct addressing]])

The memory ref will be the address number that can be found in memory.

### Branch Instructions

There are no IF statements in assembly language, instead there is 'compare' and 'branch' instructions.

| Syntax                  | Meaning                                                                                            |
| ----------------------- | -------------------------------------------------------------------------------------------------- |
| CMP Rn, (operand)       | Compare the value stored in register N with the value specified in (operand)                       |
| B (label)               | Always brand to the instruction at position (label) in the program                                 |
| B(condition)  (label) | Conditionally branch to (label) if the last comparison met the conditions specified by (condition) |

Some conditions:

	BEQ : Equal to 0

	BNE : Not equal to

	BGT : Greater than

	BLT : Less than

### While Loops

The equivalent of a while loop can be written using compare and branch instructions.

```mermaid
graph TD
Start --> Set-total-to-0
Set-total-to-0 --> Input-number
Input-number --> Number=0?
Number=0? --No--> Set-total-to-0
Number=0? --Yes--> Store(Store Total in location 100)
Store --> End

```

### Logical Operators

| Syntax                 | Meaning                                                                                                |
| ---------------------- | ------------------------------------------------------------------------------------------------------ |
| AND Rd, Rn, (operand2) | Perform a logical AND operation between register N and the operand then store the result in register D |
| ORR Rd, Rn, (operand2) | Perform a logical OR operation between register N and the operand then store the result in register D  |
| EOR Rd, Rn, (operand2) | Perform a logical XOR operation between register N and the operand then store the result in register D |
| MVN Rd, (operand2)     | Perform a logical NOT operation and store the result in register D|

### Logical Shift Operations

| Syntax                | Meaning                                                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| LSL Rd, Rn, (operand) | Logically shift the value stored in register N by the number of bits specified by the operand left and then store the result in register D  |
| LSR Rd, Rn, (operand) | Logically shift the value stored in register N by the number of bits specified by the operand right and then store the result in register D |
