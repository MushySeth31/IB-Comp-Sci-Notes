# Operating System
#### A software that manages and handles hardware and software resources for computing devices. It is the layer that sits between humans and the computer hardware, hiding all the hardware complexity and allowing users and programs to interact with the system. 

### Why the need for operating systems
Computers only understand machine-level operations such as:
- Binary instructions
- CPU registers
- Memory addresses
- Hardware signals

Humans, however, think in terms of:
- Files
- Programs
- Clicking icons
- Typing commands

#### Without the operating system, users would have to manually control hardware using machine code.

### What an operating system does
An operating system is a software that:
- Manages system resources
- Provides an interface for users and applications
- Ensures the system runs efficiently, securely, and reliably

It coordinates with:
- CPU
- Memory
- Storage
- I/O Devices
- Network Connection

---

## System Integrity
Keeping the computer stable and usable, even when:
- Multiple processes run simultaneously
- Resources are shared
- Errors occur

### Error detection and Recovery
The OS detects hardware and software faults. It quickly uses recovery mechanisms to prevent a total system crash.

### Process isolation (Sandboxing)
Each process runs in its own protected memory space. Because of this, a crash in one application does not crash the entire system.

---

## Processes and Multitasking

### Process
An instance of a program currently being executed.

Each process has its own:
- Memory allocation
- State
- CPU usage

Running the same application twice is considered two seperate process.

### Multitasking
Unless multiple cores are involved, multitasking is not true paraellism.

Instead, the OS:
- Rapidly switches the CPU between processes
- Creates the illusion that everything is running at the same time

This is achieved through context switching.

#### Context Switching
When switching processes, the OS:
- Saves the current CPU state (registers, pc, memory)
- Loads the save state of another process
- Continues execution seamlessly

---

## Process Management
