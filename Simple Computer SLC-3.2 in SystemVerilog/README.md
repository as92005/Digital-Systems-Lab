# Simple Computer SLC-3.2 in SystemVerilog
[Full Project Report](Lab5.pdf)

Overview:-
The SLC-3.2 is a simplified LC-3 processor implemented on FPGA. It executes a fetch-decode-execute cycle, performs arithmetic and logic operations, handles memory-mapped I/O, and provides visual cues using LEDs and hex displays. It is designed for educational purposes to understand processor architecture, control logic, and hardware-software interaction.

Function:-
- Executes instructions: ADD, ADDi, AND, ANDi, NOT, BR, JMP, JSR, LDR, STR, PAUSE.
- Handles memory-mapped I/O for switches and hex displays.
- Provides visual feedback using LEDs for program progress.
- Implements a multi-cycle fetch-decode-execute cycle.


Key Subcircuits:-
- CPU Core: ALU, PC, IR, MAR, MDR, control unit.
- ALU: Performs arithmetic and logic operations.
- Register File: 8 general-purpose 16-bit registers.
- Instruction Sequencer/Decoder: Controls instruction timing and ALU operation.
- Memory Interface: Manages on-chip RAM read/write operations.
- CPU-to-IO Module: Handles communication with switches and hex displays.
- Top-Level Circuit: Integrates CPU, memory, I/O, and display drivers.
