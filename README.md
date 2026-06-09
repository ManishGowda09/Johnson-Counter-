# Johnson-Counter-
A hardware implementation of a **4-bit Johnson Counter** (also known as a twisted ring counter) written in Verilog HDL. This repository includes both the synthesizable design module and a comprehensive testbench for simulation.

## Features
* **Asynchronous Reset:** Safely forces the counter back to its initial state (`4'b0000`).
* **Efficient Decoding:** Generates a sequence of 8 unique states using only 4 flip-flops without requiring heavy decoding logic.
* **Glitch-Free Output:** Only one bit changes at a time between consecutive states (similar to Gray code characteristics), minimizing output glitches.

---
## How It Works

A Johnson counter is variation of a standard ring shift register where the inverted output of the last flip-flop ($\sim Q_0$) is fed back into the input of the first flip-flop ($D_3$). 

### Counting Sequence
When clock pulses are applied, the counter cycles through the following **8 states**:
$$\text{0000} \rightarrow \text{1000} \rightarrow \text{1100} \rightarrow \text{1110} \rightarrow \text{1111} \rightarrow \text{0111} \rightarrow \text{0011} \rightarrow \text{0001} \rightarrow \text{0000}$$

---
# Waveform
<img width="1907" height="391" alt="image" src="https://github.com/user-attachments/assets/967cab67-a093-4cb1-96ac-20a0dd2942d4" />
