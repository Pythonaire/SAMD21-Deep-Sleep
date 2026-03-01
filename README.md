### Deep Sleep 
For example, a Adafruit Feather M0 board use the SAMD21 mcu. This mcu has two oscillators:
- 32 kHz internal "OSCULP32K" and
- 48 Mhz external "DFLL48M"
Mostly scripts or libraries using the DFLL48M. So working with times, the chip cannot be set into deep sleep mode to save battery capacity.

This modified library use the standard Arduino library and functions, but with the OSCULP32K oscillator. This oscillator is not very precise (drift around +/- 1 %) but we can set the chip into deep sleep, down to micro ampere power consumption.
