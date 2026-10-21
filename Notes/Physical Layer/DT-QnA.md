## ```Q1\. [2023 General SEC-A-1 - Q7(a)]``` What is line coding? What is unipolar encoding? [1 + 1 = 2 Marks]

- **Line Coding:** The process of converting digital binary data (a sequence of $0\text{s}$ and $1\text{s}$) into a digital signal with defined voltage levels for transmission over a physical channel.
- **Unipolar Encoding:** A line coding scheme where all signal voltage levels exist on one side of the time axis (e.g., positive voltage $+V$ for binary 1, and zero voltage $0\text{ V}$ for binary 0).


## ``` **Q2\. [2021 Honours Paper V - Q9(b)]``` Write down some characteristics of Line coding. [4 Marks]
1. Signal Rate vs. Data Rate: Line codes strive to minimize the signal rate ($S$) for a given data rate ($N$) to conserve bandwidth.
2. DC Component Elimination: High-quality line codes eliminate zero-frequency (DC) energy concentrations, allowing signals to pass through transformer-coupled or band-limited media.
3. Baseline Wandering Prevention: Prevents drifting of the receiver's evaluation threshold during long runs of identical bits.
4. Self-Synchronization: Incorporates built-in voltage transitions within each bit interval so the receiver clock stays synchronized with the sender.


## ```Q3\. [2022 General SEC-A-X-I - Q6(b)]``` Differentiate between NRZ and RZ line coding with examples. [3 Marks]

Feature | NRZ (Non-Return-to-Zero) | RZ (Return-to-Zero)
---|---|---
Voltage Level | Signal voltage stays constant throughout the entire bit duration | Signal returns to $0\text{ V}$ at the midpoint ($T_b/2$) of every bit duration
Voltage Levels Used | 2 levels ($+V, -V$ or $+V, 0$) | 3 levels ($+V, 0, -V$)
Synchronization | Lacks self-synchronization during long strings of $0\text{s}$ or $1\text{s}$ | Fully self-synchronizing due to mid-bit return to zero
Bandwidth Requirement | Lower bandwidth ($B_{\min} = N/2$) | Double bandwidth requirement ($B_{\min} = N$)

## ```Q4\. [2022 Honours CC-8 - Q8(b)] / [2023 General SEC-A-1 - Q7(b)]``` How does Manchester encoding differ from differential Manchester encoding? Describe Manchester encoding and differential Manchester encoding with suitable examples. [2 Marks / 6 Marks]

- **Manchester Encoding:**
    - Rule:  Combines RZ and NRZ-L311. Every bit interval has a midpoint transition311. A High-to-Low transition represents binary 0, while a Low-to-High transition represents binary 1311.
    - Example: For binary 0, signal goes $+V \to -V$. For binary 1, signal goes $-V \to +V$.
    
- **Differential Manchester Encoding:**
    - Rule: Combines RZ and NRZ-I311. A midpoint transition always occurs for clock synchronization311. The presence or absence of a transition at the beginning of the bit interval determines the bit value311:
        - Transition at start = Binary 0
        - No transition at start = Binary 1
- **Key Difference:** Manchester depends on the absolute direction of the mid-bit transition (susceptible to wire reversal), whereas Differential Manchester depends on the relative presence/absence of a transition at the start of the bit (polarity-insensitive).

## ```Q5\. [2022 General SEC-A-X-I - Q7(a)]``` What is the advantage of using Manchester line coding? [2 Marks]
1. **Complete Self-Synchronization**: The mid-bit transition in every bit interval acts as a clocking signal, preventing clock synchronization loss during long sequences of 0s or 1s.
2. **Zero DC Component**: Equal positive and negative voltage durations per bit eliminate DC energy build-up.

## ```Q6\. [2022 General SEC-A-I - Q5(a)]``` Encode the string 01001110 in NRZ-L and Differential Manchester encoding scheme. Clearly mention the conventions. [4 Marks]

- **Conventions:**
    - **NRZ-L:** Positive Voltage ($+V$) = 0, Negative Voltage ($-V$) = 1.
    - **Differential Manchester:** Mid-bit transition always present. Transition at start of bit = 0, No transition at start = 1. Assume initial signal level before first bit is Low ($-V$).

    [diagram for NRZ-L and Differential Manchester encoding of 01001110]

## ```Q7\. [2021 Honours Paper V - Q10(c)]``` Encode the following streams of bits using RZ line coding scheme: **0100011100001110**. [4 Marks]

- Convention for Polar RZ:
    - Bit 1: $+V$ for first half of bit, drops to $0\text{ V}$ for second half.
    - Bit 0: $-V$ for first half of bit, rises to $0\text{ V}$ for second half.

    [diagram for Polar RZ encoding of 0100011100001110]


## ```Q10\. [2021 General Paper-IV - Q1(b)]``` What is parallel transmission mode? [2 Marks]

**Parallel Transmission:** A data transmission mode where $n$ bits of a data group (e.g., an 8-bit byte) are sent simultaneously across $n$ separate physical wires or channels with each clock tick.

**Advantage:** Higher data transfer rate compared to serial transmission.

**Disadvantage:** Requires more physical wires and is prone to signal skew over long distances.

## ```Q11\. [2021 Honours CC-8 - Q4(d)]``` Among serial and parallel transmission which one is faster? Explain briefly with reasons. [3 Marks]

- **Parallel transmission** is theoretically faster because it transmits multiple bits concurrently across separate physical lines per clock cycle.

**Reasons & Constraints:**
- **Multifold Data Transfer:** Sending $n$ bits in parallel achieves $n$ times the throughput of a single serial line at the same clock frequency.
- **Distance Limit:** At high clock speeds over longer distances, wire skew (differing arrival delays across physical conductors) desynchronizes the arrival of parallel bits, making parallel transmission impractical over long distances compared to high-speed serial links.