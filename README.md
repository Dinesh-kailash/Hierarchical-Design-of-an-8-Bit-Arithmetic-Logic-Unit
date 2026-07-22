# 8-Bit Arithmetic Logic Unit (ALU) Using Digital Logic and Verilog HDL

## Overview

This project implements an **8-bit Arithmetic Logic Unit (ALU)** using Digital Logic and Verilog HDL. The ALU is designed using a **hierarchical modular approach**, where individual modules are developed and integrated to perform arithmetic, logical, and shift operations.

The project demonstrates fundamental concepts of digital electronics, combinational logic design, modular circuit implementation, and hardware description using Verilog.

---

## Features

- 8-bit Addition
- 8-bit Subtraction (Two's Complement Method)
- Bitwise AND
- Bitwise OR
- Bitwise XOR
- Left Shift Operation
- Right Shift Operation
- Hierarchical Modular Design
- Verilog HDL Implementation

---

## Project Architecture

The ALU is constructed using the following modules:

```
                    +----------------------+
                    |      8-Bit ALU       |
                    +----------+-----------+
                               |
      -------------------------------------------------
      |                 |                |            |
 Arithmetic Unit   Logic Unit      Shift Unit    Control Logic
      |                 |                |
      |                 |                |
 Add/Subtractor    AND OR XOR      Left/Right Shift
      |
8-Bit Ripple Carry Adder
      |
1-Bit Full Adder
```

---

## Modules

### 1. 1-Bit Full Adder

The Full Adder is the fundamental building block of the arithmetic unit.

### Inputs

- A
- B
- Carry In (Cin)

### Outputs

- Sum
- Carry Out

### Logic Equations

**Sum**

```
A ⊕ B ⊕ Cin
```

**Carry**

```
AB + Cin(A ⊕ B)
```

---

### 2. 8-Bit Ripple Carry Adder

Eight Full Adders are cascaded together to form an 8-bit Ripple Carry Adder.

Features

- 8-bit Addition
- Carry Propagation
- Carry Out Generation

---

### 3. Add/Subtract Unit

Subtraction is implemented using the Two's Complement technique.

```
A - B

= A + (~B + 1)
```

A MODE signal controls the operation.

| MODE | Operation |
|------|-----------|
| 0 | Addition |
| 1 | Subtraction |

---

### 4. Logic Unit

The Logic Block performs basic bitwise operations.

Supported Operations

- AND
- OR
- XOR

---

### 5. Shift Unit

The Shift Block performs

- Logical Left Shift
- Logical Right Shift

---

### 6. Top-Level ALU

The top-level ALU integrates

- Arithmetic Unit
- Logic Unit
- Shift Unit

A multiplexer selects the required output based on the operation select lines.

---

## Supported Operations

| Operation | Description |
|------------|-------------|
| Addition | A + B |
| Subtraction | A - B |
| AND | A AND B |
| OR | A OR B |
| XOR | A XOR B |
| Left Shift | A << 1 |
| Right Shift | A >> 1 |

---

## Project Structure

```
8-bit-ALU/
│
├── README.md
├── LICENSE
│
├── DigSim/
│   ├── 8_BIT_ADDER.dig
│   ├── FULL_ADDSUB.dig
│   ├── LOGIC_BLOCK.dig
│   ├── SHIFTFUN.dig
│   └── ALU.dig
│
├── Verilog/
│   └── ALU.v
│
├── Images/
│   ├── full_adder.png
│   ├── adder_8bit.png
│   ├── add_subtractor.png
│   ├── logic_block.png
│   ├── shift_unit.png
│   └── full_alu.png
│
└── Documentation/
    └── Project_Report.pdf
```

---

## Tools Used

- Digital Logic Simulator (.dig)
- Verilog HDL
- Git
- GitHub

---

## Prerequisites

Before running this project, ensure the following software is installed:

| Software | Purpose | Download |
|----------|---------|----------|
| Digital Logic Simulator | Open and simulate the `.dig` circuit files | https://github.com/hneemann/Digital/releases |
| Java Runtime Environment (JRE 8+) | Required to run Digital | https://adoptium.net/ |
| Icarus Verilog *(Optional)* | Compile and simulate the Verilog implementation | https://github.com/steveicarus/iverilog |
| GTKWave *(Optional)* | View Verilog simulation waveforms | https://gtkwave.sourceforge.net/ |

---

## Installation & Setup

1. Download this repository as a ZIP file or clone it.
2. Install **Digital Logic Simulator** from the official release page.
3. Install **Java Runtime Environment (JRE 8 or later)** if it is not already installed.
4. Launch **Digital Logic Simulator**.
5. Open the `DigSim` folder.
6. Open `ALU.dig` to load the complete 8-bit ALU design.
7. Explore the remaining `.dig` files to view individual modules.

---

## How to Run

1. Open `ALU.dig` in the Digital Logic Simulator.
2. Modify the input values using the input switches.
3. Observe the outputs for arithmetic, logical, and shift operations.
4. To understand the design hierarchy, open the individual module files located in the `DigSim` folder.

> **Note:** The Verilog implementation (`ALU.v`) is provided as an additional hardware description of the design and can be simulated using Icarus Verilog if desired.

---

## Applications

- Computer Architecture
- Processor Design
- Embedded Systems
- FPGA Development
- Digital System Design
- Digital Electronics Laboratory
- Educational Projects

---

## Learning Outcomes

This project demonstrates understanding of

- Boolean Algebra
- Combinational Logic Design
- Hierarchical Circuit Design
- Ripple Carry Addition
- Two's Complement Arithmetic
- Bitwise Logic Operations
- Shift Operations
- Multiplexer-Based Selection
- Hardware Description Language (Verilog)

---

## Future Improvements

- Carry Lookahead Adder
- Overflow Detection
- Zero Flag
- Sign Flag
- Negative Flag
- Barrel Shifter
- 16-bit ALU
- 32-bit ALU
- FPGA Implementation
- Comprehensive Testbench
- Timing Analysis

---

## Screenshots

### 1-Bit Full Adder

> Add image here

```
Images/full_adder.png
```

### 8-Bit Ripple Carry Adder

> Add image here

```
Images/adder_8bit.png
```

### Add/Subtractor

> Add image here

```
Images/add_subtractor.png
```

### Logic Block

> Add image here

```
Images/logic_block.png
```

### Shift Unit

> Add image here

```
Images/shift_unit.png
```

### Complete ALU

> Add image here

```
Images/full_alu.png
```

---

## Repository Topics

```
digital-logic
verilog
alu
digital-design
computer-architecture
fpga
electronics
combinational-logic
ripple-carry-adder
embedded-systems
```

---

## Author

**Dinesh Kailash**

B.E. Electrical and Electronics Engineering

GitHub: https://github.com/kumareshan3010

---

## License

This project is licensed under the MIT License.
