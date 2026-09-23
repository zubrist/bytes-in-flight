## 1. ```[2023 General SEC-A-1 - Q1(c)] / [2023 General SEC-A-X-I - Q1(o)] / [2018 General Paper-IV - Q1(c)]``` Distinguish between a periodic signal and an aperiodic (non-periodic) signal.
> Periodic Signal: Completes a specific pattern within a measurable time frame (called a period $T$) and repeats that identical pattern over subsequent periods. Example: A simple sine wave or power line current.

> Aperiodic (Non-periodic) Signal: Changes continuously without exhibiting any repeating pattern or cycle over time. Example: A speech audio signal or computer data transmission.
---
## 2. ```[2023 General SEC-A-1 - Q1(h)]``` What is a composite signal?
- A composite signal is an electromagnetic wave made up of a combination of multiple simple sine waves having different frequencies, amplitudes, and phases. Single-frequency sine waves carry no usable data; therefore, composite signals are essential for all data communications.

---
## 3. ```[2023 General SEC-A-X-I - Q6(c)] / [2023 General SEC-A-1 - Q1(e)]``` Define bandwidth of an analog signal / medium.
The bandwidth of an analog composite signal or medium is the range of frequencies contained within it. It is calculated as the difference between its highest frequency component ($f_h$) and its lowest frequency component ($f_l$), expressed in Hertz 
($\text{Hz}$): $B = f_h - f_l$
---
## 4. ```[2022 Honours CC-8 - Q1(a)] / [2023 General SEC-A-1 - Q1(d)] / [2023 General SEC-A-X-I - Q4(c)]``` Differentiate between bit rate and baud rate / Define bit rate and baud rate

- Bit Rate ($N$): The number of data elements (bits) transmitted per second, expressed in bits per second ($\text{bps}$). 
- Baud Rate ($S$): The number of signal elements (symbols or voltage changes) transmitted per second, expressed in baud.
- Relationship: $S = N \times \frac{1}{r}$, where $r$ is the number of bits carried per signal element ($r = \log_2 L$)
---
## 5. ```[2022 General SEC-A-I - Q6(b)]``` An analog signal carries 4 bits/signal element. If 1000 signal elements are sent per second, find the bit rate.

- Solution:
    - Given $r = 4 \text{ bits/signal element}$, Signal rate $S = 1000 \text{ baud}$.
    - Using the relationship $S = N \times \frac{1}{r} \implies N = S \times r$: $$N = 1000 \text{ baud} \times 4 \text{ bits/signal element} = \mathbf{4000 \text{ bps} \text{ (or } 4 \text{ kbps)}}$$

---
## 6. ```[2023 General SEC-A-X-I - Q5(a)] / [2018 General Paper-IV - Q4(a)]``` What is the difference between analog and digital transmission? What are the advantages of digital transmission over analog transmission?

- Analog Transmission: Transmits continuous electromagnetic waves over bandpass channels where information is modulated onto carrier frequencies.
- Digital Transmission: Transmits discrete binary pulses ($0\text{s}$ and $1\text{s}$) over low-pass channels without modulating them into analog waves.
- *Advantages of Digital Transmission:*
    - **Higher Noise Immunity**: Digital signals are less susceptible to distortion and noise; receivers only need to distinguish between discrete voltage thresholds.
    - **Regenerative Repeaters**: Digital repeaters recreate brand-new clean pulses, eliminating accumulated noise over long distances, whereas analog amplifiers amplify both signal and noise.
    - **Better Data Security & Processing**: Digital data can be easily encrypted, compressed, and integrated with digital switching hardware.

    ---
## 7. ```[2021 Honours CC-8 - Q6(c)]``` A signal received has values of -1, 0, 1\. Is this an analog or a digital signal?
- Answer: It is a digital signal.
- Reason: The signal exhibits a limited, discrete set of defined voltage states (3 discrete levels: $-1$, $0$, $+1$) rather than an infinite continuum of values over time.
---

## 8. ```[2022 Honours CC-8 - Q2(a)] / [2023 General SEC-A-X-I - Q3(b)] / [2022 General SEC-A-I - Q1(l)]``` What is transmission impairment? Discuss various types of transmission impairments and mention a possible remedy for attenuation.

- **Transmission Impairment**: The degradation or corruption of a signal as it travels through a physical medium, causing the received signal to differ from the transmitted signal.
- **Three Main Types**:
    1. **Attenuation**: Loss of signal energy/power due to medium resistance.
        * *Remedy*: Use **Amplifiers** (for analog signals) or **Regenerative Repeaters** (for digital signals) placed at periodic intervals along the transmission line.
    2. **Distortion**: Alteration of a composite signal's shape caused by differing propagation speeds and delays of its constituent frequency component.
    3. **Noise**: External unwanted electrical signals (thermal, induced, crosstalk, or impulse) corrupting the data

---

## 9. ```[2022 General SEC-A-I - Q6(a)] / [2023 General SEC-A-X-I - Q9(c)] / [2021 General Paper-IV - Q3] / [2023 General SEC-A-1 - Q1(k)]``` Define Signal-to-Noise Ratio (SNR) and state its unit.

- **Signal-to-Noise Ratio (SNR)**: The ratio of average desired signal power to average unwanted noise power.
    $$\text{SNR} = \frac{\text{Average Signal Power}}{\text{Average Noise Power}}$$
- **Unit**: SNR is dimensionless as a linear ratio, but it is standardly expressed in Decibels ($\text{dB}$) using the formula $\text{SNR}_{\text{dB}} = 10 \log_{10}(\text{SNR})$.

## 10. ```[2022 General SEC-A-I - Q4(c)] / [2023 General SEC-A-1 - Q1(f)]``` Explain Nyquist theorem for a noiseless channel.

- Nyquist theorem defines the theoretical maximum bit rate for a noiseless channel: $$\text{Bit Rate} = 2 \times B \times \log_2 L$$ where $B$ is the bandwidth of the channel in Hertz ($\text{Hz}$) and $L$ is the number of discrete signal levels used to represent data.
- It proves that the maximum data rate is directly proportional to channel bandwidth and the logarithm of the number of signal levels.
---
## 11. ```[2021 Honours CC-8 - Q4(a)]``` What is Nyquist rate of sampling?
According to the Nyquist sampling theorem, to accurately reconstruct a continuous low-pass analog signal from its discrete samples, the sampling frequency ($f_s$) must be at least twice the highest frequency component ($f_{\max}$) present in the original signal: $$\mathbf{f_s = 2 \times f_{\max}}$$
---

## 12. ```[2021 Honours CC-8 - Q4(b)]``` Find Nyquist rate for the signal: $m(t) = 2 \sin (4\pi t) \cos (2\pi t)$.
**Solution**: Use the trigonometric identity $2 \sin A \cos B = \sin(A + B) + \sin(A - B)$:
$$m(t) = \sin(4\pi t + 2\pi t) + \sin(4\pi t - 2\pi t) = \sin(6\pi t) + \sin(2\pi t)$$

Identify angular frequencies ($\omega = 2\pi f$):
- First term: $2\pi f_1 = 6\pi \implies f_1 = 3\text{ Hz}$
- Second term: $2\pi f_2 = 2\pi \implies f_2 = 1\text{ Hz}$

The maximum frequency in the signal is $f_{\max} = 3\text{ Hz}$.

The Nyquist Sampling Rate is:
$$\text{Nyquist Rate} = 2 \times f_{\max} = 2 \times 3\text{ Hz} = \mathbf{6\text{ samples/second (or } 6\text{ Hz)}}$$
---

## 13. ```[2021 Honours CC-8 - Q4(c)] / [2022 General SEC-A-I - Q6(d)] / [2021 General Paper-IV - Q3] / [2018 General Paper-IV - Q1(e)]``` Define channel capacity and state how SNR is related to Shannon capacity.
- **Channel Capacity**: The theoretical maximum data rate (in bits per second) supported by a communication channel.
- **Relationship**: Described by Shannon's Capacity Formula for noisy channels: $$\mathbf{C = B \log_2 (1 + \text{SNR})}$$
- Channel capacity increases logarithmically with an increase in $\text{SNR}$. If $\text{SNR} \to 0$ (noise overwhelms signal), the capacity drops to $0$ regardless of available bandwidth.
---
## 14. ```[2018 General CS Paper-IV - Q4(a)]``` Consider a noiseless channel with a bandwidth of $3000\text{ Hz}$ transmitting a signal with two signal levels. What is the maximum bit rate of this channel? [2 Marks]
**Solution**: Given $B = 3000\text{ Hz}$, $L = 2$ signal levels.
Apply Nyquist Bit Rate formula:
$$\text{Bit Rate} = 2 \times B \times \log_2 L$$
$$\text{Bit Rate} = 2 \times 3000 \times \log_2(2) = 6000 \times 1 = \mathbf{6000\text{ bps (or } 6\text{ kbps)}}$$
---