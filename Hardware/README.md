# Hardware Design
There are two custom PCBs I designed for this project, one simple one just supporting the input buttons, and the other that contains the actual logic and drivers for the flipdot panel.

The ESP32 handles all of the logic for the display, and feeds into the driver shift registers.

The drivers are MIC5841 (Low Side) and MIC5891 (High Side) devices, there's three pairs covering the 21 columns, and then two pairs covering the 14 rows. There are NAND gates on each set that provide an interlock preventing both the high side and low side drivers being active at the same time. 
