## RFID & Biometric Access Control System using ESP32

##  Description

This project presents a smart access control system based on **RFID technology** and **biometric fingerprint authentication**, powered by the ESP32 microcontroller.

The system allows only authorized users to access a secured area (door, room, etc.) using either an RFID badge or a fingerprint. Unauthorized attempts are automatically rejected.

In addition, a web-based interface enables remote user management and real-time access control.

---

##  System Architecture

The system is composed of the following main components:

* ESP32 (main controller)
* RC522 RFID reader
* Fingerprint sensor (R307)
* Servo motor (door control)
* LCD I2C display
* LEDs and buzzer (status indication)
* Web server (Flask API)

---

##  Features

*  RFID authentication (badge scanning)
*  Fingerprint authentication
*  Real-time access verification via web server
*  Remote user management (add / delete users)
*  Access restriction based on time (HORS_HORAIRE)
*  Visual and sound feedback (LCD, LEDs, buzzer)
*  Multiple operating modes (Normal / Enroll / Delete)

---

##  System Workflow

1. User scans RFID card or fingerprint
2. ESP32 reads the data
3. Data is sent to the web server (Flask API)
4. Server verifies user authorization
5. System response:

   *  Access granted → door opens
   *  Access denied → alert activated

---

##  Web API Endpoints

* `/api/verifier-carte` → Verify access
* `/api/nouvel-id` → Add new user
* `/api/mode` → Change system mode

---

##  Technologies Used

* Embedded C (Arduino IDE)
* Wi-Fi communication (ESP32)
* Python (Flask)
* HTML / CSS / JavaScript
* I2C, SPI, UART protocols

---

##  Demo Video

Scan the QR Code below or click the link to watch the system demonstration:

 https://drive.google.com/file/d/1DjmF38GSk3lGj5qkXHx3o4N-LQEZYQmE/view

---

##  Project Preview

<img width="1600" height="1200" alt="IMG-20260505-WA0005" src="https://github.com/user-attachments/assets/f969932c-480a-4785-b0e1-aebf93b0221c" />


---

##  Installation

1. Clone the repository
2. Open the project in Arduino IDE
3. Install required libraries:

   * MFRC522
   * ESP32Servo
   * Adafruit Fingerprint
   * LiquidCrystal I2C
4. Upload code to ESP32
5. Run the Flask server

---

##  Security Notes

* Ensure proper power supply (3.3V for RC522)
* Protect API endpoints for production use
* Consider using HTTPS for secure communication

---

##  Future Improvements

* Mobile application integration
* Cloud database
* Face recognition
* Advanced logging system

---

##  Author

* ABDELJAWAD EL-MANSOURY

---

##  License

This project is for educational purposes.
