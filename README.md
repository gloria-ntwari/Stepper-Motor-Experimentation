# Stepper Motor Control with Arduino

This project controls a **28BYJ-48 stepper motor** using a **ULN2003 driver board** and **Arduino**.  
The motor rotates to a specific angle (in degrees) entered via the Serial Monitor, e.g. `rotate 90` or `rotate -180`.

## 🧩 Components
- Arduino Uno or Nano  
- 28BYJ-48 Stepper Motor  
- ULN2003 Driver Board  
- Jumper Wires  
- USB Cable  

## ⚙️ Connections
| ULN2003 Pin | Arduino Pin |
|--------------|-------------|
| IN1 | 8 |
| IN2 | 10 |
| IN3 | 9 |
| IN4 | 11 |
| VCC | 5V |
| GND | GND |

## 💻 How It Works
- Uses the `Stepper.h` library to control the motor.  
- Accepts commands through Serial Monitor (e.g., `rotate 90`).  
- Converts degrees to motor steps using:  steps = (angle / 360) * 2048
- Rotates clockwise for positive angles, counterclockwise for negative angles