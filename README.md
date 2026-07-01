# The Clampinator

Inspired by the [ODrive Regen Clamp](https://shop.odriverobotics.com/products/odrive-regeneration-clamp), the clampinator is a custom built regeneration clamp targeting 16-60V systems.

<img width="275" height="181" alt="PCB-front-red" src="https://github.com/user-attachments/assets/5b626801-da6c-4c65-be0e-ef296720d8cd" />

## Key Features
 - 16-60V input
 - Adjustable clamp voltage via trimpot
 - Full reverse current protection via TI's [LM7481-Q1](https://www.ti.com/product/LM7481-Q1)
   - Ideal diode inrush current limiting supported, but marked as DNP
 - External pre-charge resistor
 - **FULL galvanic isolation between power and logic domains**
 - USB-C port for programming
 - STM32H5 based logic control
   - Digital control to disconnect power input from output
   - 2x CAN FD exposed w/toggleable termination resistors
 - Two onboard LEDs (Yellow and RGB)
 - Two 10k thermistor slots for thermistors
 - Two 15V outputs for active cooling fans

> [!CAUTION]
> The Clampinator must not be plugged in unless the power switch is off. To turn on, slide power switch to `PRECHARGE`, and only proceed to `RUN` after allowing at least 1s for the bulk capacitors to charge.

## Using the CAN bus

The STM32 on the board is equipped with two built in CAN FD controllers, and the Clampinator has two accompanying CAN transcievers in the bottom left of the board. There is dip switch `SW5` which can be used to toggle the internal 120Ω termination resistors.

## Building the Clampinator
The Clampinator can be ordered from sites like JLCPCB. The KiCAD source files are in `./KiCAD` and the production gerber files are in `./KiCAD/prod` along with the bom.

## Images 

 - Pinout here

## Schematic

### Main Circuit
<img width="1218" height="840" alt="Main Circuit (Page 1 of 3)" src="https://github.com/user-attachments/assets/99921c4a-d8c3-4e44-ae9f-53d71fed1adf" />

## Logic Side Circuit
<img width="1248" height="863" alt="(Page 2 of 3)" src="https://github.com/user-attachments/assets/288a0b78-cb1b-4c6c-b30f-257a9d822733" />

## Thermal Management
<img width="1205" height="828" alt="(Page 3 of 3)" src="https://github.com/user-attachments/assets/5fbfa781-a424-47a1-ac28-73e834e8f2a2" />

## BOM

 - Final BOM goes here
