# NE555 Variable Pulse Width Modulation (PWM) Controller

## What This Circuit Does

This is a power control circuit that uses a 555 timer to generate a square wave with an **adjustable pulse width (Duty Cycle)**. This variable signal is then used to switch a higher-voltage (30V) load, which is commonly required in applications like motor speed control or power rectification.

## Simulation Notes (LTSpice)

* **Potentiometer:** In the schematic, the two resistors **R1** and **R2** (left side, 5kΩ total) represent a **single physical potentiometer**. The combination allows you to adjust the time the pulse is OFF, thereby controlling the duty cycle from near 0% to 100%.
 **PWM Output Measurement**: The final PWM output is the voltage measured across the load resistor, R5. This voltage shows the actual switched signal going to the external 30V load.
## Schematic Preview
<img width="1450" height="792" alt="image" src="https://github.com/user-attachments/assets/b7258120-8918-46e8-addf-0ff117233dd2" />
<img width="1904" height="560" alt="image" src="https://github.com/user-attachments/assets/a8b3c55e-5ebe-43f7-b494-12f35327f454" />


## Key Components

* **U1:** NE555 - The timer chip that creates the repeating pulse.
* **R1, R2:** 5 kΩ total - **Potentiometer:** Controls the pulse width (duty cycle).
* **R3:** 1 kΩ - Charging resistor for the timing capacitor C1.
* **R4:** 1 kΩ - Current limiting resistor for the base of the transistor Q1.
* **R5:** 1 kΩ - Load resistor for the 30V switching circuit.
* **C1:** 100 nF - Timing capacitor that, along with R1, R2, and R3, sets the pulse frequency.
* **C2:** 100 nF - Bypass capacitor connected to the Control Voltage (CV) pin  to prevent noise interference.
* **D1, D2:** 1N4148 - Diodes that separate the charge (ON) and discharge (OFF) paths of C1.
* **D3:** 1N4148 - Protection diode for the switching circuit (V2/R5).
* **Q1:** 2N2222 - Transistor switch for the 30V load.
* **V1:** 9V - Power for the 555 timer control circuit.
* **V2:** 30V - Power for the external load/rectifier section being switched.

## KiCad schematics : 
<img width="1053" height="697" alt="image" src="https://github.com/user-attachments/assets/3290d87a-fb98-4d37-9c36-2bb36ad913ff" />
<img width="1195" height="616" alt="image" src="https://github.com/user-attachments/assets/5782f73b-42b5-430d-937f-ef5e46f5b73b" />
<img width="2208" height="1463" alt="image" src="https://github.com/user-attachments/assets/c78be653-2403-4049-b061-73b77a982402" />

