# Custom 16-Bit CPU Design

A custom 16-bit processor architecture designed, modeled, and simulated in the **Digital** logic simulator.

## Key Architecture Features
- **16-Bit Datapath**: All registers, buses, and memory address spaces operate on 16-bit values.
- **Modular ALU (Arithmetic Logic Unit)**:
  - **ADDER**: Custom-built adders including a 1-bit full adder and multi-bit Ripple Carry Adders.
  - **COMPARATOR**: Unsigned comparator module for logical comparisons.
  - **DIVIDER**: Custom logic for division.
  - **MULTIPLIER**: Logic design implementing unsigned multiplication.
  - **SHIFTER**: Supports left/right shifting and barrel shifting logic.
  - **LOGIC CORE**: Logic gates logic unit.
- **Storage Subsystem**:
  - **Register File (`REG V1`)**: High-speed register files for temporary variables.
  - **Instruction Memory**: Dedicated memory storage block for instructions.
  - **Data Memory**: RAM layout for reading/writing parameters.
- **Control Path**: Selectors, multiplexers (up to 16x1 16-bit configurations), and decoders (up to 4x16 configurations) coordinate signals and direct data flow.

## ISA (Instruction Set Architecture)
The CPU supports a custom instruction set specifically tailored for logic processing. Detailed micro-operations and instruction formats are cataloged in `INSTRUCTION SET/full_instruction_set_final.pdf`.

## Software & Simulation Environment
- The CPU schematics and simulator files (`.dig` extension) require Helmut Neemann's **Digital** logic simulator.
- You can download the simulator from: [Helmut Neemann - Digital](https://github.com/hneemann/Digital).

## Opening the Design Files
1. Open the **Digital** logic simulator.
2. Select **File -> Open** and navigate to `processor/MAIN PROC.dig` to view the full system schematic.
3. Open individual sub-circuits (e.g. `processor/ALU/MAIN ALU.dig` or `processor/STOREGE/REGISTER/REG V1.dig`) to analyze the custom block layouts.\n