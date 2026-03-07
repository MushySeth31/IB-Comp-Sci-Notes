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

## Key Registers:

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
The communication system between the CPU and memory

## Key Buses:

### Address Bus
One-way communication (CPU -> Memory).

Carries the memory address.

### Data Bus
Two way communication.

Transfers actual data.

### Control Bus
Carries signals:
- Read/Write
- Clock
- Interrupts

Control bus is how the CU controls everything else.

---

## Instruction Cycle (Fetch-Decode-Execute)
The process that the CPU follows from boot-up until the computer has shut down in order to process instructions.

### Fetch Stage
The CPU retrives an instruction from RAM.
1. PC -> MAR
2. Address bus -> RAM
3. Insruction (from RAM) -> MDR
4. MDR -> IR

Fetch is about getting instructions.

### Decode Stage
CU decodes instruction in IR.

Determines:
- Operation type
- Operand location
- Required control signal

### Execute Stage
1. ALU performs operation.
2. Data is moved between registers/memory.
3. Result is stored in the AC or RAM.

The CPU repeats this process thousands to billions of times per second.

---

## Memory
Data accessed by the CPU,

Organized as a hierarchy to balance:
- Speed
- Cost
- Capacity

| Feature | Registers | Cache | RAM | Secondary Storage |
|----------|----------|----------|----------|----------|
| Location   | Inside CPU   | Near CPU   | Motherboard   | Motherboard or connected via cables   |
| Speed   | Fastest   | Very Fast   | Slower   | Slowest   |
| Size   | Tiny   | Small   | Large   | Extremely Massive   |
| Cost   | Very High   | High   | Lower   | Lowest   |

---

## Cache Memory
Stores frequently used data/instructions.

Reduces RAM access.

Tries to predict future requests.

#### Cache Hit -> Data found in cache -> Instant

#### Cache Miss -> Data not found in cache -> Fetch from RAM -> Slow

Cache miss are major performance killers.

### Levels of Cache
- L<sub>1</sub> -> Fastest, Smallest, Closest
- L<sub>2</sub> -> Larger, Slower than L<sub>1</sub>
- L<sub>3</sub> -> Shared between cores, Largest, Slowest

CPU checks cache -> RAM -> Secondary Storage

### Locality of Reference
Temporal -> Recently used data is likely used

Spatial -> Nearby data likely used soon

---

## RAM
Computer's active working memory.

Stores:
- Programs
- Active data

Ram is volatile. If power turns off, contents disappear, any unsaved data is lost.

Slower than cache, faster than secondary storage.

More ram allows more programs to be open simultaneously.

### Ram interaction with CPU
Data must move:
- RAM -> Cache -> Register

CPU cannot execute directly from RAM.

---

## Multicore Processors
Each core has:
- Its own register
- Usually its own L<sub>1</sub> cache

Like a mini-CPU

Shares:
- L<sub>3</sub> cache
- RAM

### Pipelining
A processor technique that breaks instruction processing into sequential stages and overlaps them, allowing multiple instructions to work on different stages simultaneously.

#### Example:

No pipelining:

One core does all the fetch, decoding, and executing.

With pipelining:


