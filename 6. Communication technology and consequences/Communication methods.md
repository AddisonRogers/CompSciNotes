# Communication Methods

## Serial and Parallel Data Transmission

Serial data cables include the USB.
Parallel cables are a ribbon of several smaller cables used primarily for connecting internal components

### Serial Data Transmission

Bits are sent one after another along the same data line. This means that only one line is needed to transmit data in one direction.

### Parallel Data Transmission

Several bits are sent simultaneously along separate lines or channels. This means that an 8-bit block of data will require 8 data channels, plus some extra for control information.


## A short History

In the early days of computing, vast amounts of data were sent via [[Communication methods#Serial data transmission|serial connections]]. These were reliable but slow.

Makers began using [[Communication methods#Parallel data transmission|parallel connections]] 


## Problems with Parallel Data Transmission

As speeds of transmission got higher and higher, parallel connections developed problems. As each individual wire has slightly different properties, bits travel at slightly different speeds along each of the wires. Producing a problem known as skew.

### The Problem of Crosstalk

Referring to electromagnetic interference between two adjacent channels or parallel wires. It gets more obvious as the frequency increases.

## Serial Vs Parallel Transmission

Parallel transmission can be used only over very short distances of up to about 2m. While serial transmission is reliable over very long distances at very high frequencies.

Serial connectors such as USB are much smaller and cheaper than parallel connectors.

## Synchronous Transmission

All data transfers are timed to coincide with an internal clock pulse. The data is sent as one long stream or block of data, with no gaps in the transmission. The receiver counts the bits and reconstructs bytes.

## Asynchronous Transmission

Using async data transmission, each byte is sent separately the moment it is available instead of waiting for a clock signal. Each byte is preceded by a start bit and ends with a stop bit or stop 'period' - a short time gap between each set of bits.

Async transmission is relatively slow owing to the increased number of bits being sent. It is a cheap and effective form of serial transmission well suited to low-speed connections such as keyboard and mouse.


## The Parity Bit

The parity bit or check bit is added as the 8th bit as a form of error detection.

## Latency

Latency is the time delay between the moment the first byte or packet of a communication starts and when it is received at its destination.

## Protocol

All communications between devices require that the devices agree on the format of the data. The set of rules relating to communication between devices is called a protocol.
The protocol needs to define for example:
- Standards for physical connections and cabling
- The rate of transmission
- Data format
- Whether transmission is synchronous or async
- Error checking procedures

## Speed of transmission

Bit rate is the number of bits transmitted in one second over a wired or wireless data link. Using baseband at each signal change one bit is transmitted. The faster the signal change, the greater the number of bits per second.

## Bit rate and baud rate

Bit rate is the number of bits transmitted in one second over a wired or wireless data link. 
Baud rate is the rate at which the signal in a communications channel changes state.
It is usually measured in megabits per second.
Baseband carries one signal at a time. A bit is represented by a high or low voltage in the cable. Broadband carries multiple signals on a fixed carrier wave. Bits are sent as variations on the wave.

Baud rate is the rate at which the signal changes
Bit rate is bits per second
Bit rate = Baud rate x number of bits per signal

Bandwidth is a measure of the maximum capacity of a communications channel. In computer networks the term bandwidth is used as a synonym for data transfer rate usually expressed in bps, Mbps or Gbps.