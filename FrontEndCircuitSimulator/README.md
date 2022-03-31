# Overview
This repository includes the simulation of the front-end electronics (from the sense-wire upto the preamplification stage) for the MWPC.

## Design options
There are 2 options for the front-end design. 
- Measure only the charge deposition on the sense-wire.
- Record the full signal of the induced current.

## Charge-only design



# How to simulate a circuit in Qucs-S
A very brief introduction to Qucs-S and how to simulate a circuit.

## About Qucs-S
Qucs:
- Qucs is an open-source, cross-platform circuit simulator with GUI. 
- Qucs stands for "Quite Universal Circuit Simulator".
- It allows users to setup a circuit with a graphical user interface (GUI) and simulate the large-signal, small-signal and noise behaviour of the circuit. After that simulation has finished, users can view the simulation results on a presentation page.
- The defaut simulator backend is the in-house "Qucsactor".

Qucs-S:
- Qucs-S is a spin-off of the Qucs project. The "-S" stands for SPICE. It means Qucs-S uses SPICE as backend circuit simulator. Users can also pick NgSPICE as the backend simulator if they want. 
- **Ngspice** is powerful mixed-level/mixed-signal circuit simulator. The most of industrial SPICE models are compatible with Ngspice. It has an excellent performance for time-domain simulation of switching circuits and powerful postprocessor.
- **XYCE** is a new SPICE-compatible circuit simulator written by Sandia from the scratch. It supports basic SPICE simulation types and has an advanced RF simulation features such as Harmonic balance simulation.
- **SpiceOpus** is developed by the Faculty of Electrical Engineering of the Ljubljana University. It based on the SPICE-3f5 code.
- **Qucsator** is also supported as backward compatible.

## Building Qucs-S on Ubuntu (Debian)
The build instruction can be found [here](https://github.com/ra3xdh/qucs_s).

```bash
sudo apt-get install build-essential git cmake qtbase5-dev qttools5-dev qtscript5-dev libqt5svg5-dev ngspice
## Clone the git repo to your preferred location then
mkdir builddir
cd builddir
cmake ..  -DCMAKE_INSTALL_PREFIX=/your_install_prefix/
make
make install
```
The first time you start up the Qucs-S program, a dialog will open to ask you to choose a default backend simulator. This is your choice. I used NgSPICE.

## Circuit simulation with Qucs-S


# Notes on OPA656 models
Notations:
- sbomb195: TINA-TI SPICE model.
- sbom136b: PSPICE model.


