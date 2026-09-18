# Kernel Interface

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

The operating system's core program that always runs is called the **kernel**.

The kernel communicates to the hardware directly, or through systems programs called **drivers**.

## Priviledges

The hardware provides at least two privilege modes:
- Kernel/supervisor/priviledged mode
  - full access to all hardware
  - the kernel is the systems program that runs here
- User mode
  - restricted access
  - regular applications programs run here

This is enforced by a special register or a flag in the CPU that tracks which mode it's currently in. Whenever this flag is enabled, the hardware restricts which instructions can be executed and which memory can be accessed.

In order for applications programs to perform priviledge operations, it needs to transition from user mode to kernel mode. This is accomplished by requesting the kernel via **system calls** to do privileged operations

<img src="images/user_mode_kernel_mode_transition.svg" width="500">



