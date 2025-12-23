# MVME712M P2 Adapter Board

An open-source hardware replacement for the **Motorola MVME712M P2 Adapter**.

This board is designed to interface with Motorola VME CPU modules (such as the MVME147, MVME162, MVME167, and MVME177 series) to provide the necessary signals for the **MVME712M Transition Module**.

## Overview

The MVME712M P2 Adapter is a small passive board that plugs directly into the **P2 connector** on the VME backplane behind the CPU module. It breaks out the SCSI, Serial, and Centronics signals to a 50-pin header (or specific cable) that then connects to the MVME712M bulkhead/transition module.

This repository contains the KiCad design files to manufacture a modern replacement for the original Motorola part, which is often difficult to find or expensive on the used market.

## Hardware Features

* **Form Factor:** Standard VME P2 adapter dimensions.
* **Connectors:** * 96-pin DIN 41612 (Connector for VME P2 backplane).
* High-density or IDC headers for connection to the MVME712M transition board.


* **Compatibility:** Designed for use with Motorola MVME modules and the MVME712 series transition boards.
* **Passive Design:** No active components required; uses direct signal routing according to original Motorola specifications.

## Project Structure

```text
├── gerber/    # Gerbers, Drill files
└── docs/      # Pinout diagrams and reference manuals

```

## Compatibility List

This adapter is typically required for the following Motorola CPU boards when using an MVME712M transition module:

* MVME147
* MVME162 / MVME162P
* MVME167
* MVME172
* MVME177

## Usage

1. **Fabrication:** Use the provided Gerber files in the `Manufacturing/` folder to order PCBs (standard 1.6mm FR4, 1oz copper is sufficient).
2. **Assembly:** Solder the 96-pin DIN 41612 connector (Female/Socket) and the appropriate shrouded headers.
3. **Installation:** * Power down the VME chassis.
* Plug the adapter onto the **P2 pins** on the back of the backplane, directly behind your CPU module.
* Connect the internal ribbon cable from the adapter to your MVME712M transition module.



## License

This project is released under the [CERN Open Hardware Licence](https://www.google.com/search?q=https://ohwr.org/project/cernohl/wikis/Documents/CERN-OHL-version-2) or [MIT License] — *Please update this section according to your preference.*

## Disclaimer

This is a community-driven project. While every effort has been made to ensure accuracy based on original documentation, use this hardware at your own risk. The author is not responsible for any damage to vintage VME equipment.

---

*Created by [parceval*](https://github.com/parceval)
