# Unhandled Overflow in VHDL Counter

This repository demonstrates a common error in VHDL: an integer counter without an overflow check.  The `buggy_counter.vhdl` file contains a VHDL counter that increments without bound.  This can lead to unexpected simulation results or even hardware malfunctions if implemented in an FPGA.

The `fixed_counter.vhdl` file provides a corrected version with an overflow check, ensuring the counter behaves as expected.

## How to Reproduce

1. Simulate `buggy_counter.vhdl` using your preferred VHDL simulator (e.g., ModelSim, GHDL, etc.).
2. Observe the counter's behavior after it exceeds the maximum value for an integer in your simulator.
3. Simulate `fixed_counter.vhdl` and compare the results.

## Solution

The solution involves adding a check to ensure that the counter does not exceed its intended range. The fixed version uses a modulo operation to prevent overflow.