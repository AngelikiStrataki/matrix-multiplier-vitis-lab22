# matrix-multiplier-vitis-lab22
# Matrix Multiplier – Vitis FPGA Acceleration (Lab 2)

## Overview
This project uses **Xilinx Vitis** to accelerate matrix multiplication on an FPGA. The implementation builds on the Lab 1 HLS kernel and integrates it into a Vitis-based design using OpenCL. It supports both software and hardware emulation, as well as deployment on real FPGA hardware.

> 📘 **Note:** The lab report and project presentation are written in Greek.

## Contents
- `vadd.txt`: The HLS kernel for matrix multiplication using local buffers and parallel loops.
- `host_2.txt`: Host application in C++ using OpenCL to manage data transfer and kernel execution.
- `report lab 2.pdf`: Lab report with design explanation, Vitis steps, and emulation results (in Greek).
- `team_2B_lab_2.zip`: Full Vitis workspace with source files.

## How to Run
1. Open **Vitis IDE** and create a new platform + application project.
2. Import the `vadd` kernel and the host code from `host_2.txt`.
3. Compile and run:
   - Software Emulation
   - Hardware Emulation
   - Hardware Run (with Alveo board or other FPGA if available)
4. Check that hardware output matches software reference results.

## Key Optimizations
- Local buffers for storing input and output matrices.
- `#pragma HLS ARRAY_PARTITION` to improve access parallelism.
- `#pragma HLS UNROLL` for loop parallelization.
- AXI interfaces for efficient memory access:
  - `m_axi` for matrix data.
  - `s_axilite` for control signals.

## Authors
- Dimitrios Orestis Vagenas (10595)
- Angeliki Strataki (10523)
