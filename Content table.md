# Content Table

- Preface

### Part 1: Preliminary

1. Domain documents
    - Problem domains
    - Documents for implementing a problem domain
    - Documents for writing a x56 Operating System

2. From hardware to software: Layers of abstraction
    - The physical implementation of a bit
    - Beyond transitors: digital logic gates
    - Beyond logic gates: Machine language
    - Abstraction

3. Computer Architecture
    - What is a computer?
    - Computer architecture
    - x86 architecture
    - Intel Q35 Chipset
    - x86 Execution Environment

4. x86 Assembly and C
    - Objdump
    - Reading the output
    - Intel manuals
    - Experiment with assembly code
    - Anatomy of an Assembly Instruction
    - Understand an instruction in detail
    - Example: jmp instruction
    - Examine compiled data
    - Examine compiled code

5. The Anatomy of a Program
    - Reference documents
    - ELF header
    - Section header table
    - Understand section in-depth
    - Program header table
    - Segmens vs sections

6. Runtime inspection and debug
    - A sample program
    - Static inspection of a program
    - Runtime inspection of a program
    - How debuggers work: a brief introduction

## Part 2: Groundwork

7. Bootloader
    - x86 Boot Process
    - Using BIOS services
    - Boot process
    - Example Bootloader
    - Compile and load
    - Loading a program from bootloader
    - Improve productivity with scripts

8. Linking and loading on bare metal
    - Understanding relocations with readelf
    - Crafting ELF binary with linker scripts
    - C Runtime: Hosted vs Freestanding
    - Debuggable bootloader on bare metal
    - Debuggable program on bare metal

## Part 3: Kernel Programming

9. x86 Descriptors
    - Basic operating system concepts
    - Drivers
    - Userspace and kernel space
    - Memory Segment
    - Segment Descriptor
    - Types of segment descriptors 
    - Descriptor scope
    - Segment selector
    - Enhancement: Bootloader with descriptros

10. Process
    - Concepts
    - Process
    - Threads
    - Task: x86 concept of a process
    - Task Data Scructure
    - Process Implementation
    - Milestone: Code refactor

11. Interrupt
12. Memory Management
13. File System