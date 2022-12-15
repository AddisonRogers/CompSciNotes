# What is a Computer System

A computer system is any device that can take a set of inputs and process them into useful outputs
![](https://i.imgur.com/Z8C3XBI.png)

A computer system incorporates all of the hardware and software required to operate it. The hardware includes the [[Processor]], input output and storage devices.

# Parts of the CPU

The CPU contains:
- [[Processor]]
- [[#Main Memory]]
- [[#Address, Control and data buses]]
- [[#Input/output (I/O) controllers]]

![](https://i.imgur.com/CFfOStW.png)

# I/O Controllers

External devices are produced by different manufacturers and cannot be directly connected to the [[Processor]], The I/O controller for each peripheral device acts as an interface between the device and the computer.

## Device Drivers

The software that interacts directly with the I/O controller is called a device driver.

## I/O Controller Tasks

- The controller converts signals received from a peripheral device into a format the computer can process, and vice versa.
- It receives I/O requests from the CPU, and then sends device-specific control signals to the device it is controlling.
- It also manages the data flow to and from the device, freeing the CPU to get on with other tasks.

# Address, Control and Data Buses

## Introduction

### What is a Bus?

Buses in a computer consist of a series of wires that transfer data signals between internal components. They typically consist of 8, 16, 32 or 64 lines

### Sending Information via Buses

- The [[#Control buses|control bus]] is used to send control signals between each I/O controller and the [[Processor]], as well as between the [[Processor]] and memory
- The [[#Data buses|data bus]] sends data between CPU components
- The [[#Address buses|address bus]] sends memory addresses from the [[Processor]] to CPU components

### Words

Memory is divided up in equal units called words, word length is usually 8, 16, 32 or 64 bits with each word having a separate memory address

## Control Buses

Control signals are signals sent between I/O controllers and the [[Processor]] as well as the [[Processor]] and memory. These signals include:
- Memory read: causes data from the addressed location to be placed on the data bus
- Memory write: causes data on the data bus to be written into the addressed location
- Bus request: indicates that a device is requesting use of the data bus
- Bus grant: indicates that the CPU has granted access to the data bus
- Clock: used to synchronise operations.

## Data Buses

Data buses carry data from the main memory to the [[Processor]] and vice versa.
- The data bus is bi-directional as data can be send both ways along the bus
- The width of the data bus is defined by the number of wires or lines it contains
- If the data bus is the same width as a computer word, data can be transferred to and from memory in a single operation.
- Bus width affects overall system performance.

## Address Buses

The purpose of an address bus is to identify the address of the location in cache or main memory that is to be read from or written to. Each location in memory will have its own unique address, that is known as addressability.
- It is uni-directional and is from the [[Processor]] to the component
- The width of the address bus determines the maximum possible memory addresses of the system
- A 32-bit bus can carry 2^32 addresses

# Main Memory

- Main memory stores data and instructions that are to be processed
- The number of memory address is constrained by the width of the [[#Address buses|address bus]]
- Each address can store a fixed number of bits determined by the type of [[Processor]]
- The smallest addressable unit is called a [[#Words|word]]
- ![](https://i.imgur.com/q4t50Qe.png)

# Multipurpose Machines

Early computers were able to calculate an output using fixed instructions. They could perform only one set of instructions. However a general purpose computer an perform many different tasks at different times, their programming is not fixed, to achieve this computers are designed to allow data and instructions to be stored - this is called [[#Stored program concept]]

## Stored Program Concept

Machine cod instructions are loaded into main memory to be executed by the processor, these instructions are then fetched one at a time and executed immediately by the processor in a sequential order ([[Processor#Fetch - Decode - Execute Cycle]])

## John Von Neumann

The most common implementation of this concept is the von Neumann architecture with instructions and data stored on common main memory and transferred to the Processor using a single shared bus.
![](https://i.imgur.com/VCnh5SM.png)

## Harvard Architecture

An alternative model separates the data and instructions into separate memories using different buses, now the program instructions and its data are no longer competing for the same bus.
![](https://i.imgur.com/vzh3oRU.png)

