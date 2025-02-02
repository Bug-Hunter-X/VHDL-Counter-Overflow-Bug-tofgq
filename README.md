# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an unhandled counter overflow.  The `counter.vhdl` file contains a simple counter that increments on each rising clock edge. However, it doesn't account for what happens when the counter reaches its maximum value ("1111").  This can lead to unpredictable behavior.

The `counter_fixed.vhdl` file provides a corrected version that addresses this issue.

## Bug Description
The original counter lacks a mechanism to prevent overflow. Once the counter reaches its maximum value, the next increment will wrap around to "0000", potentially causing incorrect functionality in a larger design.

## Solution
The solution involves adding a check to detect when the counter reaches its maximum value and then either stopping the count or resetting it.