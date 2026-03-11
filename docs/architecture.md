# System Architecture

## Overview

The system is composed of the following subsystems:

1. Power Supply
2. Microcontroller
3. Traffic Light Output Drivers
4. Timing Control (Firmware)
5. Extended Input System (Pedestrian feature)

## Hardware Components

- Microcontroller (Arduino Uno / ATmega328P)
- 6 LEDs (Traffic lights)
- 6 Current limiting resistors (220Ω)
- Breadboard / custom PCB
- 5V power supply

## System Operation

1. The microcontroller controls LED outputs.
2. Firmware implements a Finite State Machine (FSM).
3. Each state represents a traffic condition.
4. A timer controls transitions between states.

## Pin Mapping

| Signal | Arduino Pin |
|-------|-------------|
| NS_RED | D2 |
| NS_YELLOW | D3 |
| NS_GREEN | D4 |
| EW_RED | D5 |
| EW_YELLOW | D6 |
| EW_GREEN | D7 |

## LED Wiring

Each LED is connected in series with a 220Ω resistor.

Connection format:
Arduino pin -> resistor -> LED anode
LED cathode -> GND