# Programmable Frequency Synthesizer based on PLL

## Overview
This project implements two designs for a programmable frequency synthesizer using a Phase-Locked Loop (PLL) as its core. The first design uses classic TTL logic (7493 counter), and the second uses a programmable microcontroller (PIC16F628A) for greater flexibility. The project covers design, simulation, PCB fabrication, and testing.

## Key Features
*   **Core PLL:** CD4046 / LM565
*   **Design Approaches:**
    *   **TTL Version:** Fixed division ratios (x1, x2, x4, x8) using a 7493 counter.
    *   **Microcontroller Version:** Programmable division ratio via GPIO pins using a PIC16F628A.
*   **Simulation:** performed in [Name of Simulator, e.g., NI Multisim] to validate circuit behavior.
*   **PCB Design:** Custom-designed PCB for the microcontroller-based version.
*   **Full Laboratory Report:** Includes theoretical analysis, design calculations, and test results.

## Gallery
| TTL Synthesizer (Simulation) | PIC Synthesizer (PCB Design) |
| :---: | :---: |
| [![Simulation](simulations/results/ttl-sim-thumb.png)](simulations/results/ttl-sim.png) | [![PCB](hardware/pcb/pcb-design-thumb.png)](hardware/pcb/pcb-design.png) |

| Oscilloscope Results (Physical Test) |
| :---: |
| [![Scope](media/oscilloscope-1-thumb.jpg)](media/oscilloscope-1.jpg) |

## Project Structure
```
TLL-PIC-PLL-Frequency-Synthesizer/
├── README.md
├── firmware/
│   └── pic16f628a/
├── hardware/
│   ├── datasheets/
│   ├── pcb/
│   └── schematics/
├── lab-report/
└── media/
├── simulations/
│   ├── multisim/
│   └── results/
```

## Laboratory Report
The complete lab report (in Spanish) is available in the [`/lab-report`](/lab-report/) directory. It includes:
*   **Theoretical Background** on PLLs and frequency synthesis.
*   **Design Calculations** for the 555 oscillator and the PLL filter.
*   **Simulation Results** and analysis.
*   **Comparison** between TTL and microcontroller implementations.
*   **Application Analysis** of synthesizers in FM Radio, TV, and Mobile Phones.

## Repository Contents
*   `/hardware`: Schematics, PCB layout files (e.g., Gerbers), and datasheets.
*   `/firmware`: C code for the PIC16F628A microcontroller.
*   `/simulations`: Simulation files and output waveforms.
*   `/lab-report`: Full detailed lab report in PDF format.
*   `/media`: Photos of the physical setup and oscilloscope measurements.

## Getting Started
### Prerequisites
*   **Simulation:** NI Multisim (or similar) to open simulation files.
*   **Programming:** MPLAB X IDE and a PIC programmer to flash the `.hex` file to the PIC microcontroller.
*   **PCB Viewing:** A Gerber viewer like [KiCad's GerbView](https://www.kicad.org/) or [PCBWay Viewer](https://www.pcbway.com/project/OnlineGerberViewer/).

### Hardware Build
1.  Refer to the schematics in the `/hardware/schematics/` folder.
2.  The BOM is detailed in the lab report.
3.  For the PIC version, program the microcontroller with the provided firmware.

## Conclusions
This project successfully demonstrated two practical implementations of frequency synthesizers. The TTL version offers a simple, cost-effective solution for fixed multiplication factors. In contrast, the microcontroller version provides superior flexibility and programmability, albeit with a more complex design. The results align with simulations and theoretical expectations, confirming the understanding of PLL operation and its applications in modern communication systems.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
*   Professor Ronald P. Coaguila Gómez for guidance.
*   Universidad Católica de Santa María.