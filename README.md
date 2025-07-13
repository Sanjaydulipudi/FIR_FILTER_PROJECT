FIR Filter (64-Tap) Project using Verilog HDL

Hello! 🙏  
This repository contains my Summer Internship project: a "64-Tap Finite Impulse Response (FIR) Filter", designed fully using Verilog HDL and simulated in *Xilinx Vivado 2025.1*.

📌 About the Project

This project implements a *low-pass FIR filter* with fixed symmetric coefficients (Q1.15 format). The main objective is to filter out high-frequency noise from real-world signals like voice, audio, or biomedical data.
It follows a *shift-register + multiply + accumulate* architecture and supports up to 64 input samples.

 🧠 My Learnings

I completed this during my *MeitY C2S Internship* on VLSI Design at VR Siddhartha Engineering College, and I also had exposure to tools like Synopsys Design Compiler, ICC2, and Verdi, along with MATLAB Simulink (Model Composer). But here, everything is fully built using *pure Verilog*, line by line.

 ⚙️ Modules Included

All modules were handwritten and tested in simulation:

| Module         | Description                                      |
|----------------|--------------------------------------------------|
| `fir_filter.v` | Top FIR filter module with 64 taps               |
| `dff_16bit.v`  | 16-bit D flip-flop for input shift registers     |
| `mul_16bit.v`  | 16-bit signed multiplier (partial product style) |
| `rca_32bit.v`  | 32-bit Ripple Carry Adder used for accumulation  |
| `tb_fir_filter.v` | Full testbench with simulation results         |

All internal signals and arithmetic operations are *signed* to support both positive and negative data.

📁 Folder Structure

fir-filter-verilog/
├── src/
│   ├── fir_filter.v
│   ├── dff_16bit.v
│   ├── mul_16bit.v
│   ├── rca_32bit.v
├── sim/
│   └── tb_fir_filter.v
├── docs/
│   ├── waveform.jpg
│   ├── fir_structure.jpg
│   ├── output_table.txt
├── README.md
