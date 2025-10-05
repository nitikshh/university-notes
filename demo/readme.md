# 🧾 Assignment on **Tank Circuit: Working, Diagram, and Applications**

## 1. Introduction

In the world of electronics, circuits capable of generating or selecting specific frequencies are of great importance. Among them, the **Tank Circuit**, also known as an **LC Circuit**, **Resonant Circuit**, or **Tuned Circuit**, plays a fundamental role in communication systems, signal processing, and oscillation generation.
A tank circuit consists of two key passive components — a **capacitor (C)** and an **inductor (L)** — connected either in series or in parallel. Together, they can store electrical and magnetic energy and exchange it back and forth, forming a natural oscillator at a particular frequency known as the **resonant frequency**.

This resonant behavior makes the tank circuit a vital component in devices such as **radios, filters, transmitters, and receivers**, where frequency tuning and signal selection are essential.

---

## 2. Historical Background

The discovery of oscillatory electrical behavior dates back to **1827**, when **Felix Savary** observed electromagnetic oscillations while experimenting with a **Leyden jar** (a primitive capacitor). His work laid the foundation for the understanding of oscillating electric and magnetic fields.
Later, scientists like **Guglielmo Marconi** used these principles to develop **radio communication systems**, where LC circuits played a critical role in tuning and signal transmission.

---

## 3. Definition of a Tank Circuit

A **Tank Circuit** is defined as:

> *An electrical circuit consisting of a capacitor (C) connected to an inductor (L) that stores and transfers energy between the capacitor’s electric field and the inductor’s magnetic field at a specific resonant frequency.*

It is called a **“tank”** circuit because it “stores” electrical energy temporarily, similar to how a water tank stores water. When the capacitor is charged, it holds energy in its electric field; when discharged through the inductor, energy shifts to the magnetic field — and this back-and-forth exchange creates oscillations.

---

## 4. Construction and Circuit Diagram

A basic tank circuit can be constructed using:

* **Inductor (L)** – made of a coil of conducting wire (usually copper) that stores energy in a magnetic field.
* **Capacitor (C)** – a device with two conductive plates separated by an insulator, storing energy in an electric field.
* **Connecting wires** – to connect the two components either in **series** or **parallel**.

### (a) Parallel LC Tank Circuit

In a **parallel configuration**, the inductor and capacitor are connected across the same voltage source. It behaves as a **resonant circuit** that can store energy efficiently and allows current oscillation between the two components.

<img src="https://www.allaboutcircuits.com/uploads/articles/simple-parallel-resonant-circuit.jpg" width="300px"/>

### (b) Series LC Tank Circuit

In a **series configuration**, the inductor and capacitor are connected one after another in the same path. This arrangement is often used in filters and resonators.

<img src="https://www.allaboutcircuits.com/uploads/articles/simple-series-resonant-circuit.jpg" width="300px"/>

---

## 5. Principle of Operation

The **working principle** of a tank circuit is based on **resonance** — the natural tendency of the system to oscillate at a particular frequency.

1. When the **capacitor** is charged and then allowed to discharge through the **inductor**, current flows through the coil.
2. This flow of current generates a **magnetic field** around the inductor, which stores energy.
3. As the capacitor discharges fully, the magnetic field around the inductor begins to **collapse**, inducing an EMF (electromotive force) in the opposite direction.
4. This EMF **recharges the capacitor** but with **opposite polarity**, and the process repeats.
5. Thus, energy oscillates back and forth between the capacitor’s electric field and the inductor’s magnetic field.

This continuous transfer of energy results in **oscillating current and voltage** — forming an **LC oscillator**.

---

## 6. Mathematical Expression and Resonant Frequency

The **resonant frequency (f)** of the tank circuit is the frequency at which the energy exchange between L and C occurs most efficiently.

The angular frequency (ω) and linear frequency (f) are given by:

[
\omega = \frac{1}{\sqrt{LC}}
]

[
f = \frac{1}{2\pi \sqrt{LC}}
]

Where:

* ( L ) = Inductance (Henrys)
* ( C ) = Capacitance (Farads)
* ( f ) = Resonant Frequency (Hertz)

At this frequency:

* The **inductive reactance (XL)** and **capacitive reactance (XC)** are equal in magnitude but opposite in phase.
* Therefore, ( XL = XC )
* The circuit impedance is purely resistive, allowing maximum current to flow (in series LC) or maximum voltage (in parallel LC).

---

## 7. Energy Exchange and Damping

In an ideal LC circuit, energy exchange continues indefinitely. However, in real systems, resistance in wires and components causes **energy loss**, leading to **damped oscillations**.

To maintain continuous oscillations, **positive feedback** is provided using amplifying components like **transistors or op-amps**, forming an **LC Oscillator Circuit**.

---

## 8. Types of Tank Circuits

Tank circuits can be broadly categorized as follows:

### (a) Series Resonant Circuit

* Inductor and capacitor connected in series.
* Offers **minimum impedance** at resonant frequency.
* Used in **filters** and **signal selection circuits**.

### (b) Parallel Resonant Circuit

* Inductor and capacitor connected in parallel.
* Offers **maximum impedance** at resonance.
* Used in **oscillators** and **tuned amplifiers**.

---

## 9. Working Example (Step-by-Step)

Let’s consider a **parallel LC circuit** connected to a DC power source.

1. **Charging phase:** The capacitor charges up to the supply voltage.
2. **Discharge phase:** The capacitor discharges through the inductor, building a magnetic field.
3. **Recharging phase:** When the magnetic field collapses, it recharges the capacitor in reverse polarity.
4. **Oscillation:** The capacitor continues charging and discharging alternately, creating an oscillating current and voltage.

This cycle repeats as long as energy is supplied, producing **sine wave oscillations** at the resonant frequency.

---

## 10. Importance of Resonance

Resonance allows the circuit to **select or amplify** signals of a particular frequency while rejecting others.
For example, in radio receivers:

* Each station transmits at a unique frequency.
* The LC circuit is tuned (by adjusting L or C) to that frequency.
* Only the desired signal resonates, while others are filtered out.

---

## 11. Applications of Tank Circuits

Tank circuits are extremely versatile and used across many domains of electronics and communication. Key applications include:

### 1. **Radio Tuning**

Used in both transmitters and receivers to select a particular frequency channel.
When tuning a radio, the variable capacitor in the LC circuit adjusts the resonance frequency to match the station’s frequency.

### 2. **Oscillators**

Tank circuits are the fundamental part of **LC oscillators** like **Colpitts**, **Hartley**, and **Clapp oscillators** — generating stable sinusoidal waveforms.

### 3. **Filters**

Used in band-pass, high-pass, and low-pass filters to allow or reject signals of certain frequencies.

### 4. **Frequency Mixers**

Used in devices like frequency modulators and demodulators to produce new frequencies by combining two signals.

### 5. **Tuned Amplifiers**

In RF amplifiers, parallel LC circuits act as load impedance, amplifying signals at resonant frequency.

### 6. **Induction Heating**

Both series and parallel LC circuits are employed to produce high-frequency currents used for induction heating applications.

### 7. **Communication Systems**

Used extensively in **radio transmitters, telecommunication circuits, radar systems**, and **signal generators**.

---

## 12. Advantages and Limitations

### Advantages:

* Simple design and low cost.
* Efficient energy storage and transfer.
* Capable of precise frequency selection.
* Essential for stable oscillations in RF systems.

### Limitations:

* Energy loss due to resistance (damping).
* Sensitive to component tolerances (L and C values).
* Requires stabilization for long-term oscillation.

---

## 13. Real-World Examples

| Application           | Type of LC Circuit | Function                                   |
| --------------------- | ------------------ | ------------------------------------------ |
| AM/FM Radio           | Parallel LC        | Tuning and signal selection                |
| RF Amplifiers         | Parallel LC        | Load impedance and frequency amplification |
| Colpitts Oscillator   | Series-Parallel LC | Frequency generation                       |
| Wireless Transmitters | LC                 | Frequency modulation                       |
| Metal Detectors       | LC                 | Inductive sensing and resonance shift      |

---

## 14. Formula Recap and Numerical Example

**Resonant Frequency Formula:**
[
f = \frac{1}{2\pi \sqrt{LC}}
]

**Example:**
If ( L = 270 \text{ mH} ) and ( C = 1 \text{ nF} ):

[
f = \frac{1}{2\pi \sqrt{(270 \times 10^{-3})(1 \times 10^{-9})}}
]
[
f ≈ 9.67 \text{ kHz}
]

Thus, the circuit will resonate around **9.67 kHz**.

---

## 15. Conclusion

The **Tank Circuit** forms the foundation of many modern electronic and communication systems. Its ability to **store, transfer, and resonate energy** between magnetic and electric fields allows engineers to control frequencies with high precision.

From the earliest **radio transmitters** to **wireless communication**, **oscillators**, and **filters**, the LC tank circuit continues to be a cornerstone in electronic circuit design. Understanding its working principles, mathematical relations, and practical implementations is crucial for every electronics or electrical engineering student.

Would you like me to **generate this as a formatted PDF/DOCX assignment** (with proper titles, spacing, and images placeholders for diagrams)?
That version will be ready to directly **print or submit**.
