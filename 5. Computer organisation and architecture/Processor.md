Similar to the human brain a computer processor controls, calculates and executes instructions. A CPU has a number of different components to it, each with their own role to perform.
1. [[#Arithmetic logic unit]]
2. [[#Control unit]]
3. [[#Clock]]
4. [[#General purpose registers]]
5. [[#Dedicated registers]]

# Arithmetic Logic Unit

The Problem solving part of the processor.
- This component performs arithmetic, logical and shift operations on data.
- Arithmetic operations: Add, Subtract, Multiply and Divide.
- Logical operations include: AND, OR, NOT, XOR
- Shift operations: Move bits to the left or right within a register.

# Control Unit

The part of the processor that coordinates the activity of all other components
- Each instruction is accepted and decoded
- Separate steps such as fetching the address of data, and fetching the data itself from memory, are identified
- Each step is synchronised with a regular pulse from the system [[#Clock]]

# Clock

A regular series of ON/OFF signals are used to synchronise the operations of the processor components.
- Actions are usually carried out on the rising edge of the clock
- Actions each take a fixed number of cycles to complete
![](https://i.imgur.com/NLOtrpJ.png)

# General Purpose Registers

Results from the ALU need to be stored somewhere
- Rather than writing working data back to 'slow' memory, processors have several locations of super-fast memory called registers that are used to temporarily store results.
- The processor is then able to immediately access and re-use these results in subsequent calculations.
- Some processors have a single general purpose register called an Accumulator
![](https://i.imgur.com/vwIdxVK.png)

## Executing Instructions

Carrying out sequences of programming instructions requires many different snippets of information to be held
- The processor has to temporarily hold the current instruction being executed
- It has to hold the address of the data that it needs, and also the data itself
- It has to keep track of the address of the next instruction to be executed

# Dedicated Registers

The processor uses some dedicated registers:
- ### Program Counter (PC)
	- Holds the memory address of the next instruction to be executed
- ### Current Instruction Register (CIR)
	- Holds the current instruction
- ### Memory Address Register (MAR)
	- Holds the address in memory where the processor is required to fetch or store data from or to
- ### Memory Buffer Register (MBR)
	- Temporarily holds data moving between processor and main memory
- ### Status Register (SR)
	- Holds information about the current state of operations,. IT is used to set flags or to detect error conditions

# The Processor

![](https://i.imgur.com/V22ED5m.png)


The role of the processor is to carry out instructions from programs stored in memory, the [[Processor#Control unit|Control unit]] coordinates components to work together to achieve this in the same way that a conductor controls all the components of an orchestra.

# Fetch - Decode - Execute Cycle

Processors operate in defined stages that are used to carry out program instructions. The process is repeated over and over again for each instruction in a program

## Fetch (Steps 1 - 4)

The address of the next instruction is fetched from the pc. ![](https://i.imgur.com/V4HpPj8.png)

## Decode (Steps 5 - 7)

With instructions now in the [[Processor#Dedicated registers|CIR]], the [[Processor#Control unit|Control Unit]] can work out what needs to be done to carry it out ![](https://i.imgur.com/0mV6mqB.png)

## Execute (Steps 8 - 10)

The registers in the [[Processor]] now contain everything that the [[Processor#Arithmetic logic unit|ALU]] needs to carry out the instruction ![](https://i.imgur.com/eWOI8Vz.png)

# Factors Affecting Performance

The [[#Fetch - Decode - Execute Cycle]] is triggered from the clock pulses of the system clock
- The faster the clock speed, the faster a computer can fetch, decode and execute instructions
- [[#Cache Memory]]
- Number of cores : More processors can be linked together on a single chip allowing more instructions to be executed simultaneously
- Word length : The amount of data that the CPU can process simultaneously
- Address and data bus width

## Cache Memory

Larger and faster amounts of cache memory can improve processing speed, Fastest cache memory in the CPU is named "Level 1 Cache" with the slowest but largest "Level 3 Cache" with Level 2 being an in-between.
![](https://i.imgur.com/zibA4RF.png)

# The Role of Interrupts

- An interrupt is a signal by a software program or a hardware device sent to the CPU.
	- A software interrupt occurs when an application program terminates or requests certain services from the operating system
	- A hardware interrupt occurs, for example when an I/O operation is complete or an error occurs

- A test for interrupts is made at the end of each instruction cycle:
	- ![](https://i.imgur.com/bo1Og8L.png)
	- Execution is suspended and the contents of all registers are temporarily saved
	- An [[#interrupt service routine]] is called to deal with the interrupt

## Interrupt Service Routine

- Depending on the type of interrupt, a particular routine will be run in order to service it.
- Once the interrupt has been serviced, the original values of the registers are retrieved and the [[#Fetch - Decode - Execute Cycle]] resumes from the point that it left off.