# 12-bit CPU

This README file describes the features and basic instruction set of an experimental 12-bit processor using Harvard architecture, developed and tested in Logisim simulation environment.

## General Features

* 12-bit data bus
* Harvard architecture (separate data and instruction memories)
* Single cycle operation
* 49 KB data memory
* 25 MB instruction memory

## Instruction Set
The processor has 6 basic instructions:

1. ADD (TOP) - opcode: 000
2. SUBTRACT (CIK) - opcode: 001
3. NOT AND (NND) - opcode: 010
4. LOAD (YUK) - opcode: 011
5. STORE (SAK) - opcode: 100
6. BRANCH IF EQUAL (ESD) - opcode: 101

## Instruction Format

Each instruction is 12 bits long and arranged in the following format:

```[opcode (3 bits)] [SR1 (3 bits)] [SR2/ADDR (3 bits)] [DR/ADDR (3 bits)]```

* SR1, SR2: Source registers
* DR: Destination register
* ADDR: Address field used for addressing or branching

## Development Environment

The CPU was designed and simulated using Logisim, a digital logic simulator. All circuits and components were tested in this environment to verify proper functionality.

## Special Notes

* The BRANCH IF EQUAL instruction can jump between -24 and +24 instructions from the current position
* LOAD and STORE instructions use special address calculation methods for data memory access

## Test Scenarios

The following test scenarios were implemented and verified in Logisim:

1. Addition Test
2. Subtraction Test
3. Not And Test
4. Branch If Equal Test

These tests can be used to validate the basic functionality of the processor in the simulation environment.

---

*Note: All development and testing processes were carried out using Logisim circuit simulation tool.*