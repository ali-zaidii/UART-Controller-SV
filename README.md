# UART-Controller-SV
## Project Overview

This project implements a Universal Asynchronous Receiver Transmitter (UART) using SystemVerilog, including both transmitter (TX) and receiver (RX) modules, a baud rate generator, and a self-checking testbench.
The design follows a modular RTL approach and is verified through simulation using a layered testbench architecture.

UART is a widely used serial communication protocol in embedded systems, microcontrollers, and FPGA-based designs, making this project highly relevant for digital design and verification roles.

## Key Features

Fully synthesizable UART TX and RX modules

Configurable baud rate generator

Clean top-level UART integration

SystemVerilog-based testbench

Organized and modular RTL design

Suitable for FPGA implementation and simulation-based verification

## Project Architecture

The design is divided into the following major blocks:

1. Baud Rate Generator

Generates baud tick based on system clock

Used by both transmitter and receiver for synchronization

2. UART Transmitter (TX)

Serializes parallel data

Adds start bit, stop bit

Transmits data according to baud rate

3. UART Receiver (RX)

Detects start bit

Samples incoming serial data

Reconstructs parallel data

4. UART Top Module

Integrates TX, RX, and baud generator

Provides a clean interface for external communication

5. Testbench

Verifies end-to-end UART communication

Generates stimulus and checks output behavior

Ensures correct timing and data integrity

## File Structure
├── baud_gen.sv          # Baud rate generator
├── uart_tx.sv           # UART transmitter
├── uart_rx.sv           # UART receiver
├── uart_top.sv          # Top-level UART module
├── uart_tb.sv           # UART testbench
├── uart_tb_package.sv   # Testbench package (parameters/utilities)
├── UART.mpf              # Simulation project file

## Tools & Technologies

Language: SystemVerilog

Simulation: ModelSim / QuestaSim

Design Style: RTL, Modular

Verification: Simulation-based testbench

## How to Run the Simulation

Open ModelSim / QuestaSim
Load the project file:

UART.mpf

Compile all SystemVerilog files
Run the simulation:
run -all
Observe UART TX/RX waveforms and console outputs

## Verification Highlights

Correct baud rate timing verification
Accurate serial-to-parallel and parallel-to-serial conversion
Start and stop bit validation
End-to-end UART data transmission testing

## Learning Outcomes

Hands-on experience with UART protocol
Practical understanding of serial communication
Writing clean and synthesizable SystemVerilog RTL
Building and using testbenches for verification
Strengthened FPGA and digital design fundamentals

## Future Improvements

Parameterized data width and stop bits
Parity bit support
Coverage-driven verification
FPGA hardware testing
AXI-stream or FIFO-based UART interface

## Author
Syed Ali Raza Zaidi
Digital Design & Verification Enthusiast
SystemVerilog | FPGA | RTL Design
