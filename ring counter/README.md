# Ring Counter Using Verilog HDL

## 1. Introduction

A Ring Counter is a type of shift register in which the output of the last flip-flop is connected back to the input of the first flip-flop.

This project implements a **4-bit Ring Counter using Verilog HDL**.

## 2. Objectives

* To design a 4-bit Ring Counter.
* To implement the design using Verilog HDL.
* To create a testbench for verification.
* To simulate the counter and observe its output waveform.

## 3. Working Principle

A 4-bit Ring Counter contains four flip-flops.

Initially, one flip-flop is set to `1` and all other flip-flops are set to `0`.

The `1` circulates through the flip-flops with every clock pulse.

The output sequence is:

```text
1000
0100
0010
0001
1000
```

Therefore, a 4-bit Ring Counter has **4 unique states**.

## 4. State Sequence

| Clock Cycle | Output |
| ----------: | :----: |
|           0 |  1000  |
|           1 |  0100  |
|           2 |  0010  |
|           3 |  0001  |
|           4 |  1000  |

## 5. Inputs and Outputs

| Signal | Direction | Description          |
| ------ | --------- | -------------------- |
| clk    | Input     | Clock signal         |
| reset  | Input     | Reset signal         |
| q[3:0] | Output    | 4-bit counter output |

## 6. Applications

* Sequence generation
* Timing circuits
* Digital control circuits
* Frequency division
* Counter circuits
* Digital systems

## 7. Tools Required

* Verilog HDL
* Icarus Verilog
* GTKWave
* GitHub

## 8. Project Files

### Source Code

`src/ring_counter.v`

Contains the Verilog implementation of the 4-bit Ring Counter.

### Testbench

`testbench/ring_counter_tb.v`

Used to verify the operation of the Ring Counter.

### Simulation

`simulation/simulation_results.md`

Contains the expected simulation results.

## 9. Expected Result

The output should continuously circulate the logic `1`:

```text
1000 → 0100 → 0010 → 0001 → 1000
```

## 10. Conclusion

A 4-bit Ring Counter was successfully designed and implemented using Verilog HDL. The testbench verifies the counter operation, and simulation confirms the correct circulation of the logic `1`.
