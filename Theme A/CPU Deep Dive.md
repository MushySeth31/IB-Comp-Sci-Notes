# CPU: Deep Dive
#### Focus on CPU architecture

## Central Processing Unit (CPU)
The CPU executes machine instructions and controls the entire computer system.

The CPU is built around:
- Instruction execution
- Data movement
- Control signals
- Speed optimization

Core components of the CPU:
- Arithmetic Logic Unit (ALU)
- Control Unit (CU)
- Registers

---

## Arithmetic Logic Unit (ALU)
Performs all computational work.

Operations include:
- Arithmetic (+, -, *, /)
- Logical (AND, OR, NOT)
- Comparison (>, <, ==)

Internally:
- Uses logic gates
- Operates on binary values
- Results are written to registers (often the Accumulator)

ALU does not decide what to do, only executes,

---

## Control Unit (CU)
The conductor of the CPU.

It:
- Generates control signals
- Interprets instructons (Decode)
- Coordinate data flow between
- - ALU
  - Registers
  - Memory
  - I/O

---

## Registers
Extremely tiny, ultra-fast memory in the system located in the CPU.

Why the need for registers:
- RAM is slow compared to CPU speed
- Registers eliminate delays
- Every instruction depends on registers

Key Registers:

### Program Counter (PC)
Stores the address of the next instruction, automatically increments after each fetch. Changes during jump/branches.

### Instruction Register (IR)
Holds the current instruction. The CU decodes this register.

### Memory Address Register (MAR)
Stores the memory address to access. Connected to the address bus.

### Memory Data Register (MDR)
stores the data being transferred to/from RAM. Works with data bus.

### Accumulator
Stores the intermediate result (ALU result). Common in simple CPU architecture.

MAR -> Where
MDR -> What

---

## Buses
