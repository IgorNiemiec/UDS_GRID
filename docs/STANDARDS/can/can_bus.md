 ██████╗ █████╗ ███╗   ██╗     ██████╗ ██╗   ██╗███████╗
██╔════╝██╔══██╗████╗  ██║    ██╔═══██╗██║   ██║██╔════╝
██║     ███████║██╔██╗ ██║    ██║   ██║██║   ██║█████╗  
██║     ██╔══██║██║╚██╗██║    ██║▄▄ ██║██║   ██║██╔══╝  
╚██████╗██║  ██║██║ ╚████║    ╚██████╔╝╚██████╔╝███████╗
 ╚═════╝╚═╝  ╚═╝╚═╝  ╚═══╝     ╚══▀▀═╝  ╚═════╝ ╚══════╝


The Controller Area Network (CAN) is the central nervous system of modern vehicles.
It allows ECUs (Electronic Control Units) to communicate without a central computer orchestrating them.

Originally designed by Robert Bosch GmbH, CAN has become the ISO standard (ISO 11898) for inter-module communication in automotive, industrial, aerospace and robotics sectors.


**Why CAN Matters in Diagnostics?

Every modern car relies on CAN for:

✔ Reading live telemetry
✔ ECU diagnostics (UDS / KWP2000 / OBD-II)
✔ Safety systems (ABS, ESP, Airbags)
✔ Powertrain data
✔ Immobilizer handshake signaling
✔ Firmware flashing (Bootloader protocols)

Your diagnostic tools (J2534, Mongoose, VCX, etc.) operate entirely through CAN or CAN-based protocols.

**CAN Bus — Technical Overview

Voltage Levels

Recessive (1): CAN_H ≈ 2.5V / CAN_L ≈ 2.5V

Dominant (0): CAN_H ≈ 3.5V / CAN_L ≈ 1.5V

Differential signaling provides:

Noise immunity

Long cable reliability

Safety-critical communication

2. Bus Speeds

** Speed	       ** Usage
125 kbps	    Comfort modules
250 kbps	    Body CAN, Gateway
500 kbps	    Powertrain (engine, ABS, gearbox)
1 Mbps	        High-performance ECUs, some gateways
2–5 Mbps (FD)	CAN FD – modern ECUs, faster diagnostics

Toyota Yaris 2012 uses: 500 kbps for powertrain CAN and 250 kbps for body CAN


Example (UDS request):

ID: 0x7E0
DATA: 02 10 01 55 55 55 55 55
Meaning: DiagnosticSessionControl (start extended session)


Response example:

ID: 0x7E8
DATA: 02 50 01 55 55 55 55 55
Meaning: Positive Response


╔══════════════════════════════════════╗
          IGOR NIEMIEC SYSTEMS
╚══════════════════════════════════════╝

