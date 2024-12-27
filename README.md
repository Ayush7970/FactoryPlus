# FactoryPlus - A Smart Conveyor Belt System

## Introduction
FactoryPlus is an innovative conveyor belt system designed to enhance safety and productivity in factory environments. Utilizing two Arduino boards, it integrates various sensors and output devices to monitor and control the conveyor belt operations effectively.


## Features
- **Safety Monitoring:** Uses ultrasonic, temperature and humidity sensors to detect potential hazards.
- **Productivity Enhancement:** Manages conveyor operations such as product counts and displays relevant information on an LCD.
- **Alert System:** Issues visual and auditory alerts through buzzers and LED lights to notify workers of potential safety issues.
- **Communication:** Utilizes I2C protocol for seamless data exchange between the two Arduino boards to coordinate safety and productivity features.

## Hardware Setup
- **Arduino Uno Boards** x 2
- **Ultrasonic Sensor**
- **Temperature and Humidity Sensor (DHT11)**
- **Servo Motors** x 2
- **LCD Screen**
- **Piezo Speaker**
- **LED Lights** x 5
- **Photoresistor**
- **Breadboards** x 2
- **Resistors, Jumper Wires, Power Adapters, USB Cables**

### Wiring and Connections
- **Arduino 1 Connections:**
  - Ultrasonic Sensor: Trig pin to pin 9, Echo pin to pin 8
  - LCD Screen: RS to pin 12, Enable to pin 11, D4 to pin 5, D5 to pin 4, D6 to pin 3, D7 to pin 2
  - Piezo Speaker: Buzzer pin to pin 7
  - I2C Communication: SDA and SCL connected to A4 and A5 respectively

- **Arduino 2 Connections:**
  - Servo Motors: Connected to pins 8 and 9
  - Temperature and Humidity Sensor: Data pin to pin 2
  - Photoresistor: Analog input pin to A1
  - LED Lights: Red LED to pin 7, Green LED to pin 6, White LEDs to pins 5, 4, and 3
  - I2C Communication: SDA and SCL connected to A4 and A5 respectively

## Software Development
The software integrates various modules using the following libraries:
- `LiquidCrystal.h` for the LCD
- `DHT.h` for reading temperature and humidity
- `Wire.h` for I2C communication

## User Guide
### Setup Instructions
Place the 2 Arduinos next to each other with the ultrasonic sensor facing the servo motors. Ensure the motors are positioned near the temperature and humidity sensor, maintaining a distance of about 4 cm to 10 cm between them.

### Operation
- **Arduino 1** monitors the environment for safety hazards.
- **Arduino 2** handles fire hazards and light levels, controlling the motors based on the data received.
- **I2C Communication** facilitates the sending of signals between devices for coordinated actions in response to detected hazards.

## Timeline of Development
- **Phase 1:** Setup and initial testing (10/28/24 - 11/01/24)
- **Phase 2:** Implementation and integration (11/04/24 - 11/29/24)
- **Phase 3:** Final adjustments and presentation (12/02/24 - 12/06/24)

## References
Detailed documentation and tutorials utilized for building and programming components are available here:
- [Arduino Official Documentation](https://www.arduino.cc)
- [I2C Communication Tutorial](https://www.arduino.cc/en/Tutorial/ArduinoMasterWriter)
- [Servo Motor Control with Arduino](https://www.arduino.cc/en/Reference/Servo)

For more information and troubleshooting, visit the Arduino forums and community support pages.
