# [[Abstraction and Automation]]
1. **Problem-solving**
2. **Following and writing algorithms**
3. **Abstraction**
4. **Information hiding**
5. **Procedural abstraction**
6. **Functional abstraction**
7. **Data abstraction**
8. **Problem abstraction/reduction**
9. **Decomposition**
10. **Composition**
11. **Automation**

# [[Regular languages]]
1. **Finite state machines (FSMs) with and without output**
2. **Maths for regular expressions**
3. **Regular expressions**
4. **Regular language**

# [[Context-free languages]]
1. **Backus-Naur Form (BNF)/syntax diagrams**

# [[Classification of algorithms]]
1. **Comparing algorithms**
2. **Maths for understanding Big-0 notation**
3. **Order of complexity**
4. **Limits of computation**
5. **Classification of algorithmic problems**
6. **Computable and non-computable problems**
7. **Halting problem**

# [[A model of computation]]
1. **Turing machine**


>**Following and writing algorithms:** an algorithm is a sequence of steps necessary to accomplish a certain task.

**Abstraction:** the process of separating ideas from reality.

>Representational abstraction means omitting unnecessary information.

>Abstraction by generalisation/categorisation is a grouping by common characteristics to arrive at a hierarchal relationship of the “is kind of” type.

**Procedural Abstraction:** result of abstracting away the actual values used in any particular computation is a computational pattern/method - a procedure.

**Functional Abstraction:** result of a procedural abstraction is a procedure not a function. to get a function requires yet another abstraction, which disregards the particular computation method.

**Data Abstraction:** methodology that enables us to isolate how a compound data object is used from the details of how it is constructed.

**Problem abstraction/reduction:** removing details from a problem until you can represent it in a way that is possible to solve, because the problem has been reduced to one that has already been solved.

**decomposition:** breaking a problem into a number of subproblems, so that each sub-problem accomplishes an identifiable task, which might itself be further subdivided.

**Information hiding:** hiding design details behind a standard interface.

**Composition:** combining simpler functions or modules to create more complex ones. It allows for modular design, code reusability, and enhances code readability. This concept is crucial in functional programming.

---

**Regex:**
1. **Metacharacters**: Special characters in regex define patterns. For example, **`.`** matches any character, **``** matches zero or more occurrences, etc.
2. **Character Classes**: Define sets of characters to match. **`[0-9]`** matches any digit, **`[a-zA-Z]`** matches any letter, and so on.
3. **Quantifiers**: Indicate the quantity of times a character or group must occur. For instance, **`+`** matches one or more occurrences, **`?`** matches zero or one occurrence.
4. **Anchors**: Specify the position within the text. **`^`** matches the start of a line, **`$`** matches the end.
5. **Escape Sequences**: Allow literal interpretation of metacharacters. For example, **`\\.`** matches a literal period.
6. **Alternation**: Using **`|`** allows for alternatives. For instance, **`A|B`** matches either "A" or "B".
7. **Grouping and Capturing**: Parentheses **`()`** group expressions and allow capturing of matched text for later use.
8. **Modifiers**: Control the matching behaviour, like case insensitivity (**`/i`** flag).
9. **Greedy vs. Non-Greedy**: Greedy matching (**`*`**, **`+`**) matches as much as possible, while non-greedy (**`*?`**, **`+?`**) matches as little as possible.

>The Halting Problem states that there's no algorithm to determine if any given program will halt or run indefinitely.

>A Turing Machine is an abstract mathematical model of computation. It consists of a tape with cells, a read/write head, and a set of rules for transitioning between states. It can simulate any algorithm and is pivotal in understanding the limits of computation.