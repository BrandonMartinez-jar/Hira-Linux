# Preface:

Greetings!
You’ve probably asked yourself at least once how an operating system is written from the ground up. You might even have years of programming experience under your belt, yet your understanding of operating systems may still be a collection of abstract concepts not grounded in actual implementation. To those who’ve never built one, an operating system may seem like magic: a mysterious thing that can control hardware while handling a programmer’s requests via the API of their favorite programming language. Learning how to build an operating system seems intimidating and difficult; no matter how much you learn, it never feels like you know enough. You’re probably reading this book right now to gain a better understanding of operating systems to be a better software engineer. 
If that is the case, this book is for you. By going through this book, you will be able to find the missing pieces that are essential and enable you to implement your own operating system from scratch! Yes, from scratch, without going through any existing operating system layer to prove to yourself that you are an operating system developer. You may ask,“Isn’t it more practical to learn the internals of Linux?”. Yes... and no. Learning Linux can help your workflow at your day job. However, if you follow that route, you still won’t achieve the ultimate goal of writing an actual operating system. By writing your own operating system, you will gain knowledge that you will not be able to glean just from learn-ing Linux. 

### Here’s a list of some benefits of writing your own OS:
- You will learn how a computer works at the hardware level, and you
will learn to write software to manage that hardware directly
- You will learn the fundamentals of operating systems, allowing you to adapt to any operating system, not just Linux
- To hack on Linux internals suitably, you’ll need to write at least one operating system on your own. This is just like applications   programming: to write a large application, you’ll need to start with simple ones.
- You will open pathways to various low-level programming domains such as reverse engineering, exploits, building virtual machines, game console emulation and more. Assembly language will become one of your most indispensable tools for low-level analysis. (But that does not mean you have to write your operating system in Assembly!
- Writing an operating system is fun

### Why another book on Operating Systems?
There are many books and courses on this topic made by famous professors and experts out there already. Who am I to write a book on such an advanced topic? While it’s true that many quality resources exist, I find them lacking. Do any of them show you how to compile your C code and the C runtime library independent of an existing operating system? Most books on operating system design and implementation only discuss the software side; how the operating system communicates with the hardware is skipped. Important hardware details are skipped, and it’s difficult for a self-learner to find relevant resources on the Internet. 
One of the core focuses of this book is to guide you through the process of reading official documentation from vendors to implement your software. Official documents from hardware vendors like Intel are critical for implementing an operating system or any other software that directly controls the hardware. At a minimum, an operating system developer needs to be able to comprehend these documents and implement software based on a set of hardware requirements. Thus, the first chapter is dedicated to discussing relevant documents and their importance.
Another distinct feature of this book is that it is “Hello World” centric. Most examples revolve around variants of a “Hello World” program, which will acquaint you with core concepts. These concepts must be learned before attempting to write an operating system. Anything beyond a simple “Hello World” example gets in the way of teaching the concepts, thus lengthening the time spent on getting started writing an operating system. 
Let’s dive in. With this book, I hope to provide enough foundational knowledge that will open doors for you to make sense of other resources. This book will be beneficial to students who’ve just finished their first C/C++ course greatly. Imagine how cool it would be to show prospective employers that you’ve already built an operating system.

## Prerequisites
### Basic knowledge of circuits
- Basic concepts of electricy: atoms, electrons, proton, neutron, current flow.
- Ohm's law.
If you are unfamiliar with these concepts, you can quickly learn them [here](http://www.allaboutcircuits.com/textbook/), by reading chapter 1 and chapter 2.

### C programming in particular
- Variable and function delclarations / definitions.
- While loops.
- Pointers and function pointers.
- Fundamental algorithms and data structures in C.

### Linux Basics
- Know how to navigate directory with the command line interface (CLI).
- Know how to invoke a command with options.
- Know how to pipe output to another program.

### Touch typing.
Since we are going to use Linux, touch typing helps. I know typing speed does not relate to problem-solving, but at least your typing speed should be fast enough not to let it get in the way and degrade the learning experience.
In general, I assume that the reader has basic C programming knowledge, and can use an IDE to build and run a program.

## What you will learn in this book
- How to write an operating system from scratch by reading hardware datasheets. In the real world, you will not be able to consult Google for a quick answer.
- Write code independently. It’s pointless to copy and paste code. Real learning happens when you solve problems on your own. Some examples are provided to help kick start your work, but most problems are yours to conquer. However, the solutions are available online for you after giving a good try.
- A big picture of how each layer of a computer related to each other, from hardware to software.
- How to use Linux as a development environment and common tools for low-level programming.
- How a program is structured so that an operating system can run.
- How to debug a program running directly on hardware with gdb and QEMU.
- Linking and loading on bare metal x86_64, with pure C. No standard library. No runtime overhead.

## What this book is not about
- Electrical Engineering: The book discusses some concepts from electronics and electrical engineering only to the extent of how software operates on bare metal.
- How to use Linux or any OS types of books: Though Linux is used as a development environment and as a medium to demonstrate high-level operating system concepts, it is not the focus of this book.
- Linux Kernel development: There are already many high-quality books out there on this subject.
- Operating system books focused on algorithms: This book focuses more on actual hardware platform - Intel x86_64 - and how to write an OS that utilizes of OS support from the hardware platform.
 
## The organization of the book

__Part 1:__ provides a foundation for learning operating system.
- Chapter 1: briefly explains the importance of domain documents. Documents are crucial for the learning experience, so they deserve a chapter.
- Chapter 2: explains the layers of abstractions from hardware to software. The idea is to provide insight into how code runs physically.
- Chapter 3: provides the general architecture of a computer, then introduces a sample computer model that you will use to write an operating system.
- Chapter 4: introduces the x86 assembly language through the use of the Intel manuals, along with commonly used instructions. This chapter gives detailed examples of how high-level syntax corresponds to low-level assembly, enabling you to read generated assembly code comfortably. It is necessary to read assembly code when debugging an operating system.
- Chapter 5: dissects ELF in detail. Only by understanding how the structure of a program at the binary level, you can build one that runs on bare metal.
- Chapter 6: introduces gdb debugger with extensive examples for commonly used commands. After acquainting the reader with gdb, it then provides insight on how a debugger works. This knowledge is essential for building a debuggable program on the bare metal

__Part 2:__ presents how to write a bootloader to bootstrap a kernel. Hence the name “Groundwork”. After mastering this part, the reader can continue with the next part, which is a guide for writing an operating system. However, if the reader does not like the presentation, he or she can look elsewhere, such as [OSDev_Wiki](http://wiki.osdev.org/).
- Chapter 7: introduces what the bootloader is, how to write one in assembly, and how to load it on QEMU, a hardware emulator. This process involves typing repetitive and long commands, so GNU Make is applied to improve productivity by automating the repetitive parts and simplifying the interaction with the project. This chapter also demonstrates the use of GNU Make in context.
- Chapter 8: introduces linking by explaining the relocation process when combining object files. In addition to a bootloader and an operating system written in C, this is the last piece of the puzzle required for building debuggable programs on bare metal, including the bootloader written in Assembly and an operating system written in C.

__Part 3:__ provides guidance on how to write an operating system, as you should implement an operating system on your own and be proud of your creation. The guidance consists of simpler and coherent explanations of necessary concepts, from hardware to software, to implement the features of an operating system. Without such guidance, you will waste time gathering information spread through various documents and the Internet. It then provides a plan on how to map the concepts to code.