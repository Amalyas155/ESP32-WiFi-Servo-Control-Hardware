# 🔌 ESP32 WiFi Servo Control — Hardware Implementation

## 📌 Project Overview

This project demonstrates how to control an SG90 Servo Motor using a real ESP32 board through a simple web interface.

The ESP32 creates its own WiFi Access Point. After connecting to the ESP32 network, the user can open a control page containing **Open** and **Close** buttons.

No internet connection is required to control the Servo Motor.

## ✨ Features

* 📶 Creates a local WiFi Access Point.
* 🌐 Provides a simple web control page.
* 🔓 Open button moves the Servo Motor to 90°.
* 🔒 Close button returns the Servo Motor to 0°.
* 🔵 Uses the built-in blue LED as an Open indicator.
* 📱 Can be controlled using a phone or computer.
* ⚡ Implemented and tested using real hardware.

## 🧰 Components

* ESP32 Board
* SG90 Servo Motor
* Male-to-Male jumper wires
* USB data cable
* Built-in blue LED on the ESP32

## 🔧 Hardware Wiring

| Servo Wire  | ESP32 Connection | Function             |
| ----------- | ---------------- | -------------------- |
| Red wire    | VCC              | Servo power          |
| Brown wire  | GND              | Ground               |
| Orange wire | IO18             | Servo control signal |

The built-in blue LED uses `GPIO 2`, so it does not require any external wiring.

> ⚠️ Disconnect the USB cable before connecting or changing any wires.

## ⚙️ How It Works

1. The ESP32 creates a WiFi network named `ESP32-Servo`.
2. The user connects a phone or computer to the ESP32 network.
3. The user opens `http://192.168.4.1` in a browser.
4. The ESP32 displays a web page with Open and Close buttons.
5. Pressing **Open** moves the Servo Motor to 90° and turns on the blue LED.
6. Pressing **Close** returns the Servo Motor to 0° and turns off the blue LED.

## 📶 WiFi Information

| Setting   | Value                |
| --------- | -------------------- |
| WiFi Name | `ESP32-Servo`        |
| Password  | `12345678`           |
| Web Page  | `http://192.168.4.1` |

> The ESP32 network does not provide internet access. If the phone displays **No Internet**, choose to remain connected.

## 💻 Software and Libraries

The project was programmed using the Arduino IDE.

### Required Libraries

* `WiFi.h`
* `WebServer.h`
* `ESP32Servo.h`

The `WiFi` and `WebServer` libraries are included with the ESP32 board package.

The `ESP32Servo` library can be installed from:

`Arduino IDE → Sketch → Include Library → Manage Libraries`

## ⬆️ Uploading the Code

1. Disconnect the Servo Motor from the ESP32.
2. Connect the ESP32 to the computer using a USB data cable.
3. Open the project code in the Arduino IDE.
4. Select `ESP32 Dev Module` from the Boards menu.
5. Select the correct COM port.
6. Set the Upload Speed to `115200`.
7. Click the Upload button.
8. Wait until `Done uploading` appears.
9. Disconnect the USB cable.
10. Connect the Servo Motor to `VCC`, `GND`, and `IO18`.
11. Reconnect the USB cable.

## ▶️ Running the Project

1. Power the ESP32 using the USB cable.
2. Open the WiFi settings on the phone or computer.
3. Connect to the `ESP32-Servo` network.
4. Enter the password `12345678`.
5. Open a web browser.
6. Enter `http://192.168.4.1`.
7. Press Open or Close to control the Servo Motor.

## 🎥 Real Hardware Run

Here we show the project running using the real ESP32 board and SG90 Servo Motor.





https://github.com/user-attachments/assets/5cf5f61d-e504-41b4-97b1-ea60df4deb52




## 📁 Repository Files

* `sketch.ino` — ESP32 source code.
* `README.md` — Project documentation.
* Project demonstration video.

## ✅ Project Result

The project was successfully implemented and tested using a real ESP32 board.

The ESP32 successfully created a local WiFi network, displayed the control web page, and controlled the Servo Motor using the Open and Close buttons.

---

### 👩‍💻 Developed by Amal Yasser
