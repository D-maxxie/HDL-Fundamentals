# Logic Gates using Verilog

## 📖 Overview

This project implements the seven fundamental digital logic gates using Verilog HDL. The module takes two single-bit inputs (`a` and `b`) and simultaneously generates the outputs of AND, OR, NOT, NAND, NOR, XOR, and XNOR gates.

The design is written using combinational logic (`always @(*)`) and is suitable for simulation, FPGA implementation, and digital logic learning.

---

## ✨ Features

- Implements 7 basic logic gates
- Pure combinational logic
- Single-bit input operation
- Synthesizable Verilog HDL
- Suitable for FPGA and ASIC design flows
- Beginner-friendly RTL example

---

## 📋 Specifications

| Parameter | Description |
|-----------|-------------|
| Language | Verilog HDL |
| Module Name | `logic_gates` |
| Design Type | Combinational Logic |
| Inputs | `a`, `b` |
| Outputs | `and_g`, `or_g`, `not_g`, `nand_g`, `nor_g`, `xor_g`, `xnor_g` |

---

## 🏗️ Block Diagram (Conceptual)

```
        a -----------+
                     |
                     |-----------------> AND
                     |-----------------> OR
                     |-----------------> NAND
                     |-----------------> NOR
                     |-----------------> XOR
                     |-----------------> XNOR
                     |
        b -----------+

        a -----------------------------> NOT
```

---

## ⚙️ Functional Description

The module continuously monitors inputs `a` and `b`.

- **AND Gate** → Outputs HIGH only when both inputs are HIGH.
- **OR Gate** → Outputs HIGH when at least one input is HIGH.
- **NOT Gate** → Inverts input `a`.
- **NAND Gate** → Inverted output of AND.
- **NOR Gate** → Inverted output of OR.
- **XOR Gate** → Outputs HIGH when inputs are different.
- **XNOR Gate** → Outputs HIGH when inputs are the same.

Since the module uses `always @(*)`, every output updates immediately whenever either input changes.

---

## 📊 Truth Table

| A | B | AND | OR | NOT(A) | NAND | NOR | XOR | XNOR |
|---|---|-----|----|--------|------|-----|-----|------|
| 0 | 0 | 0 | 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 |

---

## ⏱️ Timing Behavior

- Outputs change immediately whenever `a` or `b` changes.
- No clock is required.
- No sequential elements (flip-flops or latches) are used.

---

## 💡 Applications

- Digital logic education
- FPGA laboratory experiments
- Basic RTL design practice
- ASIC design fundamentals
- Logic verification
- Building larger combinational circuits

---

## ✅ Advantages

- Simple and easy to understand
- Fully synthesizable
- Minimal hardware resources
- Fast combinational response
- Reusable in larger digital systems

---

## 🧪 Simulation

### Recommended Simulators

- Xilinx Vivado Simulator
- ModelSim
- QuestaSim
- Icarus Verilog
- GTKWave (waveform viewing)

### Test Cases

| A | B | Expected Outputs |
|---|---|------------------|
|0|0|AND=0 OR=0 NOT=1 NAND=1 NOR=1 XOR=0 XNOR=1|
|0|1|AND=0 OR=1 NOT=1 NAND=1 NOR=0 XOR=1 XNOR=0|
|1|0|AND=0 OR=1 NOT=0 NAND=1 NOR=0 XOR=1 XNOR=0|
|1|1|AND=1 OR=1 NOT=0 NAND=0 NOR=0 XOR=0 XNOR=1|

---

## 🔧 Synthesis

- FPGA Compatible ✅
- ASIC Compatible ✅
- Synthesizable RTL ✅
- No inferred latches
- No clock dependency

---

## 📁 Project Structure

```
logic_gates/
│
├── rtl/
│   └── logic_gates.v
│
├── tb/
│   └── logic_gates_tb.v
│
├── docs/
│   └── logic_gates_diagram.png
│
└── README.md
```

---

## 🚀 Future Improvements

- Parameterize for multi-bit logic operations
- Add behavioral and gate-level implementations
- Create a comprehensive self-checking testbench
- Include waveform screenshots
- Add FPGA demonstration project

---

## 👨‍💻 Author

**Maddineni Dileep Kumar**
