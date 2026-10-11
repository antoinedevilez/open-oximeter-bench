# Open Oximeter Bench

A low-cost, open-source test bench to compare how pulse oximeters behave across skin tones.

> Work in progress: personal project started in October 2026.

## Why

Pulse oximeters estimate blood oxygen saturation (SpO2) from how a finger absorbs red and infrared light. Clinical studies show that they overestimate SpO2 more often in patients with darker skin: in a large hospital study, low oxygen levels went undetected about three times as often in Black patients as in White patients (Sjoding et al., *NEJM*, 2020). Testing oximeters on volunteers is slow and expensive, and existing lab simulators have not reproduced this bias.

## The idea

A silicone finger with a soft vessel, through which a motor-driven syringe pumps a coloured liquid to mimic the pulse. Interchangeable skin sleeves of measured tone slide over the finger, and the oximeter under test clips on as it would on a patient.

The key question is the pulsed liquid: does it need the same spectral slope as hemoglobin in the red LED band to reproduce the skin-tone bias? The bench compares two liquids to find out.

The bench is a tool to compare oximeters with each other. It does not replace clinical studies on people.

## Repository structure

| Folder | Content |
|---|---|
| `simulation/` | Python model of the expected bias |
| `cad/` | 3D models: finger, mould, pulse mechanism, enclosure |
| `electronics/` | Schematics and PCB |
| `firmware/` | Microcontroller code |
| `software/` | Oximeter screen reading and data logging |
| `docs/` | Design notes and references |

## Roadmap

- [x] Repository set up
- [x] Python model of the expected bias
- [ ] CAD of the finger, mould, pulse mechanism and enclosure
- [ ] Electronics and firmware
- [ ] Automatic reading of the oximeter screen
- [ ] Physical prototype

## License

Code: MIT (see `LICENSE`). Hardware design files: CERN-OHL-S (to be added).

## Author

Antoine Devilez, microengineering student. Feedback and questions are welcome via Issues.
