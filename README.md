
Tunable Function Generator

This project involves the design and implementation of a Tunable Function Generator capable of generating sine, square, and triangular waveforms. The key feature of this function generator is tunability — both the magnitude and frequency of the waveforms can be controlled using potentiometers.

1.Generates three types of waveforms:

SINE WAVE:
A sine wave is defined by a smooth, periodic oscillation characterized by a continuous wave-like pattern. It is foundational in signal processing, used in various applications including audio and radio signals.

SQUARE WAVE: 
A square wave is a non-sinusoidal waveform that switches abruptly between high and low states. It is widely used in digital electronics and signal processing, where it represents binary states.

TRIANGULAR WAVE:
A triangular wave is a periodic, non-sinusoidal waveform characterized by its triangular shape. It's a piecewise linear, continuous real function where the rise and fall times are equal

2.Components: DSO,Power Supply,Breadboard,Connecting Wires,Opamps,Diodes,Resistors,Capacitors,Potentiometer.

3.Tunability:
Amplitude of each waveform can be varied using potentiometers.

How can we control Amplitude? - Non-inverting circuit gain controls amplitude of waveforms.

Frequency Control Modes:

1. Common Frequency Mode

All waveform outputs (Sine, Square, Triangle) are derived from a single oscillator.Sine is generated from wein bridge,using sine as input in non inverting schmitt trigger we get square as output , and taking square as output in integrator we get triangular wave.

Same frequency across all waveforms.

No individual control.

Minimal hardware required (simplest design).

2. Partially Controlled Frequency Mode

Sine wave has independent frequency control with its respective wein bridge.Integrator integrates square wave ,produces a triangle wave and this Triangle wave is fed into non inverting Schmitt trigger, which compares it to thresholds (Vth and vtl) and gives a square output and loop continues.

Square and Triangle share a common frequency.

Moderate hardware requirement due to partial decoupling.

3. Fully Independent Frequency Mode

Sine, Square, and Triangle generators all have separate, independently controlled frequencies 

Maximum control over signal behavior.

High hardware requirement due to complete separation of control paths but complex.

Here we implemented the second (Partially Controlled ) configuration, as it offers the best balance from the perspective of hardware control and frequency flexibility.
The formulas for frequency is prooved in attached images for sine , square and triangular wave.

PRACTICAL RESULTS:(Partially Controlled mode)

SINE:

Frequency-203Hz to 16.83kHz
Amplitude-0.5V to 12V

SQUARE:

Frequency: 400Hz to 12KHz
Amplitude: 1V to 11V

TRIANGLE:

Frequency: 400Hz to 12KHZ
Amplitude: 1V to 12V










