---
title: Review of Fundamental Concepts
---

<style>
:root {
    --markdown-font-family: "Times New Roman", Times, serif;
    --markdown-font-size: 10.5pt;
}
</style>

<p class="supt1 center">Electronic Systems</p>

# Assignment 1: Review of Fundamental Concepts

<p class="subt2 center">
Academic year 2024-2025
</p>
<p class="subt2 center">
Alonso Herreros Copete
</p>

---

## Self-test Questions

### Question 1
What mathematical function corresponds to a signal amplifier? Consider a sinusoidal voltage signal
with a peak- to-peak amplitude of 1V, a mean value of 3V, and a frequency of 3kHz. Model this signal
as the function x(t). Can you model the output y(t) if the voltage gain is 2?

> It's a multiplication factor which is the Gain ($G$) of the amplifier
>
> $$V_o = G · V_i ⇒ V_o(t) = G · V_i(t)$$

### Question 2
Draw an electrical model of a voltage amplifier with a gain of 2V/V, and input/output resistances of
1MΩ and 1kΩ, respectively.

> ![alt](figures/fig1.2.drawio.svg)

### Question 3
Calculate the gain symbolically when a voltage generator with a 50Ω output resistance is connected
to the amplifier's input, and a resistive load of 10kΩ is connected to its output.

>
> The voltage at the input of the amplifier is simple to find, as the circuit is a voltage divider:
>
> $$
> V_i = \frac{R_i}{R_i + R_g} V_g
> $$
>
> A similar analysis can be done at the output of the amplifier:
>
> $$
> V_o = \frac{R_L}{R_L + R_o} A_v V_i
> $$
>
> By chaining those two expressions we can find the output voltage and the gain of the amplifier:
>
> $$
> V_o = \frac{R_L}{R_L + R_o} A_v \frac{R_i}{R_i + R_g} V_g
> $$
>
> $$
> G = \frac{V_o}{V_g} = \frac{R_i}{R_i + R_g} \frac{R_L}{R_L + R_o} A_v
> $$
>
> Substituting the given values:
>
> $$
> \boxed{G = \frac{V_o}{V_g} = \frac{1M}{1M + 50} \frac{10k}{10k + 1k} · 2 = 1.82}
> $$

### Question 4
We will now review the basic amplification stages using MOSFETs and resistors. Match the elements in
the table.

| Configuration         | Function          |
| :-------------------- | :---------------- |
| CS or Common Source   | Voltage buffer    |
| SF or Source Follower | Voltage amplifier |
| CG or Common Gate     | Current buffer    |

>
> | Configuration         | Function              |
> | :-------------------- | :-------------------- |
> | CS or Common Source   | **Voltage amplifier** |
> | SF or Source Follower | **Voltage buffer**    |
> | CG or Common Gate     | **Current buffer**    |

### Question 5
What is the advantage of using an active load in a CMOS amplifier instead of a resistive load?

> There are many advantages to using active loads in CMOS amplifiers
>
> * An active load provides much higher output impedance than a resistive load, which allows greater
>   gain
> * The active load's higher output impedance also allows for a higher load impedance, which again
>   translates into higher gain
> * The active load usually operates with a lower voltage drop, which allows the amplifier to have a
>   greater swing
> * Resistors dissipate energy as heat, while active loads can be designed to be more efficient
> * For the ouput impedance provided by an active load, its size on the chip is much smaller than the
>   size of the resistor required to match it
> * The active load, being transistor-based, can be included in the CMOS manufacturing process, while
>   a resistor would have to be added as a separate component.

### Question 6
What is a virtual short in an operational amplifier?
