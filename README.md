# VHDL Counter Overflow Bug
This repository demonstrates a common error in VHDL: counter overflow.  The provided VHDL code implements a simple counter, but lacks proper handling for when the counter reaches its maximum value. This can lead to unexpected behavior and simulation failures.

## Bug Description
The `counter` entity increments `internal_count` without checking for overflow. When `internal_count` reaches 15, the next increment results in a value of 16, which is outside the defined range (0 to 15).  This can cause unpredictable results, including silent errors.

## Solution
The solution demonstrates how to correctly handle counter overflow.  It incorporates a modulo operator to ensure the counter wraps around to 0 after reaching its maximum value.