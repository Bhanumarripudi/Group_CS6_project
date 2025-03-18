## 🎯 **System Design**

### 🔥 **1. System Architecture**
The project is designed using a **modular architecture** consisting of the following key components:  

- **Transmitter Module:**  
  - Captures EMG signals using **EMG sensors** placed on the forearm.  
  - Detects hand orientation using the **MPU6050 sensor**.  
  - Processes and transmits gesture data wirelessly via **ESP8266 Wi-Fi module**.  

- **Receiver Module:**  
  - Receives gesture data through **Wi-Fi communication**.  
  - Controls the robot's movements by sending signals to the **motor driver**.  
  - Executes corresponding robot actions (e.g., forward, backward, left, right).  

- **Signal Processing and Classification:**  
  - Applies **band-pass and notch filters** to remove noise from EMG signals.  
  - Uses a **CNN model** to classify gestures with **>92% accuracy**.  
  - Sends classified gesture commands to the robot.  

---

### ⚙️ **2. Block Diagram**


![image](https://github.com/user-attachments/assets/d411230d-1ad9-4076-9144-fcf4a83af5d6)


✅ **Explanation:**  
- The **EMG sensors** and **MPU6050** capture hand movements and send data to the ESP8266 transmitter.  
- The **Wi-Fi communication** ensures real-time, low-latency data transfer.  
- The receiver interprets the classified gesture commands and controls the robot movements.  

---

### 🔧 **3. Hardware Design**
The **hardware setup** includes the following components:
- **EMG Sensors:** To capture muscle activity signals during hand gestures.  
- **MPU6050 Sensor:** To detect hand orientation and improve gesture accuracy.  
- **ESP8266 Wi-Fi Module:** To wirelessly transmit gesture data.  
- **Motor Driver (L298N or similar):** To control the robot’s motors based on classified gestures.  
- **DC Motors:** For robot movement execution.  
- **Power Source:** Rechargeable battery or power adapter for continuous operation.  

---

### 🛠️ **4. Software Design**
The **software architecture** consists of the following key elements:
- **Signal Acquisition:**  
  - Reads EMG signals from sensors.  
  - Captures hand orientation data using MPU6050.  
- **Signal Pre-processing:**  
  - Applies **band-pass and notch filters** to reduce noise.  
  - Extracts meaningful features for gesture classification.  
- **Gesture Classification:**  
  - Uses a **CNN model** to classify hand gestures with high accuracy.  
- **Robot Control:**  
  - Transmits gesture commands via **Wi-Fi**.  
  - Controls robot movements through the **motor driver**.  





