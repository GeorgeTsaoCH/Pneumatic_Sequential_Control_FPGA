# Pneumatic Sequential Control → FPGA FSM
Mapping a pneumatic sequential control sequence into a digital Finite State Machine (FSM) implemented in Verilog on a Basys3 FPGA.

## Overview
This project maps a pneumatic sequential control sequence into a digital Finite State Machine (FSM) implemented on an FPGA.

**Platform:** Basys3  
**HDL:** Verilog  
**Tool:** Vivado

## Pneumatic Sequence (Example)
A+ → B+ → A- → B-

## FSM Design
### States
- S0: IDLE
- S1: A_EXTEND
- S2: B_EXTEND
- S3: A_RETRACT
- S4: B_RETRACT

### Inputs (Sensors)
- start
- A_ext_limit, A_ret_limit
- B_ext_limit, B_ret_limit

### Outputs (Valve Commands)
- A_extend, A_retract
- B_extend, B_retract

## Repository Structure
src/   : Verilog source files (fsm, top)  
tb/    : Testbench files  
docs/  : Diagrams (FSM state diagram, pneumatic system)

## Development Roadmap
- [ ] Draw pneumatic diagram and FSM state diagram
- [ ] Implement FSM in Verilog
- [ ] Write testbench and simulate waveforms
- [ ] Map inputs/outputs to Basys3 switches/LEDs
- [ ] Add results and photos
