# CMOS NOT Gate Using Transistor-Level Modeling in Verilog

## Overview

This project implements a **CMOS NOT gate (Inverter)** using transistor-level modeling in Verilog HDL. Instead of using logic operators or gate primitives, the inverter is built using one PMOS transistor and one NMOS transistor connected to the power (`VDD`) and ground (`GND`) supplies. This approach demonstrates how a basic CMOS inverter is physically implemented in digital integrated circuits.

## Features

- Transistor-level implementation of a CMOS inverter
- Uses one PMOS and one NMOS transistor
- Includes built-in power (`supply1`) and ground (`supply0`) connections
- Implements a basic NOT operation
- Suitable for learning CMOS circuit design fundamentals

## Inputs and Outputs

### Input

| Signal | Description |
|--------|-------------|
| `in` | Single-bit input signal |

### Output

| Signal | Description |
|--------|-------------|
| `out` | Inverted output of the input signal |

## How It Works

The CMOS inverter consists of two complementary MOS transistors:

- **PMOS transistor** connects the output to `VDD` when the input is logic `0`.
- **NMOS transistor** connects the output to `GND` when the input is logic `1`.

The operation is straightforward:

- If `in = 0`
  - PMOS turns ON
  - NMOS turns OFF
  - Output becomes `1`

- If `in = 1`
  - PMOS turns OFF
  - NMOS turns ON
  - Output becomes `0`

Since only one transistor conducts at a time, CMOS logic provides very low static power consumption.

## Project File

```
not_gate.v
```

## Truth Table

| Input | Output |
|------:|:------:|
| 0 | 1 |
| 1 | 0 |

## Requirements

- Verilog HDL
- A simulator that supports transistor-level primitives (such as Vivado Simulator, ModelSim, or Icarus Verilog)

## Applications

- Learning CMOS digital circuit design
- VLSI and ASIC design education
- Understanding transistor-level implementations of logic gates
- Foundation for designing more complex CMOS logic circuits

## Future Improvements

- Create a testbench to verify the inverter operation.
- Implement additional CMOS logic gates such as NAND, NOR, and XOR using transistor-level modeling.
- Perform timing and power analysis to study CMOS characteristics.

## Author

**Dileep Kumar Maddineni**