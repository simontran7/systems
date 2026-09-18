# Introduction

An **operating system (OS)** is the core software that manages a computer's hardware and provides a platform for running other software (applications).

An operating system is analogous to:
- An illusionist: it provides clean, easy-to-use abstractions of physical resources
  - Processor → Thread
  - Memory → Address Space
  - Disks, SSDs, … → Files
  - Networks → Sockets
  - Machines → Processes
- A referee: it manages protection, isolation, and sharing of resources
- Glue: it glues common services together

## Organization

An operating system can be broken down into three parts:
- Kernel
- Systems program
- Application program

The hardware provides at least two privilege modes:
- Kernel mode
  - full access to all hardware
  - only the OS kernel runs here
- User mode
  - restricted access
  - regular applications run here

A special register or flag in the CPU tracks which mode it's currently in, and this restricts which instructions can be executed and which memory can be accessed.

In order for applications programs to perform priviledge operations, it involves from user mode to and must ask the kernel (via **system calls**) to do privileged operations like reading a file or accessing the network 



The kernel is the operating system. As the figure illustrates, the kernel communicates to hardware both directly and through drivers.

Just as the kernel abstracts the hardware to user programs, drivers abstract hardware to the kernel. For example there are many different types of graphic card, each one with slightly different features. As long as the kernel exports an API, people who have access to the specifications for the hardware can write drivers to implement that API. This way the kernel can access many different types of hardware.

