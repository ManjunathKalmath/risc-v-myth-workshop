# RISC V (RV32I) CPU Core

This repository contains all the information about RISC V CPU Core that is builtin the 5-days Workshop “RISC-V based Microprocessor for You in Thirty Hours"

## Workshop Flow
- Day - 1 : Introduction to RISC-V ISA and GNU compiler toolchain
- Day - 2 : Introduction to ABI and basic verification flow
- Day - 3 : Digital Logic with TL-Verilog and Makerchip
- Day - 4 : Basic RISC-V CPU micro-architecture
- Day - 5 : Complete Pipelined RISC-V CPU micro-architecture/store

## Workshop Outcome
- Understanding of RISC V ISA
- RISC V GNU Toolchain
- TL-Verilog
- Designing the Digital Circuits using TL-Verilog
- RISC V RV32I microarchitecture

## Day - 1 : Introduction to RISC-V ISA and GNU compiler toolchain

**RISC V ISA**
RISC V is an open and free Instruction Set Architecture(ISA) which is enabling the modern processor design.RISC V ISA avoids over-architecting for a particular 
implementation technology and microarchitecture style.RISC V ISA is divided into base integer ISA and optional standard extensions such as Integer Multiplication 
and Division, Atomic Instructions,Single and Double Precision Floating Points which helps general purpose software development.

**RISC V GNU Toolchain**
1. To compile with RISC-V GCC compiler:
> `riscv64-unknown-elf-gcc <compiler option -O1 ; Ofast> <ABI specifier -lp64; -lp32; -ilp32> <architecture specifier -RV64 ; RV32> -o <object filename> <C filename>` 
2. To view the disassembly aka assembly code - RISC V :
> `riscv64-unknown-elf-objdump -d <object filename> | less `

In the workshop SPIKE RISC V ISA Simulator is used.
More on Spike Simulator Visit https://github.com/riscv/riscv-isa-sim

## Day - 2 : Introduction to ABI and basic verification flow

#### Sum 1 to n program using SPIKE
In this picture we can get to know the contents of any register by:
> `reg 0 "ABI name of register"`

![day-1](https://user-images.githubusercontent.com/48850794/97297491-215fca00-1878-11eb-86f7-3f6c9374b924.png)

#### Application Binary Interface

RISC-V architecture has 32 registers. Application programmer, can access each of these 32 registers through its ABI name,
for example, you need know the value of stack pointer or move the stack pointer, all you need to do is “addi sp, sp, -16”,
where ‘sp’ is the ABI name of stack pointer.

![32-registers](https://user-images.githubusercontent.com/48850794/97298238-28d3a300-1879-11eb-9c24-6e7b40c1c2ac.png)

## Day - 3 : Digital Logic with TL-Verilog and Makerchip

Transaction-Level Verilog (TL-Verilog) is an emerging extension to SystemVerilog that supports transaction-level design methodology.
In transaction-level design, a ​transaction is an entity that moves through a microarchitecture. 


Check the folders for assignments for particular days.
