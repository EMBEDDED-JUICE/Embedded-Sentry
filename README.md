# Embedded Sentry 🔐
Gesture-Controlled Lock/Unlock System Using IMU

## 📌 Overview
**Embedded Sentry** is an embedded-systems project that transforms a development board’s built-in accelerometer/gyro (IMU) into a **gesture-based locking mechanism**.  
Users can record a unique hand-gesture sequence as a “key” and then reproduce it to unlock the system. The design emphasizes **security, ease of use, and robustness** — providing a simple alternative to PIN codes or physical keys.

This project was developed as part of the **Embedded Challenge – Fall 2024** course assignment.

---

## ✨ Features
- **Gesture-based authentication:** Record and reproduce hand motions to unlock.
- **On-board storage:** Saves the recorded gesture sequence on the microcontroller.
- **Real-time feedback:**  
  - LCD prompts guide the user during record/unlock.  
  - **Green LED** → unlock successful.  
  - **Red LED** → unlock failed.  
- **User button:** Clears stored gestures.
- **Cross-platform build:** Developed with [PlatformIO](https://platformio.org/) for consistency.

---

## 🗂 Project Structure
```
Embedded Sentry/
├── include/              # Header files
│   └── README
├── lib/                  # External libraries
│   └── README
├── src/                  # Main source code
│   ├── drivers/
│   ├── gyro.cpp
│   ├── gyro.h
│   ├── main.cpp
│   └── serial_dump.py
├── test/                 # Test scripts & docs
│   ├── README
│   └── README.md
├── mbed_app.json         # mbedOS configuration
└── platformio.ini        # Build configuration
```

---

## ⚙️ Hardware & Software Requirements
- Development board with **built-in accelerometer/gyro** (IMU)
- On-board **LCD display** and **LED indicators (red, green)**
- **User button** (blue) for clearing recorded keys
- **PlatformIO** IDE or CLI installed on your host machine
- USB cable for flashing firmware

---

## 🚀 How to Build & Run
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/embedded-sentry.git
   cd embedded-sentry
   ```
2. **Open in PlatformIO** (or use CLI)
   ```bash
   pio run
   pio run --target upload
   ```
3. **Connect the board** via USB and upload the firmware.
4. **Power-cycle/reset** the board to start the application.

---

## 🕹️ How to Use
1. After startup, the LCD shows **“Record”** and **“Unlock”** buttons.
2. **Record a Gesture Key**
   - Tap **“Record”** on the LCD.  
   - Follow on-screen prompts.  
   - When **“Recording…”** appears at the bottom, perform the intended hand gesture **within 5 seconds**.
3. **Unlock with Gesture**
   - Tap **“Unlock”** on the LCD.  
   - Follow prompts until **“Recording…”** appears again.  
   - Perform the **same gesture** to unlock the device.
4. **Feedback**
   - ✅ Green LED → unlock successful  
   - ❌ Red LED → unlock failed
5. **Clear Stored Gesture**
   - Press the **blue user button** to erase all recorded keys.

---

## 📁 Key Files
- `src/main.cpp` – Application entry point.
- `src/gyro.cpp` / `gyro.h` – Handles IMU data acquisition and processing.
- `src/serial_dump.py` – Optional Python tool for serial data logging/debugging.
- `platformio.ini` – Build environment settings.
- `mbed_app.json` – mbed-OS runtime configuration.

---

## 🧪 Testing
Test scripts and notes can be found in the **`/test`** folder.  
For debugging IMU readings, use `serial_dump.py` with a connected serial terminal.

---

## 🏆 Project Context
Developed as part of the **Embedded Challenge – Fall 2024 Term Project**, focusing on:
- Reliable gesture recording/unlocking
- Robust tolerance handling
- User-friendly feedback system

---

## 👥 Contributors
- **Naveen Kumar Senthil Kumar** – [ns6503@nyu.edu](mailto:ns6503@nyu.edu)  

---

