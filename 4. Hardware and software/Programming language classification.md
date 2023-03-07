## Old computers

### Colossus
Colossus Mark 1 was developed by Tommy Flowers built at Bletchley Park in 1943 for the Military to crack the Enigma Code used by Germans in WW2. Input was a continuous loop of paper tape with 20,000 5-bit characters programmed using switches and plug panels. Output was just a indicator lamp panel. 

### 1940s
By the late 1940s there were still only a handful of computers around, used by large companies for commercial applications such as payroll. 
These computers had limited memory with each memory cell consisting of a vacuum tube the size of a light bulb. They had a control unit and an accumulator where instructions were carried out. These were programmed using machine code, entered using a series of switches. 

## Modern computers
Modern computers started using Machine Code. A typical instruction holds an operation code in the first few bits and an operand in the rest of the bits. 

![[Instruction Set#Machine Code]]

[[Instruction Set]] of a computer is all the instructions that it can understand and execute. The operand can be either an actual value or the address in memory where the value is held.

### Assembly
[[Assembly language]] was the next stage in the development of programming languages. This featured [[OLD/Computer Systems (OLD)/Hardware and Software#Mnemonics|Mnemonics]] which gave a clue as to what the operation did. The Assembly language made making programs much easier as it was easier to write understand and debug but at the disadvantage of the code being translated into machine code by an assembler.

### High-level languages
In the 1960s FORTRAN was made. The first high-level language that looked similar to maths or English than machine code. This is an example of abstraction

#### Imperative high-level languages
An imperative high-level language consists of commands for the computer to perform. This contrasts a declarative language which focuses on what the program should do without listing the steps needed to achieve the result. 

### Translation
A high-level program has to be converted into machine code before it can be executed. Assembly language has a one-to-one relationship with machine code. Unlike assembly languages high-level languages like Fortran or C are **portable**. This means that programs written for one type of computer can be recompiled for a different type of computer. 

### Evaluation
The object code (compiled or interpreted code) may run slower and more hardware expensive than assembly or machine code, but it is also much easier to write and debug because of its legibility and portability. 