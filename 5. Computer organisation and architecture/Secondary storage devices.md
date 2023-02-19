#Remake 
Primary storage devices are volatile and usually refer to RAM. However Secondary storage refers to non-volatile storages such as:
- Magnetic storage (Hard Disk)
- Optical storage (CD-ROM)
- Solid state devices (Flash memory)

- Different technologies have evolved for saving data, each of these have their own advantages and disadvantages in terms of:
	- Durability
	- Read / Write speed
	- Capacity
	- Portability
	- Cost

# Magnetic Storage

As platters spin drive heads read the sectors that is filled with data when the sector moves under the head.
![][https://i.imgur.com/z5JgbGn.png]
This data gets read because of the positive or negative polarisation of magnetic particles creates a binary pattern on the disk. Each electromagnetic pulse is read as a one with no pulse is read as a 0.
Fitting more data in the same physical space has required technological changes such as:
- More densely packed platters
- Smaller magnetic parts and read/write heads
- Perpendicular over longitudinal recording ![](https://i.imgur.com/sy7qMHK.png)

## Disk Latency

- Latency is the time taken to read/write disk data, types of latency includes:
	- Seek delay - The time the head takes to move across the disk
	- Rotational delay - the time the disk takes to move to the correct sector underneath the read/write head
	- Transfer time to move the actual data

# Optical Storage

CDs work on similar principles with high powered laser 'burns' pits into the CD surface. A low powered laser then detects the reflection from the pits and lands. Only a pit end or start deflects the laser light to be read as binary 1 by the light sensor.
![](https://i.imgur.com/9RD7igu.png)

Optical storage also has different disk formats with each using slightly different techniques to achieve a differential between a 'pit' and a 'land':
	- Recordable formats use a transparent dye that becomes opaque when heated by a laser
	-  Re-writable formats use a laser to change the state of a phase-change alloy and a magnet to set the new state.
Different forms of Optical storage (ie cd vs dvd vs bluray) uses different laser wavelengths which burn smaller pits and then more tightly wound creating more space

# Solid State Devices

Flash memory contains no moving parts. Floating gate transistors trap and store a charge.
![](https://i.imgur.com/v7IatUX.png)
Cells are combined in blocks
	An electron trapped inside the middle layer reads as a 0, outside the middle is read as a 1.
	Data must be read, deleted or written in blocks.
	Data cannot be overwritten without being erased first.
	![](https://i.imgur.com/hGqK3MR.png)
	Cells are also managed by a controller that organises pages and blocks of memory.

The advantages of an SSD over a traditional hard disk:
- Faster access speed as there is no moving read/write head
- Lower power consumption
	- Extended battery life in portable devices
	- Devices stay cooler
- Less susceptible to damage
- Silent in operation
- Lighter in weight