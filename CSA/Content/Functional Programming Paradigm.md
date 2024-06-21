[[12. Functional Programming]]

**MAIN FEATURES OF FUNCTIONAL PROGRAMMING**
- **Statements** written as a series of functions
- **Statements** accepts inputs as arguments & returns outputs
- **Stateless** & **Immutability**

_**ADVANTAGES**_
- Code easier to write & interpret
- Easier to predict program behaviour
- Less prone to bugs
- Ideal for processing big data (CPU parallel processing)
# Function Type
---
- [ ] *Know that a function, $f$, has a function type $f: A → B$ 
	(where the type is $A → B$, $A$ is the argument type, and $B$ is the result type).* 
- [ ] *Know that $A$ is called the domain and $B$ is called the co-domain.* 
- [ ] *Know that the domain and co-domain are always subsets of objects in some data type.*
---

>A **function** is a rule, that for each element of set A (domain) of inputs, assigns an output chosen from set B (co-domain), but without necessarily using every member of B.

**FUNCTIONS ARE FIRST-CLASS OBJECTS**
$$ {A ⇒ B \quad Where: f(x) = x^{2}} $$
$\text{A = argument type, B = result type}$
# First-class object
---
- [ ] *Know that a function is a first-class object in functional programming languages and in imperative programming languages that support such objects. This means that it can be an argument to another function as well as the result of a function call.*
---
# Function Application
---
- [ ] *Know that function application means a function applied to its arguments*
---
>**Function Application** is the process of giving inputs to functions
* Functions only takes one argument (in Haskell)
# Partial Function Application
---
- [ ] Know what is meant by partial function application for one, two and three argument functions and be able to use the notations shown opposite.
---
>**Partial Function Application** is the process of decomposing multi-argument functions into smaller functions with less arguments
- Partial application results in ‘binding’ the value of some of the inputs to a function to produce another more specific function
# Composition of Functions 
---
- [ ] Know what is meant by composition of functions.
---
>**Composition of Functions** is the idea that you can combine two functions to get a new function

$$L : A \rightarrow B \Rightarrow K \circ L : A \rightarrow C$$
$A = domain, B = co\text{-}domain$

Function $K \circ L$  is known as the composition of K and L
- Co-domain of L must be the same as the domain of K