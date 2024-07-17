# 32-bit IEEE 754 Floating Point Multiplier

This project implements a 32-bit floating point multiplier following the IEEE 754 standard in Verilog.

## Overview

The IEEE 754 standard defines the format and methods for floating-point arithmetic in computer systems. This multiplier operates on 32-bit single-precision floating-point numbers, providing accurate and standardized multiplication results.

[![The-proposed-architecture-for-32-bit-Floating-point-multiplier.png](https://i.postimg.cc/yNzBYQtB/The-proposed-architecture-for-32-bit-Floating-point-multiplier.png)](https://postimg.cc/Yv8Td3ty)

## Features

- Multiplies two 32-bit floating-point numbers
- Complies with IEEE 754 single-precision format
- Handles special cases (NaN, infinity, zero)
- Implements proper rounding
- Detects overflow and underflow conditions
- Flags exceptions

## Circuit Structure

[![Architecture-of-32-bit-Single-Precision-Floating-Point-Multiplier.png](https://i.postimg.cc/1Xzy18Tq/Architecture-of-32-bit-Single-Precision-Floating-Point-Multiplier.png)](https://postimg.cc/qhWP8vpJ)

The multiplier consists of the following main components:

1. Sign calculation
2. Exponent addition
3. Mantissa multiplication
4. Normalization
5. Rounding
6. Exception handling

[Insert here: Individual circuit diagrams or logic schematics for each of the above components]

## Module Structure

The project consists of two main modules:

1. `Multiplication`: The core multiplier module
2. `multiplication_tb`: A testbench for verifying the multiplier's functionality

### Multiplication Module

[Insert here: A diagram showing the inputs and outputs of the Multiplication module]

The `Multiplication` module takes two 32-bit inputs (`a` and `b`) and produces a 32-bit output (`res`). It also outputs flags for exception, overflow, and underflow.

### Testbench

The `multiplication_tb` module provides a comprehensive test suite for the multiplier. It includes various test cases covering normal operations, edge cases, and special values.

[Insert here: A flowchart or diagram illustrating the testbench process]

## Usage

To use the multiplier in your project:

1. Include the `Multiplication` module in your Verilog project.
2. Instantiate the module with appropriate input and output connections.

Example:
```verilog
Multiplication mult_instance(
    .a(input_a),
    .b(input_b),
    .exception(exception_flag),
    .overflow(overflow_flag),
    .underflow(underflow_flag),
    .res(result)
);
