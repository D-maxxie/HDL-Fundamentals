# Logic Gates Using Continuous Assignment in Verilog

## Overview

This project demonstrates the implementation of basic digital logic gates using Verilog HDL with continuous assignment (`assign`) statements. The module accepts two single-bit inputs and produces the outputs of seven fundamental logic operations. Since the design uses continuous assignments, the outputs update automatically whenever the inputs change, making it a simple example of combinational logic.

## Features

- Implements seven basic logic gates
- Uses continuous `assign` statements instead of an `always` block
- Simple combinational logic design
- Suitable for beginners learning Verilog HDL
- Easy to simulate and synthesize on FPGA platforms

## Logic Gates Implemented

- AND
- OR
- NOT (Input `a`)
- NAND
- NOR
- XOR
- XNOR

## Inputs

| Signal | Description |
|--------|-------------|
| `a` | First input (1-bit) |
| `b` | Second input (1-bit) |

## Outputs

| Signal | Description |
|--------|-------------|
| `and_g` | AND gate output |
| `or_g` | OR gate output |
| `not_g` | NOT gate output of input `a` |
| `nand_g` | NAND gate output |
| `nor_g` | NOR gate output |
| `xor_g` | XOR gate output |
| `xnor_g` | XNOR gate output |

## Working

The design uses Verilog's `assign` statement to implement each logic gate. Continuous assignments continuously evaluate the expressions on the right-hand side and automatically update the outputs whenever an input changes. Because there is no clock or sequential logic involved, the module behaves as a purely combinational circuit.

## Project File

```
logic_gates.v
```

## Example Truth Table

| A | B | AND | OR | NOT(A) | NAND | NOR | XOR | XNOR |
|---|---|-----|----|--------|------|-----|-----|------|
| 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 |

## Requirements

- Verilog HDL
- Any Verilog simulator (ModelSim, Vivado Simulator, Icarus Verilog, etc.)

## Applications

- Digital logic fundamentals
- Verilog HDL learning
- FPGA and ASIC design practice
- Academic laboratory experiments

## Future Improvements

- Create a testbench to verify all input combinations.
- Extend the module to support multi-bit buses.
- Compare this implementation with an `always @(*)` block version to understand different coding styles.

## Author

**Dileep Kumar Maddineni**