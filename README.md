Memory Allocation and Process Management
This project focuses on understanding and demonstrating memory allocation techniques on the stack and heap, along with a deeper understanding of process management, including context management in an operating system kernel, specifically in Linux.

Table of Contents
Project Description
Objectives
Key Concepts
Memory Allocation: Stack vs Heap
Process and Thread Context
Kernel and System Architecture
Conclusion
Project Description
This project investigates the differences in memory allocation on the stack and heap in operating systems and explores how the kernel manages these memory areas. The focus is also on understanding the relationship between process contexts and thread contexts as managed by the kernel, particularly in a Linux environment.

The project also touches upon the context switching mechanism, the Process Control Block (PCB), and the role of the stack and heap in process and thread execution.

Objectives
The key objectives of this project include:

Understanding how memory is allocated on the stack and heap.
Exploring the differences in performance and management of memory between stack and heap allocations.
Analyzing the kernel's role in process and thread management, especially in relation to memory management and context switching.
Investigating the process context and thread context as part of the kernel's internal mechanisms.
Key Concepts
Stack Allocation:

The stack is used for local variables and function calls. It's a region of memory where each function call adds a stack frame, which holds the function's local variables, return address, and other information necessary for the function’s execution.
Memory is allocated automatically and freed when the function exits.
Stack size is limited, and excessive allocation can lead to a stack overflow.
Heap Allocation:

The heap is used for dynamic memory allocation. Memory is allocated at runtime, and the programmer is responsible for manually freeing the memory when it is no longer needed.
The heap has no strict size limitations (other than system memory), and it is typically used for objects whose lifetime is not confined to a single function call.
Process Control Block (PCB):

The PCB is a data structure used by the kernel to manage processes. It contains essential information about a process, such as the process state, program counter, CPU registers, memory management information, and more.
Context Switching:

Context switching refers to the mechanism that allows the CPU to switch between different processes or threads. This involves saving the state of the current process (its context) and loading the state of the next process.
Process and Thread Context:

The process context includes information about the execution state of a process, such as memory mapping and register values.
The thread context refers to the information related to individual threads within a process, including thread-specific data and the stack used by that thread.
Memory Allocation: Stack vs Heap
Stack Memory:
Characteristics:

Automatically allocated when a function is called and deallocated when the function returns.
Memory management is handled by the system.
Limited size — large allocations can lead to stack overflow.
Fast allocation and deallocation.
Usage:

Ideal for small, temporary allocations, such as function call variables or arrays with fixed size.
Heap Memory:
Characteristics:

Dynamically allocated and deallocated during runtime.
The programmer is responsible for managing memory (allocating and freeing).
Virtually unlimited size (subject to system memory).
Slower allocation and deallocation compared to stack memory.
Usage:

Suitable for large or variable-sized data that needs to persist outside the scope of a function call.
Process and Thread Context
Process Context:
The kernel saves and restores the process context during context switches, ensuring that each process continues execution from where it left off.
The context includes the process's stack, registers, and memory mappings.
Thread Context:
Similar to process context, but specific to threads. Each thread within a process has its own context and stack.
The kernel manages the thread context for efficient multitasking and thread execution.
Kernel and System Architecture
The kernel is responsible for managing system resources, including memory, processes, and threads. It ensures that processes and threads are scheduled and executed effectively.
The Process Control Block (PCB) plays a vital role in storing the context of each process, enabling efficient context switching.
Memory management is handled by the kernel through memory management units (MMUs) and involves managing both stack and heap areas.
In Linux, the kernel manages memory allocation, virtual memory, and context switching using a combination of hardware and software techniques.

Conclusion
This project highlights the importance of memory management in modern operating systems, particularly in the context of the stack and heap. It demonstrates how the kernel manages processes and threads, the role of context switching, and how it uses PCBs to manage the state of each process. Understanding the stack and heap, as well as their interactions with system processes, is critical for efficient resource management and performance optimization in operating systems.
