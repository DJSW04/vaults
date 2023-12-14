[[Communication and Networking]]
# Communication Methods
---
- [ ] *Define serial and parallel transmission methods and discuss the advantages of serial over parallel transmission.* 
- [ ] *Define and compare synchronous and asynchronous data transmission.* 
- [ ] *Describe the purpose of start and stop bits in asynchronous data transmission.*
---
### Serial Transmission
In serial data transmission, data is sent one bit at a time over one communication line (this is usually a metal wire, but could also be an optical fibre or a wireless channel).

Serial data transmission is frequently used for transmitting data over medium to long distances (computationally speaking), such as from wired peripherals like mice and keyboards to your computer.

### Parallel Transmission
Parallel data transmission uses numerous parallel communication lines in order to send multiple bits between components in a computer simultaneously.
*The more lines that a parallel communication medium uses, the more data can be transferred simultaneously.*
![](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9d/Serial_and_Parallel_Data_Transmission.svg/300px-Serial_and_Parallel_Data_Transmission.svg.png)
Each of the communication lines that forms part of a parallel communication medium will have slightly different electrical properties, meaning that the time taken for one bit to be transferred will differ slightly from line to line. This means that bits sent together may not be received together, a problem referred to as skew.

Skew is worst over long distances and, in extreme cases, can lead to bits from different pulses overlapping, causing corruption of data. Furthermore, parallel communication mediums are more expensive than their serial counterparts because of their use of multiple lines. For these reasons, parallel data transmission is most often used over short distances, such as between parts of the processor and within RAM.

Another issue, referred to as crosstalk, can occur with parallel data transmission. When communication lines are tightly packed, signals from one line can “leak” into another, another cause of data corruption.

#### Advantages of serial over parallel
Serial data transmission doesn’t suffer from skew or crosstalk making it a more reliable communication method, especially over long distances. Serial communication mediums, which use just one line, are cheaper to install than parallel mediums which use more than one line.

### Synchronous transmission
When data is transmitted using synchronous transmission, a clock signal (which is shared by both the sender and the receiver) is used to time when signals are sent. Synchronous data transmission is used within the busses of a computer’s processor in the fetch-execute cycle. 

The signals, which are sent at regular intervals, will be received in the same order that they were sent. This makes synchronous data transmission suitable for transmitting information in real-time systems.

### Asynchronous transmission
In asynchronous data transmission, the requirement for a shared clock signal is done away with by using start and stop bits to indicate the duration of a transmission. 

The start bit can be either a 0​ or a 1​ and the stop bit is always the opposite of the start bit. 

The sender and receiver must use the same Baud rate and need only synchronise their clocks for the duration of data transmission

# Communication Basics
---
- [ ] *To be able to define:* 
	● **baud rate** 
	● **bit rate**
	● **bandwidth** 
	● **latency**
	● **protocol**  
- [ ] *Differentiate between baud rate and bit rate.* 
- [ ] *Understand the relationship between bit rate and bandwidth.*
---
**Baud rate**: the number of signal changes in the medium per second (1Bd)
**Bit rate**: the number of bits transmitted per unit time. (bps)
**Bandwidth**: the range of frequencies at which data can be transmitted through a channel, measured in Hz.
**Latency**: the time delay between the transmitter sending the data and the recipient receiving the data.
**Protocol** A set of rules used for communication.

A communication system’s bit rate is equal to its Baud rate multiplied by the number of bits per signal in the communication medium.
$$Bit \ rate = Baud \ rate \times \ № \ of \ bits \ per \ signal$$
A communication medium’s bit rate will be higher than its Baud rate if there is more than one bit sent per signal.

