# 4WD Bluetooth Controlled Car
This project controls a 4-wheel drive car using an ESP32 microcontroller and a Bluetooth connection. The user can control the car's movement through commands sent via Bluetooth, using directions like forward, backward, left, and right. The car uses four motors and is capable of various driving maneuvers, including turning, moving diagonally, and stopping.

## Features
- Bluetooth control via ESP32
- 4-wheel drive system with independent motor control for each wheel
- Supports basic movement commands: forward, backward, left, right, and stop
- PWM control for motor speed adjustment
- Timeout for resetting the state if no signal is received

## Hardware Requirements
- ESP32 microcontroller
- Motor driver capable of controlling 4 motors
- Four DC motors
- Power source for motors and ESP32
- Bluetooth-enabled device (e.g., smartphone or tablet)

## Pin Configuration
The motor driver pins are connected as follows:


| Motor       |   IN1  Pin | IN2 Pin | PWM Pin | PWM Channel |
|-------------|------------|---------|---------|-------------|
| Back  Right |  4	       | 2	     | 22      | 4           |
| Back  Left	|  18        | 19      | 23      | 5           |
| Front Right |  27        | 26	     | 14      | 6           |
| Front Left	|  33        | 25      | 32      | 7           |

## Software Requirements
- Arduino IDE with ESP32 board support
- Bluetooth Serial library (BluetoothSerial.h)

## Installation
1. Download and install the Arduino IDE if you haven't already.
2. Install the ESP32 board support:
   - Open File > Preferences.
   - In the "Additional Boards Manager URLs" field, add:
       ```arduino
          https://dl.espressif.com/dl/package_esp32_index.json
       ```
   - Go to Tools > Board > Boards Manager and search for "esp32" and install.
3. Install the BluetoothSerial library.
4. Connect the hardware as per the pin configuration table.
5. Upload the code to your ESP32.

## How to Use
1. Power up the ESP32 and the motors.
2. Pair your Bluetooth-enabled device with the ESP32. The device name is 4WH Car.
3. Use a Bluetooth terminal app to send the following commands to control the car:
    - F: Move Forward
    - G: Move Backward
    - L: Turn Left
    - R: Turn Right
    - S: Stop

## Functionality Overview
- Forward(): Moves the car forward by rotating all wheels in the forward direction.
- Backward(): Moves the car backward by reversing the rotation of all wheels.
- Left(): Rotates the front-left and back-left motors in opposite directions for a left turn.
- Right(): Rotates the front-right and back-right motors in opposite directions for a right turn.
- Stop(): Stops all motors by setting their PWM speed to 0.

## Adjustments
You can modify the maximum motor speed by changing the value of MAX_MOTOR_SPEED defined in the code.

## Troubleshooting
- Make sure the correct COM port is selected in the Arduino IDE when uploading the sketch.
- Check motor connections and ensure the power supply is sufficient for all motors.

## Materials
- 2 acrylic plates
- 3 motors
- 4 black wheels
- 1 cable
- 1 battery
- 4 red cables
- 4 black cables
- 17 small screws
- 8 large screws
- 8 pieces of wood
- 6 transparent tubes
- 14 drill bits
- 1 Esp plate

# Contact
If you have any questions or suggestions, feel free to reach out!
[Linkedin](https://www.linkedin.com/in/gabriel-bessi-5b0160230/)
