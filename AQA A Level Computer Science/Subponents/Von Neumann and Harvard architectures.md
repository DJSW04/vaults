[[Internal hardware components of a computer]]

**Two different ways of setting up a processor’s access to main memory:**
# Harvard Architecture
[Harvard architecture - Wikipedia](https://en.wikipedia.org/wiki/Harvard_architecture)
- The processor will use **two separate main memory locations**. One for **instructions** and another for **data**.
- **Each piece of main memory can be given different characteristics;** 
	Memory used for instructions could be made read-only so that instructions cannot be altered
- Extensively **used in embedded systems such as digital signal processing**
![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Harvard_architecture.svg/362px-Harvard_architecture.svg.png)
# Von Neumann
[Von Neumann architecture - Wikipedia](https://en.wikipedia.org/wiki/Von_Neumann_architecture)
- **Both instructions and data are stored together in the same memory**
- The **same buses have to be shared for fetching both instructions and data**
- Systems based on von **Neumann architecture often perform worse than on Harvard architecture**
- Used in **everyday general-purpose computer systems** like laptops and smartphones
![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e5/Von_Neumann_Architecture.svg/300px-Von_Neumann_Architecture.svg.png)