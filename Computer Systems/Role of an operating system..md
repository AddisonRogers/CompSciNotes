
An OS forms a bridge between the physical hardware of a computer and the user or application software.

# Hiding the Complexities of Operation

- The true complexities of operations are hidden from the user via an Application Programming Interface (API)
- Users can issue commands to perform complex operations without having to know what they carried out

# Functions of an OS

- [[Role of an operating system.#Memory management |Memory Management]]
- [[Role of an operating system.#Processor scheduling|Processor scheduling]]
- [[Role of an operating system.#Backing store management |Backing store management]]
- [[Role of an operating system.#IO device management |Peripheral management of IO devices]]

# Memory Management

-  A PC allows many processes to be running at the same time.
- The OS allocates memory to each process
- If there is not enough memory, a program may be swapped out of memory onto disk or "virtual memory" and reloaded when activated

# Processor Scheduling

The OS controls which programs can send data to the [[Processor]] to be processed.

## The Scheduler

The scheduler is the operating system module responsible for ensuring that [[Processor]] time is used as efficiently as possible. There are different scheduling algorithms:
- Round Robin: each process in turn has use of the [[Processor]] for a given time slice.
- Shortest job next
- Priority system.

# Backing Store Management

The OS keeps track of where all files are stored on the hard disk or external drives, and where space is free to be used if the user performs a save operation.

# IO Device Management

- Communicates with I/O devices via the I/O controller, part of the CPU
- Checks that a required output device is switched on and ready to receive data
- Deals with [[Processor]] 'interrupts'