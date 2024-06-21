[[11. Big Data]]

---
- [ ] *Know that 'Big Data' is a catch-all term for data that won't fit the usual containers. Big Data can be described in terms of:*
	• **volume** - too big to fit into a single server 
	• **velocity** - streaming data, milliseconds to seconds to respond 
	• **variety** - data in many forms such as structured, unstructured, text, multimedia.
- [ ] *Know that when data sizes are so big as not to fit on to a single server:* 
	• the processing must be distributed across more than one machine 
	• functional programming is a solution, because it makes it easier to write correct and efficient distributed code.
- [ ] *Know what features of functional programming make it easier to write:*
	• correct code 
	• code that can be distributed to run across more than one server.
- [ ] *Be familiar with the:* 
	• fact-based model for representing data 
	• graph schema for capturing the structure of the dataset 
	• nodes, edges and properties in graph schema.
---
## **FACT BASED MODELLING**

> Fact based modelling deconstructs data into fundamental units called ‘facts’ and adds them into a master dataset. The master dataset is an ever-growing list of immutable atomic facts

**PRINCIPLES OF FBM**
1. Raw data stored as atomic facts
2. Facts capture one single piece of information
3. Facts are immutable and eternally true (due to timestamp)
4. Each is identifiable so querying can identify duplicates

_**Advantages**_
- Simplicity (NO INDEXING NEEDED)
- New items are appended to the growing dataset
- Data is true forever
- Immutable facts means errors are easy to correct by returning to earlier ‘good’ facts
- Historical queries easy to run as facts are immutable

## **BIG DATA & [[12. Functional Programming|FUNCTIONAL PROGRAMMING]]**

>when data volumes are so large the processing of the datasets must be distrusted across more than one machine which can present unique problems when analysing it using traditional programming methods. functional programming is one solution

**Advantages**
- Functions have a ‘side-effect’ if they modify anything about the calling program, functional languages are ‘stateless’ however which results in code being easy to interpret/write and predict behaviour
- Higher-order functions are easily parallelised
- Immutable data structures means parallel processing can be easy (same function returns same result)

**Statelessness / Higher-order functions / Immutable data structures***

> Big data are extremely large datasets that may be analysed computationally to reveal patterns / trends / associations relating to human behaviour and interactions

**Volume:** Too big to fit in a single server
**Velocity:** Streaming data (milliseconds → seconds response)
Variety: Data can arrive in various formats

**ISSUES WITH VARIETY**
- Makes analysing data more difficult
- relational databases cannot be used and don’t scale well across multiple servers

**Machine learning techniques used to analyse big data**