[[Computer Organisation and Architecture]]
# Internal hardware components of a computer
---
- [ ] *Have an understanding and knowledge of the basic internal components of a computer system.*
- [ ] *Understand the role of the following components and how they relate to each other:* 
	• processor
	• main memory
	• address bus 
	• data bus 
	• control bus 
	• I/O controllers.
- [ ] *Understand the need for, and means of, communication between components. In particular, understand the concept of a bus and how address, data and control buses are used.*
- [ ] *Understand the need for, and means of, communication between components. In particular, understand the concept of a bus and how address, data and control buses are used.*
- [ ] *Understand the concept of addressable memory*
---
### Processor
A computer’s processor executes program instructions in order to run applications. further details within [[Sub/Structure and role of the processor and its components]].

### Main Memory
A computer uses its main memory (RAM/ROM), to store program instructions and frequently used data to execute instructions quickly. (Primary Storage faster than Secondary Storage)

### Buses
>A bus is a series of parallel wires that connects internal components of a computer system, allowing signals to be passed between them.

*The number of parallel wires in a bus is called its width and has a direct relationship to the number of bits can be transferred simultaneously by the bus.*

#### Address Bus
The address bus is used to transport memory addresses, specifying where data is to be sent to or retrieved from. 

*Increasing the width of the address bus increases the range of addresses that it can specify, hence increasing the computer’s amount of addressable memory. Adding a single wire doubles the number of addressable memory locations.*
#### Data Bus
A computer’s data bus sends data and instructions to and from the different components of the computer system.

*Increasing the width of the data bus increases the volume of data that can be transferred over the bus at any one time.*

#### Control Bus
The control bus is used to carry control signals that regulate the operation of the computer system. The control bus also carries the computer’s clock signal.

### I/O Controllers
Pieces of hardware that control the communication of data between the processor and external hardware devices such as keyboards, mice and monitors

### Addressable Memory
>An addressable memory location is a portion of memory that can be accessed by its address. If there are not enough addresses available, some portions memory may go unused.

\***OUT OF SPEC:** Two different ways of setting up a processor’s access to main memory: [[Von Neumann and Harvard architectures]]
