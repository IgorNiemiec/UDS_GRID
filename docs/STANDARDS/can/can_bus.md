# TRON DIAGNOSTICS

     ██████╗ █████╗ ███╗   ██╗     ██████╗ ██╗   ██╗███████╗
    ██╔════╝██╔══██╗████╗  ██║    ██╔═══██╗██║   ██║██╔════╝
    ██║     ███████║██╔██╗ ██║    ██║   ██║██║   ██║█████╗  
    ██║     ██╔══██║██║╚██╗██║    ██║▄▄ ██║██║   ██║██╔══╝  
    ╚██████╗██║  ██║██║ ╚████║    ╚██████╔╝╚██████╔╝███████╗
     ╚═════╝╚═╝  ╚═╝╚═╝  ╚═══╝     ╚══▀▀═╝  ╚═════╝ ╚══════╝

------------------------------------------------------------------------

# 🛰️ Controller Area Network (CAN)

The **Controller Area Network (CAN)** is the central nervous system of
modern vehicles.\
It allows ECUs (Electronic Control Units) to communicate without needing
a central computer.

Originally created by **Robert Bosch GmbH**, CAN evolved into the global
standard:\
**ISO 11898** --- used in automotive, industrial, aerospace and robotics
systems.

------------------------------------------------------------------------

## 🚗 Why CAN Matters in Diagnostics

Every modern car uses CAN for:

-   ✔ Live telemetry\
-   ✔ ECU diagnostics (UDS / KWP2000 / OBD-II)\
-   ✔ ABS / ESP / Airbag communication\
-   ✔ Powertrain data\
-   ✔ Immobilizer handshake\
-   ✔ Firmware flashing (bootloaders)

All diagnostic tools (J2534, Mongoose, VCX, Techstream, IDS, ODIS etc.)
operate entirely on CAN or CAN-based protocols.

------------------------------------------------------------------------

# ⚡ CAN Bus --- Technical Overview

## 🔌 Voltage Levels

  State           CAN_H     CAN_L
  --------------- --------- ---------
  Recessive (1)   ≈ 2.5 V   ≈ 2.5 V
  Dominant (0)    ≈ 3.5 V   ≈ 1.5 V

Differential signaling provides:

-   Noise immunity\
-   Long-cable reliability\
-   Safety-critical communication integrity

------------------------------------------------------------------------

## 🚀 Bus Speeds

  Speed            Usage
  ---------------- -----------------------------------
  125 kbps         Comfort modules
  250 kbps         Body CAN, Gateway
  500 kbps         Powertrain (engine, ABS, gearbox)
  1 Mbps           High-performance ECUs
  2--5 Mbps (FD)   Modern CAN-FD systems

**Toyota Yaris 2012:**\
- 500 kbps --- Powertrain\
- 250 kbps --- Body CAN

------------------------------------------------------------------------

# 🧪 UDS Example

### ▶ Request

    ID: 0x7E0
    DATA: 02 10 01 55 55 55 55 55

Meaning: **DiagnosticSessionControl -- start extended session**

### ◀ Response

    ID: 0x7E8
    DATA: 02 50 01 55 55 55 55 55

Meaning: **Positive Response**

------------------------------------------------------------------------

    ╔══════════════════════════════════════╗
            IGOR NIEMIEC SYSTEMS
    ╚══════════════════════════════════════╝
