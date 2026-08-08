# Simulation Results

## Simulation Tools

The Ring Counter was simulated using:

* Icarus Verilog
* GTKWave

## Input Conditions

The counter is first reset to:

```text
1000
```

After reset is released, the counter shifts the logic `1` on every positive clock edge.

## Expected Output

| Clock Cycle | Q[3:0] |
| ----------: | :----: |
|       Reset |  1000  |
|           1 |  0100  |
|           2 |  0010  |
|           3 |  0001  |
|           4 |  1000  |
|           5 |  0100  |
|           6 |  0010  |
|           7 |  0001  |

## Result

The simulation shows that the logic `1` circulates through all four flip-flop positions correctly.

The Ring Counter produces the sequence:

```text
1000 → 0100 → 0010 → 0001 → 1000
```

## Conclusion

The 4-bit Ring Counter was successfully designed, tested, and simulated using Verilog HDL.
