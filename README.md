# 📡 RFID Attendance System with Live Excel (Google Sheets) Integration

**An IoT-based smart attendance system that uses RFID technology to automatically record attendance and store it in real-time on Google Sheets (Excel format) with LCD feedback and buzzer alerts.**

---

## 1. Project Title & Tagline

A smart RFID-based attendance system that captures user data from RFID cards and logs attendance live into Google Sheets using WiFi-enabled microcontroller.

---

## 2. Problem Statement

Traditional attendance systems are manual, time-consuming, and prone to errors such as proxy attendance and incorrect records.

This project solves these issues by:
- Automating attendance using RFID cards
- Storing data in real-time on Google Sheets
- Providing instant feedback via LCD and buzzer

It ensures **accuracy, efficiency, and real-time monitoring**.

---

## 3. Features

| Feature                     | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| RFID-Based Attendance      | Scan RFID cards to mark attendance instantly                               |
| Live Google Sheets Logging | Attendance data stored in real-time (Excel format)                          |
| LCD Display                | Displays user name and system messages                                      |
| Buzzer Alert               | Audio feedback on successful scan                                           |
| WiFi Connectivity          | Sends data to cloud using ESP8266                                           |
| Unique User Identification | Reads stored data from RFID tags                                            |
| Secure Data Handling       | Uses HTTPS requests for data transfer                                       |
| Easy Setup                 | Simple hardware and software integration                                    |

---

## 4. Tech Stack

### Hardware
- ESP8266 (NodeMCU)
- MFRC522 RFID Reader
- RFID Tags/Cards
- LCD Display (I2C)
- Buzzer

### Software
- Arduino IDE (C++)
- Google Apps Script (for Sheets integration)

### Libraries Used
- SPI.h
- MFRC522.h
- ESP8266WiFi.h
- ESP8266HTTPClient.h
- WiFiClientSecureBearSSL.h
- LiquidCrystal_I2C.h

---

## 5. Project Structure

```

RFID-Attendance-System/
│
├── write_rfid.ino        # Store user name into RFID tag
├── attendance_system.ino # Main attendance system
├── README.md

````

---

## 6. Installation & Setup

### 1️⃣ Hardware Connections

- RFID RC522 → ESP8266 (SPI pins)
- LCD → I2C (SDA, SCL)
- Buzzer → Digital Pin (D8)

---

### 2️⃣ Install Required Libraries

In Arduino IDE:
- MFRC522
- ESP8266WiFi
- ESP8266HTTPClient
- LiquidCrystal_I2C

---

### 3️⃣ Configure WiFi

Update in code:

```cpp
#define WIFI_SSID "your_wifi_name"
#define WIFI_PASSWORD "your_wifi_password"
````

---

### 4️⃣ Setup Google Sheets Integration

1. Create a Google Sheet
2. Open Apps Script
3. Deploy Web App
4. Copy Web App URL

Update in code:

```cpp
const String sheet_url = "your_google_script_url";
```

---

### 5️⃣ Upload Code

* Upload `write_rfid.ino` → Write name into RFID card
* Upload `attendance_system.ino` → Run main system

---

## 7. How It Works

### 1. RFID Data Writing

1. User name is written into RFID tag
2. Stored in memory block
3. Each card becomes unique identifier

---

### 2. Attendance Process

1. User scans RFID card
2. System reads stored name
3. LCD displays: "Hey [Name]"
4. Buzzer gives confirmation sound

---

### 3. Cloud Data Logging

1. ESP8266 connects to WiFi
2. Sends HTTP request to Google Script
3. Data is stored in Google Sheets
4. Sheet updates instantly (live Excel)

---

## 8. Scalability

* Can support multiple users with unique RFID cards
* Can be extended to:

  * Cloud databases (Firebase, MySQL)
  * Web dashboards
* Suitable for:

  * Schools
  * Colleges
  * Offices

---

## 9. Feasibility

* Low-cost hardware components
* Easy to build and deploy
* Requires minimal maintenance
* Works in real-time with internet connection

---

## 10. Novelty

This system combines:

* RFID automation
* IoT (ESP8266 WiFi)
* Cloud integration (Google Sheets)

It creates a **real-time attendance system without manual intervention**.

---

## 11. Feature Depth

* Reads RFID memory blocks securely
* Uses HTTPS for secure communication
* Handles:

  * Authentication failures
  * Connection errors
  * Invalid scans
* Provides instant user feedback via LCD + buzzer

---

## 12. Ethical Use & Disclaimer

* No personal data is shared without consent
* Data is stored only for attendance purposes
* Users must authorize Google Sheet access
* Designed for educational and institutional use

---

## 13. License

This project is for educational and learning purposes.

---

## 14. Author

**Sanjay**
📧 [your-email@sanjaypriyan0987@gmail.com]
🔗 [https://github.com/sanjay-ux391]

---
