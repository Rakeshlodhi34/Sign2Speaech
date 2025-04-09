🤖 Sign2Speech - Smart Glove for Speech & Hearing Impaired
The Gesture Vocalizer is an assistive technology device designed to bridge the communication gap between speech- and hearing-impaired individuals and those who do not understand sign language. The glove-based system interprets hand gestures and translates them into audible speech using flex sensors, an accelerometer, and a speech synthesizer.

📷 Project Preview

🧠 Project Description
People with speech and hearing impairments often face challenges communicating with others, especially those who do not understand sign language. The Gesture Vocalizer project offers a solution by translating hand gestures (made using sign language) into voice and text output, enabling smoother communication.

This glove-based device reads gestures through flex sensors (mounted on fingers) and an accelerometer (MPU6050) to capture finger bends and hand movements, respectively. The readings are processed by an ATmega328p microcontroller (Arduino Uno), and the interpreted gesture is sent over Bluetooth and converted into audio/text output using a speech synthesizer.

🔧 Components Used
Component	Description
Flex Sensors (x4)	Measures bending of each finger
MPU6050 Accelerometer	Detects motion and orientation of the hand
Arduino Uno (ATmega328p)	Core processing unit for reading sensor data
Bluetooth Module (HC-05)	Sends data to external devices (phone/laptop)
Breadboard & Jump Wires	For circuit prototyping and connections
Glove	Base for mounting sensors
Speech Synthesizer	Converts text data into audio signals (external)
⚙️ Working Principle
Flex Sensors detect the degree of bending in each finger.

MPU6050 detects acceleration and gyroscope data (hand movement and tilt).

Arduino Uno processes sensor readings and compares them to preset gesture patterns.

When a gesture matches a predefined condition, a corresponding message is sent over Bluetooth.

The message is converted to audio using a text-to-speech system (e.g., mobile app, PC, or external module).

💬 Recognized Gestures and Outputs
Flex Sensor Pattern	Output Message
All flex values low	"Welcome Advitya 2022"
Flex3 > 30 only	"" (reset/neutral)
Flex2 > 40	"You are beautiful"
Flex2 & Flex3 > 30	"Call police"
Flex1 > 40	"God Bless you"
Flex1 & Flex2 > 30	"This is a gesture vocalizer"
Flex1, Flex2, Flex3 > 30	"I have a doubt"
Flex0 > 30	"Have a nice day!"
Flex0 & Flex3 > 50	"I am hungry!"
Flex0 & Flex1 > 50	"Good Afternoon, Madam"
Flex0, Flex1, Flex2 > 50	"I need to pee"
Flex2 & Flex3 > 50	"Very Good"
All flex > 40	"Help me!"
📂 Code Overview
Reads values from 4 analog flex sensors (A0 to A3)

Initializes MPU6050 for motion sensing

Compares sensor values with pre-defined gesture thresholds

Sends corresponding message via Bluetooth using SoftwareSerial

Monitors MPU6050 for motion events and prints acceleration/gyro data to serial monitor

📦 Installation & Setup
Prerequisites
Arduino IDE

Libraries:

Adafruit_MPU6050

Adafruit_Sensor

Wire

SoftwareSerial

Steps
Connect all hardware components as shown in the image.

Upload the code to Arduino Uno using the Arduino IDE.

Pair Bluetooth module with mobile/PC.

Open a serial terminal or mobile app to receive Bluetooth messages.

Wear the glove and perform gestures to trigger vocal outputs.

📊 Future Enhancements
Add more sensors for better gesture resolution

Integrate display (OLED/LCD) for visual feedback

Use machine learning to recognize a wider range of gestures

Add audio playback directly using speaker and voice module (e.g., DFPlayer Mini)

📚 References
Adafruit MPU6050 Library

Arduino Documentation

Research on gesture recognition and assistive technologies

👨‍💻 Author
Rakesh Lodhi
Electronics and Communication Engineering
VIT Bhopal


![gesturevoc02](https://user-images.githubusercontent.com/68192323/167282485-f7b298f6-8a5d-4ada-a908-8bbc81e1da39.jpeg)
