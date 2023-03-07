#Remake

## Half-adder

A Half-adder is a circuit that performs the addition of two bits.

![[Pasted image 20220509084807.png]]`center`

S represents the Sum of A+B, C represents the carry bit.

Half adders can only have two inputs and cannot use the carry bit from a previous addition therefore it can only add one-bit numbers.

## Full Adder

A Full-adder is a combination of two [[#Half-adder|half adders]] With three inputs: A, B and the carry input.

![[Pasted image 20220509085315.png]]`center`

Here the circuit outputs S and the new carry bit.

Multiple full adders can be connected together. N full adders can be connected together to input the carry bit into a subsequent adder along with two new inputs.

## D-Type Flip Flops

A flip is an elemental sequential logic circuit that can store one bit and flip between two states, 0 and 1.

![[Pasted image 20220509142923.png]]`center`

The output will only be positive if the clock signal is on a “rising edge”. Pain.

### The Clock

The clock is another type of sequential circuit that changes state at regular time intervals. A clock is needed to synchronise the change of flip flop circuits.

![[Pasted image 20220509143709.png]]`CENTER`

So Q is only updated when the clock pulses (Rising edge).

### What Are D-type Flip Flops Used For?

D-type flip flops are commonly used to create:

- Registers and counters,
- Static Ram,
- Immediate storage needed during arithmetic operations.

 Static ram is much faster and more expensive than regular dynamic Ram which must be periodically refreshed. Static Ram is typically used for cache memory, while DRAM is used for main memory.
