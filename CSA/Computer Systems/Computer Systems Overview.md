# Hardware & Software
## Relationship between hardware and software
**Hardware** - Any physical parts of a computer and related devices
**Internal Hardware** - Motherboards / Hard drives / RAM
**External Hardware** - Monitors / Keyboards / Mouse / Printers / Web Cam
**Software** - Computer Programs (non-physical)

---
## Classification of software
**System Software** -System software operates, controls and maintains the computer and its components. Ex. OS, Utility Programs (Firewalls/Drivers/Virus Checkers), Libraries, Translators (Compilers/Assemblers/Interpreters)

**Application Software** - Programs that complete a specific task for the user.
Ex. Games/Browsers/Mail/IDEs/Apps

---
## System software 

**OS** - An operating system simplifies computer control for users by employing a virtual machine to conceal the system's complexity. It also oversees resource access, managing memory, scheduling processor tasks, and handling interrupts.

**UP** - Utility programs perform essential housekeeping tasks in a computer system, including data backup, hard drive defragmentation (reorganizing data for faster access), data compression, and encryption

********LP -******** Libraries house frequently used functions that programmers can leverage to simplify program development. To utilize a library, programmers need to import it into their code. **********TL********** - Translators are pieces of software which translate between different types of language. This course covers three types of translator: compilers, assemblers and interpreters.

## Role of an operating system (OS)****

* role of the operating system is to hide the complexities of the hardware.
* the OS handles resource management, managing hardware to allocate processors, memories and I/O devices among competing processes
---
# Classification of programming languages

Programs in low-level languages are specific to the type of processor they are written for and directly affect the computer’s processor.

There are two categories of low-level language: machine code and assembly language:

Machine code, using only binary digits, is challenging for humans to understand. Despite its error-prone nature, it provides powerful control over a computer's processor, making it beneficial for tasks like embedded systems and real-time applications that require speedy execution.

Assembly language, created to simplify computer program development, employs mnemonics like ADD and MOV instead of machine code's binary instructions. This results in more concise and less error-prone code, with a direct 1-to-1 correlation between assembly language and machine code instructions.

*High-level languages Ex. C#, Java, Pascal, Python, and VB

High-level languages, unlike low-level ones, are platform-independent but require compilation or interpretation to machine code before execution. They use English instructions and mathematical symbols, making them more human-friendly and easier to debug. Built-in functions save programming time, and features like named variables enhance debuggability. Imperative high-level languages dictate task completion instructions, contrasting with declarative programming.

---
# Types of program translator

For a computer's processor to execute a program, it must be in machine code. This requires translation of programs written in assembly language or high-level languages into machine code before execution.

There are three types of program translator: **assemblers, compilers and interpreters:**

An **assembler** converts assembly language into machine code with a direct 1-to-1 relationship between assembly and machine code instructions, making the translation quick and straightforward. However, assemblers are platform-specific, requiring a distinct assembler for each processor instruction set.

A **compiler** translates high-level language programs like C# and Python into machine code, checking for errors before generating platform-specific code. Compiled programs can run independently without the need for additional software, a contrast to interpreters.

**Interpreters** translate high-level languages line-by-line, checking for errors on the fly. They allow partial translation of programs with errors but require both the source code and interpreter for execution, offering less source code protection compared to compilers.

Some compilers translate source code into an intermediate language like bytecode for platform independence. This allows a single translation of the source code, which can then be executed on different processors using a virtual machine tailored to each processor's instruction set.

Source code refers to the input for a translator, being assembly language code for an assembler and high-level language code for compilers and interpreters. The output from a translator is known as object code, generated from the provided source code.
