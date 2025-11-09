4-Bit Serial Logic Processor

Overview:
- Designed and implemented a 4-bit serial logic processor capable of performing eight logic operations (AND, OR, XOR, NAND, NOR, XNOR, SET, CLR) and routing results back into registers based on user input. Built first on a breadboard using TTL components, then extended to an 8-bit SystemVerilog version on an FPGA using Vivado and vSim.

How It Works:-
- The processor operates on two 4-bit registers (RegA and RegB) that store input values provided through switches.
- A finite state machine (FSM)–based control unit manages loading, execution, and shifting cycles.
- When the Execute signal is activated, the processor performs the selected bitwise logical operation on the register contents one bit at a time (bit-serial). The result is routed back to one or both registers according to user-selected routing controls.
- LEDs display the current contents of both registers, allowing visual verification of the logic operations.

Key Subcircuits:- 
- Register Unit: Two 4-bit bidirectional shift registers (CD74HC194E) store operands (RegA and RegB). They can load, hold, or right-shift values synchronously based on control signals.
- Computation Unit: Implements 8 logical functions (AND, OR, XOR, NAND, NOR, XNOR, SET, CLR) using combinational logic. Output f(A,B) represents the selected operation result.
- Routing Unit: Uses multiplexers to select how results are routed back to RegA and RegB depending on routing inputs (R1, R0).
- Control Unit (FSM): A Mealy state machine generates control signals for shifting and loading. It ensures each computation cycle executes exactly once per “Execute” signal.
- Clocking and Debugging: Clock generated via FPGA or pulse generator. LEDs used for debugging and visualization of register states.

Tools & Technologies:-
- Hardware: TTL logic (breadboard), FPGA development board
- Software: Xilinx Vivado, ModelSim/vSim
- Language: SystemVerilog
- Concepts: Finite State Machines, Bit-Serial Processing, Combinational/Sequential Logic, Hardware Debugging

Overall Circuit: 
![WhatsApp Image 2025-11-09 at 4 34 57 PM](https://github.com/user-attachments/assets/b7f5ff00-92d0-40d6-8b52-30ca2c5391f6)
