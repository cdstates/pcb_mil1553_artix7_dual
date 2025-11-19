# MIL-STD-1553 Ethernet Protocol Adapter - Dual Configuration

A practice PCB project converting a quad MIL-STD-1553 connection design to an optimized dual connection configuration with enhanced USB and Ethernet connectivity. Built around the Xilinx Artix-7 FPGA for protocol conversion and data handling.

![PCB Overview - Original Quad Version](readme_dependancies/scrsho_pcb_overview_quad_v1.png)

To adapt to a dual traix connector version with greater galvanic isolation to reduce noise, below is the current flow chart plan for the entire board make up.
<img width="1240" height="759" alt="image" src="https://github.com/user-attachments/assets/5d5ff565-8619-46d4-bed8-679be0af9ed2" />


## Project Overview

This project represents an evolution in MIL-STD-1553 protocol adapter design, transitioning from a quad-channel to a more streamlined dual-channel architecture while significantly improving the USB and Ethernet interfaces.

**Design Goals:**
- Convert quad MIL-STD-1553 connections to dual configuration
- Enhance USB connectivity for better data throughput and reliability
- Improve Ethernet interface for more robust network communication
- Maintain compatibility with Artix-7 FPGA architecture
- Practice advanced PCB design techniques with real-world military/aerospace protocols

## Features

### Current Dual Configuration
- **2x MIL-STD-1553 Channels** - Dual triaxial connections for aerospace/defense bus communication
- **Artix-7 FPGA** - Xilinx FPGA for protocol conversion and signal processing
- **Enhanced Ethernet PHY** - Improved network connectivity for remote operation
- **Upgraded USB Interface** - Better USB implementation with FTDI chipset for reliable data transfer
- **Power Management** - Comprehensive power supply design with switching regulators
- **SRAM Memory** - External memory for data buffering and FPGA operations

### Key Subsystems
- **Ethernet to MIL-STD-1553 Protocol Bridge**
- **FPGA Configuration & Programming Interface**
- **USB Data and Power Management**
- **Multi-rail Power Generation (3.3V, 2.5V, 1.0V, etc.)**
- **Memory Interface (SRAM)**
- **MIL-STD-1553 Transceiver Circuitry**

## Technical Specifications

### FPGA Platform
- **Device:** Xilinx Artix-7 series
- **Configuration:** JTAG & SPI Flash programming
- **I/O:** Extensive general-purpose I/O for connectivity

### Communication Interfaces
- **MIL-STD-1553:** 2 dual-redundant bus connections (triaxial connectors)
- **Ethernet:** 10/100 Mbps PHY
- **USB:** FTDI-based USB 2.0 interface

### Power Requirements
- Multiple regulated voltage rails
- Switching regulators for efficiency
- Comprehensive ground plane management

## Project Structure

```
├── Eth2Mil1553_Quad_Artix7.SchDoc          # Top-level quad schematic
├── Ethernet2Mil_Adapter_Dual.PcbDoc        # Dual configuration PCB layout
├── Artix7_IO_General.SchDoc                # FPGA I/O connections
├── Artix7_Power_*.SchDoc                   # FPGA power distribution
├── Artix7_ProgramAndConfig.SchDoc          # FPGA programming interface
├── Artix7_SRAM.SchDoc                      # Memory interface
├── Ethernet_PHY.SchDoc                     # Ethernet physical layer
├── USB_FTDI.SchDoc                         # USB controller
├── Power_Generation.SchDoc                 # Power supply design
├── IO_MIL1553_TopConfiguration.SchDoc      # MIL-1553 interface
├── readme_dependancies/                    # Documentation resources
│   ├── pdf_current_dual_schematics_v1.pdf # Current dual version schematics
│   └── scrsho_pcb_overview_quad_v1.png    # Original quad PCB overview
└── README.md                               # This file
```

## Documentation

### Schematics
The complete dual configuration schematics are available in PDF format:
- [Dual Version Schematics (PDF)](readme_dependancies/pdf_current_dual_schematics_v1.pdf)

### Design Files
This repository contains Altium Designer project files:
- `.PrjPcb` - Main project file
- `.SchDoc` - Schematic documents
- `.PcbDoc` - PCB layout documents

## Changes from Quad to Dual

**MIL-STD-1553 Connections:**
- Reduced from 4 channels to 2 channels
- Maintained dual-redundant bus architecture per channel
- Optimized routing for better signal integrity

**USB Improvements:**
- Enhanced FTDI controller implementation
- Separate power and data management circuits
- Improved USB data reliability and throughput

**Ethernet Enhancements:**
- Updated PHY configuration
- Better EMI/EMC considerations
- Improved routing and impedance matching

## Development Status

🚧 **Practice/Learning Project** - This is an educational PCB design project focused on:
- High-speed digital design techniques
- Military/aerospace communication protocols (MIL-STD-1553)
- FPGA integration and power design
- Multi-layer PCB layout best practices

Currently transitioning from private to public release — expect incremental updates and documentation improvements.

## Tools & Technologies

- **PCB Design:** Altium Designer
- **FPGA:** Xilinx Artix-7 (Vivado toolchain)
- **Version Control:** Git/GitHub
- **Standards:** MIL-STD-1553, IEEE Ethernet standards

## License

See [LICENSE](LICENSE) file for details.

## Author

Cody States  
*January 2025*

---

**Note:** This is a practice project demonstrating PCB design skills with real-world aerospace communication protocols. The design is shared for educational and portfolio purposes.
