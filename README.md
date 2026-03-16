# RP2350 MCU Development Board With Built-In Debugger Tools and ADC Precision Voltage Reference
Designing my own large-scale RP2350-based microcontroller development board PCB with a 4-layer stack and impedance controller track using KiCAD software, with a built-in debugger for the RP2350/RP2040 MCU, like Debugprobe, based on the Raspberry Pi Pico development board.

1) Support built-in and external debugger tools for my development board to allow the use of third-party debugger tools via the JTAG connector. Capable external Raspberry Pi Debugprobe debugger tools via Raspberry Pi 3-pin debug connector with UART port. The jumper can reconfigure the UART source on JP9-JP12. The board is provided with two JST SH-SM03B-SRSS connectors.

2) Support power priority, which will override the ‘target’ USB Type-C connector when ‘Debugger’ is connected to the PC for debugging a code project. It helps to prevent power from the PC’s USB port when the ‘target’ connector is connected to an adapter or USB charger. Power multiplexer with a setting to prioritise the power source brought from the Texas Instruments TPS2116 IC.

3) Switching voltage regulator 3.3V with Texas Instruments TPS62A01 IC, which is capable of up to one ampere to power a load by using the 3.3V pin in the connector of the board and also powering both RP2040 (debugger) and RP2350B (target).

4) The RP2350B MCU GPIO support up to 48 I/O pins as well as eight analogue ports.

5) Compatibility Qwiic modules where the board has a 4-pin JST SM04B-SRSS-TB.

6) Flash memory W25Q128/W25Q16 or similar for both debugger and target for RP2040, RP2350 MCU because these Raspberry Pi MCUs don’t have internal flash memory, so need to add. If you don’t want to add flash, consider using the RP2354A/B MCU, which includes 2 MB of flash memory.

7) A differential pair is applied with 90-ohm impedance for two USB ports with a common choke to prevent EMI interference, according to the USB specification.

8) A four-layer stack PCB include 2 layers each for powering and signal tracks groups.

9) Included built-in three-user LEDs with tri-colour (Red, Yellow, Green) and two buttons with a debouncing circuit. Two green LEDs indicate the board's power and are connected to the PC via the debugger's USB connector. The TH and SMT jumpers support configuration of UART GPIO ports, QSPI memory chip selection GPIO port, enable/disable of user and power LEDs, and the user button.

My design work is copyrighted by Mihails Zaslavskis. All rights are reversed. Reproduction and distribution of this design work are strictly forbidden without my prior permission.
