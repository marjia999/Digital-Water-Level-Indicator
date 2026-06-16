# Design-and-Implementation-of-Digital-Water-Level-Indicator

## Project Overview
In this project I have explained 2 software simulation of water level indicator.

## Water Level Indicator using 555 Timer & 7 Segment Display
![Software](images/Software.png)

### Components

| Component | Purpose |
|-----------|---------|
| **7SEG-MPX1-CC** | Common cathode seven segment display to show water level percentage |
| **74LS245** | Octal bus transceiver buffer IC to drive seven segment display |
| **4011** | Quad 2-input NAND gates (CMOS) for signal inversion and buffering |
| **4081** | Quad 2-input AND gates (CMOS) for filtering false signals |
| **LM7805** | 5V voltage regulator to provide stable power to CMOS ICs |
| **NE555** | Timer IC configured as astable multivibrator for 1Hz blinking |
| **BC547** | NPN transistor for switching applications |
| **LED-BIBY/LED-BLUE/LED-GREEN/LED-RED/LED-YELLOW** | LEDs for visual water level indication |
| **RES** | Resistors for current limiting |
| **CAP/CAP-ELEC** | Capacitors for filtering and timing |
| **DIODE** | Protection diode for reverse voltage protection |
| **CONN-SIL2/CONN-SIL6** | Connectors for sensor and buzzer interface |
| **BATTERY** | Power source for the circuit |

### Working Principle

This project presents a **Digital Water Level Indicator** designed using digital logic gates. It accurately displays the water level in a tank as percentages 0%, 20%, 40%, 60%, 80%, 100% on a seven-segment display and provides visual LED indications for each level. The circuit is built using CMOS logic gates, ensuring minimal current draw from the water sensors. When water touches a sensor, it connects to ground creating a LOW signal, which is inverted by 4011 NAND gates. AND gates filter false signals caused by water splashing, and the processed signals drive LEDs and seven-segment display through 74LS245 buffer. When 100% level is reached, NE555 timer generates a 1Hz blinking signal for alert.

---

## Water Level Indicator using NOT Gate
![Hardware](images/Hardware.png)

### Components

| Component | Purpose |
|-----------|---------|
| **BC547** | NPN transistor used for switching and signal amplification |
| **LED-BLUE** | Blue LED indicator for water level detection |
| **LED-GREEN** | Green LED indicator for normal water level (40%-80%) |
| **LED-RED** | Red LED indicator for 100% full tank alert |
| **LED-YELLOW** | Yellow LED indicator for 20% low water level warning |
| **NOT** | NOT gate IC for inverting sensor signals |
| **RES** | Resistors for current limiting and biasing transistors |
| **CAP** | Capacitors for filtering and stabilization |
| **VSOURCE** | DC power supply to power the circuit |

### Working Principle

This circuit uses simple NOT gates, resistors, capacitors, NPN transistors, and LEDs to indicate water levels. When water touches a sensor wire in the tank, it completes the circuit path to ground, creating a LOW signal. The NOT gate inverts this LOW signal to HIGH, which then drives the corresponding LED through the BC547 transistor. The LEDs indicate Empty, Low, Half, and Full water levels sequentially as water rises. The transistor acts as a switch, providing enough current to light up the LEDs with proper brightness. This simple design effectively displays water levels without any microcontroller or complex logic.

---

## 👤 Author

**Marjia999**

⭐ If you found this project helpful, please give it a star on GitHub!
