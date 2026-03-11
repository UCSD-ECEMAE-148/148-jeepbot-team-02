# System Schematic

This schematic shows the current high-level electrical and communication architecture of the Jeepbot platform.

## Main Components
- 24V lead acid battery
- Antispark switch
- Power distribution board (PDB)
- Five VESC controllers
- Raspberry Pi 5
- Radio receiver
- Powered USB hub
- Two OAK-D cameras
- GPS
- LIDAR
- Steering motor and absolute encoder

## Power Architecture
- The 24V battery feeds the antispark switch, which connects to the PDB.
- The PDB distributes power to the five VESCs.
- DC-DC converters step 24V down to 12V and 5V for lower-voltage components.
- The 12V rail powers the LIDAR.
- The 5V rail powers the Raspberry Pi 5, radio receiver, and powered USB hub.

## Motor Control
- VESC 1 through VESC 4 control the four drive motors:
  - Back Left
  - Back Right
  - Front Left
  - Front Right
- Each drive motor includes a hall encoder.
- VESC 5 controls the steering motor and receives feedback from the absolute encoder.

## Sensors and Peripherals
- Two OAK-D cameras and the GPS connect through the powered USB hub.
- The Raspberry Pi 5 acts as the main onboard compute platform.
- The radio receiver interfaces with the Raspberry Pi for control input.
- The LIDAR is powered through the 24V to 12V converter.

## Safety
- Emergency stop buttons are included in the signal chain for safety shutdown and control interruption.

## Communication
- CAN bus is used between the VESCs and related control hardware.
- Signal wiring connects motor encoders, the steering system, radio receiver, and emergency stop chain.
- Ethernet is used where required for higher-speed communication links.

## Notes
This schematic is intended as a high-level system overview and should be updated as the hardware integration evolves.
