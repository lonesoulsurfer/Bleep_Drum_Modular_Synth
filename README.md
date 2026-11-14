# Bleep Drum: Arduino drum machine for Eurorack

This is the [Bleep Drum](https://bleeplabs.com/product/the-bleep-drum/) by Bleep Labs, in a Eurorack module. It is an Arduino drum machine with 4 sounds. You record patterns when you play them, and you can add layers to make drum beats. I added a sync input, so you can play with other modules.

![Bleep Drum](https://github.com/user-attachments/assets/ce6583b1-c790-486d-bd8b-8271f86fc775)

## Build guide and video

- Step-by-step build guide on Instructables: [Bleep Drum Synth - Powered by Arduino](https://www.instructables.com/Bleep-Drum-Synth-Powered-by-Arduino/)
- Video on YouTube: [Bleep Drum](https://youtu.be/1a5sbbQQU68)

## Features

- 4 sounds, 2 of them with pitch control
- Record patterns when you play them. A quantizer keeps the hits in time.
- Reverse mode and noise mode
- Click track and tap tempo
- Sync input
- Power from 9 V (or 12 V)

## What you need

### Hardware

- All parts are in the [parts list](Parts%20List.pdf).
- The schematic is [Schematic.png](Schematic.png).
- The Gerber files for the PCB and the front panel are in [Gerber Files](Gerber%20Files/). You can send them to a PCB maker.

### Software

- Arduino IDE
- An Arduino Nano

## Upload the firmware

1. Download this repository. Click **Code → Download ZIP**, then extract the ZIP file.
2. Open `Software/BLEEP_DRUM_15_legacy_upgrade/BLEEP_DRUM_15_legacy_upgrade.ino` in the Arduino IDE.
3. Connect the Arduino Nano to your computer with a USB cable.
4. In the **Tools** menu, set these values:
   - **Board:** Arduino Nano
   - **Processor:** ATmega328P
   - **Port:** the COM port of your Nano
5. Click **Upload**.
6. Wait for the message **Done uploading**.

> **Note:** If the upload fails, set **Processor** to **ATmega328P (Old Bootloader)**, then try again. Many clone Nano boards need this setting.

## Files in this repository

| Folder or file | Contents |
|----------------|----------|
| `Software/BLEEP_DRUM_15_legacy_upgrade/` | Firmware (Bleep Labs code) |
| `KiCad - Bleep Drum/` | KiCad files for the front panel |
| `Front Panel Design - Inkscape.svg` | Front panel artwork |
| `Gerber Files/` | Gerber files for the PCB and the front panel, ready to order |
| `Parts List.pdf` | Parts list |
| `Schematic.png` | Schematic |

## Why I made it

I want to make my own modular synth that is simple to build. Each module has these aims:

- It operates from 9 V (and 12 V).
- It is easy to build, with a minimum of components.
- It uses an Arduino, to keep the parts count low and everything in tune.
- It fits in any Eurorack case, and it can use normal Eurorack power.
- It sounds good.
- It is portable.

![Bleep Drum module](https://github.com/user-attachments/assets/3c29e68c-9d75-4e66-9e00-e2650b4bcf37)

## Credits

- Original design and code: the [Bleep Drum](https://bleeplabs.com/product/the-bleep-drum/) by John-Mike Reed (Dr. Bleep), [Bleep Labs](https://bleeplabs.com/). Thank you, Bleep Labs.
- PCB, front panel, Eurorack version and sync input: Marcus ([lonesoulsurfer](https://github.com/lonesoulsurfer)).

## Support

Do you like this project? You can support my work on [GitHub Sponsors](https://github.com/sponsors/lonesoulsurfer).

## Licence

- **Hardware** (PCB, front panel and Gerber files): [CERN Open Hardware Licence v2, Strongly Reciprocal](LICENSE). You can make, change and sell boards. If you share or sell a changed design, you must also share the changed design files under the same licence. Copyright (c) 2025 Marcus (lonesoulsurfer).
- **Firmware** (`Software/`): the Bleep Drum code by Bleep Labs. Bleep Labs does not give a licence for this code. The CERN licence does **not** apply to it. Before you use the code for a commercial purpose, ask [Bleep Labs](https://bleeplabs.com/) for permission.
