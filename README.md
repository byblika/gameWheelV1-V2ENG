# Game Wheel — controlling potentiometers via Arduino as a gaming wheel

This project allows you to use potentiometers as steering, throttle, brake, and clutch, creating a full-featured DIY controller for games. Works through Arduino and VJoy emulation.

## 🎛️ Wiring potentiometers to Arduino

| Element        | Arduino | Function     |
|----------------|---------|--------------|
| `xValue`       | A0      | Steering     |
| `yValue`       | A1      | Throttle     |
| `zValue`       | A2      | Brake        |
| `sliderValue`  | A3      | Clutch       |
| `VCC`          | 5V      | Power        |
| `GND`          | GND     | Ground       |

---

## 🚀 How to run

### 1. Arduino
- Open `arduino.ino` in **Arduino IDE**.
- Upload the code to the board (e.g., Arduino Uno).

### 2. VJoy Setup
- Download and install **VJoy**.
- Open **VJoy Config** → click **"Add Device"**.
- Enable checkboxes: **X**, **Y**, **Z**, **Slider**.
- In the **"Number of Buttons"** field, set the value to `3`.

### 3. Python scripts (on PC)

#### 📌 Before launching:
- Install the required libraries:
  ```bash
  pip install pyserial pyvjoy tkinter

Variant 1: joyv1.py

Open the file in an editor.

Manually enter your Arduino COM port in the code.

Run the script.

Variant 2: joyv2.py

Launch the program.

Select the Arduino COM port via the graphical interface (Tkinter).

🕹️ Possible use cases

Game steering simulation.

Gamepad alternative.

DIY controller for robots, cars, flight simulators, etc.

📌 Notes

If you're using Linux, the COM port will look something like /dev/ttyUSB0.

If it doesn't work — check the VJoy driver and admin rights.

Can be adapted for games like Euro Truck Simulator, BeamNG, Assetto Corsa, etc.

👨‍💻 Author

Bublika© (2025)
Project created as a DIY alternative to expensive wheels.
