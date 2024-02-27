# Multi-Cycle-RISC-Processor-In-Verilog-
design, and implementation of a Multi Cycle Processor  according to a given RISC instruction set.

# Introduction
## Objective
The objective of this project is to successfully design, model and simulate a MIPS 
Multi-Cycle Processor using Verilog HDL. The design approach was used where 
each sub-module of the processor was first designed, coded, and tested. Once all 
sub-modules were designed and determined to be fully functional, they were 
instantiated into a structural module to form our processor.
## Introduction to RISC Machines
RISC is a type of CPU design in which it is believed that a simplified instruction 
set will enhance performance of the processor. It uses a small, highly-optimized 
set of instructions rather than a more complex set as found in other processors. 
The word “reduced” in the name refers to the amount of work for any single 
instruction set.
Typical features of RISC architecture include: fixed length, standard format, 
identical general-purpose registers, simple addressing modes, one cycle execution 
time, and pipelining.
Aside from quicker performance, RISC processor components are generally 
cheaper to design and produce as they utilize less transistors. RISC is the newer 
technology and is widely used in the industry compared to other processor types.
## Multi Cycle Processors
A multi-cycle processor is a type of processor architecture that divides the 
execution of instructions into multiple stages or cycles. Each cycle performs a 
specific operation, allowing instructions to be executed efficiently and enabling 
more complex instructions to be processed. Using the Multi-cycle approach, 
different instruction may take different amounts of time to process unlike in the 
Single-cycle approach where instruction processing is as fast as the slowest 
instruction.
In a multi-cycle processor, each instruction goes through several stages, with each 
stage completing within a single clock cycle. The stages typically include:
### 1. Instruction Fetch (IF): The processor fetches the instruction from memory 
using the program counter (PC) and increments the PC to point to the next 
instruction.
### 2. Instruction Decode (ID): The fetched instruction is decoded to determine 
the operation to be performed. This stage also involves fetching any 
necessary operands or data from registers.
### 3. Execution (EX): The actual operation specified by the instruction is 
performed in this stage. It may involve arithmetic calculations, logical 
operations, or address computations.
### 4. Memory Access (MEM): If the instruction requires accessing memory, 
such as loading or storing data, it is performed in this stage. Data is read 
from or written to memory.
### 5. Write Back (WB): The results of the previous stage are written back to the 
appropriate register(s). This stage updates the register file with the 
computed values
## Processor Properties
1. The instruction size is 32 bits.
2. 32 32-bit general-purpose registers: from R0 to R31.
3. A special purpose register for the program counter (PC).
4. It has a stack called control stack which saves the return addresses
5. Stack pointer (SP), another special purpose register to point to the top of the 
control stack. SP holds the address of the empty element on the top of the 
stack. For simplicity, you can assume a separate on-chip memory for the 
stack, and the initial value of SP is zero.
6. Four instruction types (R-type, I-type, J-type, and S-type).
7. The processor’s ALU has an output signal called “zero” signal, which is 
asserted when the result of the last ALU operation is zero.
8. Separate data and instructions memories
## Conclusion
The design for a multi-cycle system must be precise and accurate, and it requires 
a large number of components.
NOTE: some delays has been added for each execution stage to make a 
correction of flow of the instruction execution and to prevent glitches, also to 
give enough time for read and write operations and prevent conflicts
