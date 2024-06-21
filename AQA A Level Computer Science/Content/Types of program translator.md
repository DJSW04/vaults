[[6. Computer Systems]]
# Types of program translator
>For a computer's processor to execute a program, it must be in machine code. This requires translation of programs written in assembly language or high-level languages into machine code before execution.

There are three types of program translator: **assemblers, compilers and interpreters:**

An **assembler** converts assembly language into machine code with a direct 1-to-1 relationship between assembly and machine code instructions, making the translation quick and straightforward. However, assemblers are platform-specific, requiring a distinct assembler for each processor instruction set.

A **compiler** translates high-level language programs like C# and Python into machine code, checking for errors before generating platform-specific code. Compiled programs can run independently without the need for additional software, a contrast to interpreters.

**Interpreters** translate high-level languages line-by-line, checking for errors on the fly. They allow partial translation of programs with errors but require both the source code and interpreter for execution, offering less source code protection compared to compilers.

Some compilers translate source code into an intermediate language like bytecode for platform independence. This allows a single translation of the source code, which can then be executed on different processors using a virtual machine tailored to each processor's instruction set.

Source code refers to the input for a translator, being assembly language code for an assembler and high-level language code for compilers and interpreters. The output from a translator is known as object code, generated from the provided source code.