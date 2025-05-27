# A-Eye: Assistant for the Visually Impaired

## Overview

Millions of visually impaired individuals struggle with daily tasks due to the lack of accessible technology that offers real-time awareness. **A-Eye** is a wearable smart assistant designed to support the blind by enabling scene understanding, recognizing familiar faces, and providing memory assistance through voice commands. With compact hardware and AI capabilities, A-Eye aims to enhance autonomy and confidence in everyday navigation and social interaction.

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Technologies Used](#technologies-used)
* [Project Structure](#project-structure)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

## Features

1. ### **Scene Reading**

   Captures surroundings and converts them to spoken descriptions using image recognition models.
   ![Scene Reading](https://github.com/user-attachments/assets/sample-scene.jpg)

2. ### **Face Recognition**

   Recognizes known individuals and announces their names to help in social interactions.
   ![Face Recognition](https://github.com/user-attachments/assets/sample-face.jpg)

3. ### **Voice Memory Recall**

   Users can store and retrieve spoken reminders or notes via simple voice commands.
   ![Voice Recall](https://github.com/user-attachments/assets/sample-voice.jpg)

4. ### **Compact Wearable**

   Chest-mounted hardware ensures proper alignment and consistent camera feed for accurate detection.
   ![Wearable](https://github.com/user-attachments/assets/sample-wearable.jpg)

## Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/username/a-eye.git
cd a-eye
```

### Step 2: Install Required Libraries

It's recommended to use a virtual environment:

```bash
python -m venv env
source env/bin/activate      # Mac/Linux
env\Scripts\activate         # Windows
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### Step 3: Flash ESP32-CAM

Install and flash the firmware to the ESP32-CAM using Arduino IDE or esptool.

```bash
esptool.py --chip esp32 --port COM3 write_flash -z 0x1000 firmware.bin
```

### Step 4: Connect Servo Motor

Connect servo motors to rotate the camera module (if applicable) and test using PWM control code.

## Usage

1. **Run the Python Backend** to launch scene and face recognition modules:

```bash
python main.py
```

2. **Use voice commands** to interact with the assistant:

```bash
"What's in front of me?"
"Who is this?"
"Remember this for later..."
```

3. **Power the Wearable Device** and ensure it’s mounted securely on the chest for optimal performance.

## Technologies Used

1. **Computer Vision**: OpenCV
2. **AI/Deep Learning**: TensorFlow
3. **Hardware**: ESP32-CAM, Servo Motor
4. **Programming Language**: Python
5. **Speech Processing**: pyttsx3, SpeechRecognition

## Project Structure

```
A-Eye/
├── esp32/                   # Firmware for ESP32-CAM
├── hardware/                # Chest-mount design files, wiring diagrams
├── models/                  # Pretrained models (scene, face recognition)
├── voice_assistant/         # Voice command interface
├── main.py                  # Main integration script
├── requirements.txt
└── README.md
```

## Contributors

* **Gokulan** – Memory recall - RAG and AI Model developer
* **Srikanth** – Module Integration, Hardware Development
* **Haresh** – Voice Module and Bot Conversation
* **Shyaam kumar** – Internal Navigation and Scene description
* **Sendhanee** – Face Recognition and Conversation Assistant
* **Nithian** – Computer Vision Analytics
