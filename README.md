This project is a discrete implementation of a Class D Audio Amplifier designed from first principles. Instead of using a dedicated Class D chip (like the TPA3116), this design utilizes the ubiquitous NE555 Timer IC to generate Pulse Width Modulation (PWM).⚙️ Specifications
Architecture: Asynchronous Class D (PWM)

⚙️ Specifications

Controller: NE555 Timer (Astable Configuration)

Supply Voltage: 12V DC (Single Supply)

Carrier Frequency: ~218 kHz

Output Power: ~20W (into 4Ω load)

Input Sensitivity: Line Level (Standard AUX)
PWM Generator (NE555): The audio signal is fed into the Control Voltage (Pin 5) of the 555. This modulates the threshold comparators inside the chip, converting the analog audio amplitude into a variable pulse width (Digital PWM) at Pin 3.Power Stage (Half-Bridge): The low-current PWM signal drives a Push-Pull MOSFET pair (IRF540N and IRF9540N). This amplifies the current significantly, allowing the circuit to drive heavy loads.Output Filter (LC): A Low-Pass Filter ($L=22\mu H, C=1\mu F$) removes the high-frequency 218kHz carrier wave, reconstructing the amplified audio signal for the speaker.
