# Proiect-InkTime
Design for a minimalist smartwatch optimized for month-class battery life and sunlight readability.


![Block Diagram](InkTime.drawio.png)

## Hardware Overview
### Microcontroller nRF52840
- It has a powerful ARM Cortex-M4 processor but uses very little electricity. It also has built-in Bluetooth 5.0.

### The Screen: E-Paper Display (EPD)
- Connection: Uses the SPI interface.
- E-Paper only uses power when the image changes.It is ideal for preserving battery. 

### The Motion Sensor: IMU (Accelerometer)
- Connection: Uses the I2C interface.
- It counts steps and detects when you lift your wrist to look at the watch. It can send a signal to wake up the processor only when it feels movement.

### Power Management
Battery: A small Lithium-Polymer (Li-Po) battery.
Charging: A dedicated chip (PMIC) handles safe charging via USB.Regulator
Regulator: 3.3V LDO ensures the electronics get a steady voltage even as the battery drains.