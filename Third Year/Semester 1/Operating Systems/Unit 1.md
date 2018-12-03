# Operating Systems
## Unit 1: Overview of Operating Systems

### Operating System
**Operating System:**
An OS is a program that acts an intermediary between the user of a computer and its hardware. Simply stated, an OS simply provides an interface between the user and the hardware.

**Functions of an OS:**
- Process management
- Memory management
- I/O device management
- File management
- System protection and security
- Program execution
- Provides support for networking

**Kernel:**
The kernel is the core part of an OS. It is a program which is running at all times on the computer.

### The Evolution of Operating Systems
- The evolution process of operating systems is divided into different generations. The following are the types of the operating systems that have been in use since the beginning of the computing period:
  - Simple Batch Processing System
  - Multiprogramming Batch Processing Systems
  - Multi-process systems (Multi-testing systems)
  - Time sharing systems
  - Multi user systems
  - Real time systems

### Developments Leading to Modern Operating Systems
**Monolithic kernel:**
- The traditional UNIX OS uses a monolithic kernel.
- In a monolithic kernel, the entire OS runs as a single program in kernel mode.
- The program contains the OS, the core functions (process management, memory management, File and I/O management), and drivers for I/O devices. Eg: Linux OS, Free BSD, Windows 95, 98.

*Draw diagram*

**Microkernel:**
- In this, only the absolutely essential functions are in the core OS.
- Less essential services/applications are built on the microkernel and are executed in user mode.
- Many services that were traditionally part of the OS are now external sub-systems with the kernel and each other. These include device drivers, file systems, virtual memory manager, windowing system, and security services.
  The microkernel only provides Inter-Process Communication (IPC), low level device management services and some basic scheduling.

*Draw diagram*

