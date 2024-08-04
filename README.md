# VerySimpleCPU and Testbench

This repository contains the Verilog implementation of a simple CPU and its corresponding testbench. The CPU module performs basic operations and interacts with a block RAM (BLRAM) module. The testbench simulates the CPU's behavior and verifies its functionality.

## VerySimpleCPU

### Overview

`VerySimpleCPU` is a basic CPU design implemented in Verilog. It supports a variety of instructions including arithmetic operations, logical operations, and control flow. The CPU operates on a 14-bit addressable memory space.

### Features

- **Instructions:**
  - **ADD**: Addition operation.
  - **NAND**: NAND logical operation.
  - **SRL**: Shift Right Logical operation.
  - **LT**: Less Than comparison.
  - **MUL**: Multiplication operation.
  - **CP**: Copy data between registers.
  - **CPI**: Copy Immediate value to register.
  - **BJZ**: Branch if Zero.

- **Registers:**
  - **r1_current**: First operand.
  - **r2_current**: Second operand.

- **Memory:**
  - Addressable by a 14-bit address space.

### Usage

1. **Compile and Simulate**: Use a Verilog simulator to compile and simulate the `VerySimpleCPU` module.

2. **Instruction Set**: The CPU understands specific instructions encoded in the 32-bit instruction word.

## Testbench

### Overview

The testbench simulates the `VerySimpleCPU` and its interaction with a `blram` (Block RAM) module. It provides a clock signal, a reset signal, and initializes memory with test values.

### Features

- **Clock Generation**: Provides a clock signal toggling every 5ns.
- **Reset Logic**: Asserts the reset signal for the first 10 clock cycles.
- **Memory Initialization**: Loads initial values into the `blram` for testing.
- **Verification**: Checks the CPU's functionality by comparing expected results with actual outputs.

### Usage

1. **Compile and Simulate**: Use a Verilog simulator to compile and run the testbench.

2. **Check Results**: Verify that the CPU operates as expected and that the memory interactions are correct.

## How to Run

1. **Compile the Design**: Use your preferred Verilog compiler to compile the `VerySimpleCPU` module and testbench.
   
2. **Run Simulation**: Execute the simulation to observe the CPU behavior and verify functionality.

3. **Review Output**: Check the simulation output for correctness and make necessary adjustments to the CPU design or testbench as needed.

## Dependencies

- Verilog simulator (e.g., ModelSim, VCS, etc.)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- Thanks to the Verilog community for providing resources and support.
