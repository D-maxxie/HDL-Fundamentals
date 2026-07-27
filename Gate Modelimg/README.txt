# Logic Gates Using Gate-Level Modeling in Verilog

## Overview

This project implements the basic digital logic gates using Verilog HDL through **gate-level modeling**. Instead of using behavioral code or continuous assignment statements, the design directly instantiates Verilog's built-in logic gate primitives. This approach closely represents how digital circuits are constructed at the hardware level and is useful for understanding the fundamentals of digital design.

## Features

- Implements seven basic logic gates using gate primitives
- Uses built-in Verilog gate instantiations
- Pure combinational logic with no clock dependency
- Simple and easy-to-understand implementation
- Suitable for FPGA and ASIC design fundamentals

## Logic Gates Implemented

- AND
- OR
- NOT
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

## How It Works

The module uses Verilog's built-in gate primitives to implement each logic function. Each gate is instantiated by specifying the output signal first, followed by the input signals.

For example:

- `and` generates the logical AND of `a` and `b`
- `or` generates the logical OR
- `not` inverts input `a`
- `nand`, `nor`, `xor`, and `xnor` produce their respective logic outputs

Since gate primitives continuously respond to input changes, the circuit behaves as a combinational logic circuit without requiring an `always` block or `assign` statements.

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
- Any Verilog simulator such as ModelSim, Vivado Simulator, or Icarus Verilog

## Applications

- Learning gate-level modeling in Verilog
- Digital electronics and logic design courses
- FPGA and ASIC design practice
- Understanding hardware implementation of logic circuits

## Future Improvements

- Develop a testbench to verify all possible input combinations.
- Expand the design to support multi-bit logic operations.
- Compare this gate-level implementation with dataflow and behavioral modeling approaches.

## Author

**Dileep Kumar Maddineni**