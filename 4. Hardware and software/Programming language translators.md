## Assembler
All programs have to be translated into machine code before they can run. Assembly language is translated into machine code by an assembler. The assembly code program is the input to the assembler. Source code gets converted into object code which can be saved and run whenever needed.
Assembly code is used when a program needs to execute as fast as possible, occupy as little space as possible or manipulate individual bits and bytes. 

## Compiler 
Compilers translate code into a form that can be executed. However the compiler does not execute the code. Compilers produce executable code in a form that cannot be read by a human or readily reverse-engineered. 

### The compilation process
The compiler takes the source code as its set of instructions, which it then puts through a series of processes to produce executable code. A compiler also carries out:
- Lexical analysis - removes white space and comments
- Syntax analysis - syntax errors
- Semantic analysis - logic errors
- Code generation - generating the code
- Optimisation - removing unreachable code and other stuff
When the program is compiled the file will not need to be translated again. Resulting in faster running times as no further translation is required. Another advantage is that the object code not reverse engineerable meaning that it can be easily commercialised and sold. 

## Interpreter
Interpreters translate and execute each line of source code one by one. 
Each program line, when run, is first syntax-checked. If a syntax error is found then the program halts and it is reported. 
This line-by-line approach allows the developer to test the program and to quickly identify and remedy each error as it occurs, without having to go through the whole process of translating the entire program every time. Interpreters are thus very useful at the development stage of a program. Because of the constant translation during runtime, interpreted languages run slower than compiled ones. Interpreters are also more portable than compiled languages. 
But most interpreted languages now use bytecode as a intermediate stage. This bytecode is then interpreted using a virtual machine (JVM, CLR).


## Compiled vs Interpreted languages

### Compiler

#### Benefits
-   Code can be well optimised by the compiler
-   Compiled programs can be distributed as machine code, meaning that the source code is hidden and can be kept secret for commercial reasons
-   No translation is required at execution time, as it has already been done (when the source code was compiled)

#### Drawbacks
-   You have to wait until the entire program is compiled before receiving any errors, which for a large program may take some time
-   If you want to change something in the program, you have to recompile the entire program
-   The executable code produced is specific to the processor platform

### Interpreter

#### Benefits
-   Errors will be reported as soon as they are encountered, which means that you don't have to wait for the entire program to be compiled
-   Errors are shown line by line as the interpreter reaches them
-   Debugging is quicker and easier as errors are reported in the console, which shows what and where the error is in the code

#### Drawbacks
-   The program requires an interpreter to be run
-   Translating the code line by line at execution time is slower than running compiled machine code
-   The interpreter takes up space in memory