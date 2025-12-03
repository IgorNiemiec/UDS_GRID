## 🔷 UDS GRID — Compatibility Matrix
A structured overview of the most relevant open-source automotive diagnostic tools.
Matrix focuses on UDS, ISO-TP, J2534 and ECU flashing capabilities.

| Repository | UDS | ISO-TP | K-Line | J2534 | CAN (SocketCAN) | Flashing | Immobilizer | OEM-Level | Language |
|-----------|-----|--------|--------|-------|------------------|----------|-------------|-----------|----------|
| **OpenVehicleDiag** | ✔️ | ✔️ | ❌ | ✔️ | ✔️ | ⚠️ (partial) | ❌ | ❌ | Rust |
| **python-can** | ⚠️ (extensions) | ✔️ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **isotp (Python)** | ❌ | ✔️ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **cantools** | ⚠️ DBC only | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **UdsPy** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **PyFlash** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ✔️ ECU Flash | ❌ | ❌ | Python |
| **STM32-UDS-Bootloader** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ✔️ Bootloader | ❌ | ❌ | C |
| **EcuFlashTool** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ✔️ Flash/Read | ❌ | ❌ | C++ |
| **AUDS (Android UDS)** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Java/Kotlin |
| **J2534-API (Open)** | ⚠️ wrapper | ❌ | ❌ | ✔️ | ✔️ via J2534 | ❌ | ❌ | ❌ | C |
| **busmaster** | ⚠️ limited | ❌ | ✔️ | ❌ | ✔️ | ❌ | ❌ | ❌ | C++ |
| **CanCat** | ⚠️ experimental | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **OpenGarages / Car Hacker’s Repo** | ⚠️ | ⚠️ | ⚠️ | ❌ | ✔️ | ⚠️ mixed | ❌ | ❌ | mixed |
| **UDS Scapy Addons** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **SavvyCAN** | ❌ | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | C++/Qt |
| **kayak** | ❌ | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Java |
| **SocketCAN-utils** | ❌ | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | C |
| **CANTact Tools** | ⚠️ | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | Python |
| **CANdevStudio** | ❌ | ❌ | ❌ | ❌ | ✔️ | ❌ | ❌ | ❌ | C++ |
| **EcuDiag (Python)** | ✔️ | ✔️ | ❌ | ❌ | ✔️ | ⚠️ limited | ❌ | ❌ | Python |

### Legend:
- ✔️ = Full support  
- ⚠️ = Partial / limited / experimental  
- ❌ = Not supported  
