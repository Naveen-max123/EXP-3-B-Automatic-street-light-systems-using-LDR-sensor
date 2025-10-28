# EXP-3-B-Automatic-street-light-systems-using-LDR-sensor

## Aim: 
To execute the -Automatic-street-light-systems-using-LDR-sensor  in tinkercad software
## Hardware / Software Tools required:
-PC/ Laptop with Internet connection
-Tinker CAD tool (Online)
-Arduino UNO 
-Board/ESP-32
-Photoresistor
  
## Schematic Diagram:
<img width="973" height="745" alt="image" src="https://github.com/user-attachments/assets/9cf45d55-ace8-4830-9d72-df48cd9fc3d2" />

## Circuit Diagram:

<img width="1151" height="697" alt="image" src="https://github.com/user-attachments/assets/57ec9b54-27b1-4094-8164-4df6074b0f86" />


## Theory :

 The Arduino Uno is powered by the ATmega328P, an 8-bit microcontroller that runs at 16 MHz. It has 32 KB of flash memory, 2 KB of SRAM, and 1 KB of EEPROM. The board has 14 digital I/O pins (of which 6 can be used as PWM outputs) and 6 analog input pins. These pins allow the board to interface with various sensors, actuators, and other devices.The Arduino Uno can be powered via a USB connection or an external power supply. The board has a built-in voltage regulator to manage power from 7 to 12 volts.
The board is programmable using the Arduino IDE (Integrated Development Environment), which supports a simplified version of C/C++. The code, known as a "sketch," is uploaded to the board via a USB connection. The Uno has a USB-B port, which is used for communication with a computer. The USB connection also powers the board when connected. The board includes a reset button that restarts the microcontroller, useful during programming and troubleshooting. The In-Circuit Serial Programming (ICSP) header allows for low-level programming of the microcontroller or firmware updates. The Uno has a built-in LED on pin 13, commonly used for simple tests and debugging.

## Procedure:

### Step 1: 
Set Up the Tinkercad Environment
•	Log in to Tinkercad: Open Tinkercad in your web browser and log in to your account.
•	Create a New Circuit: In the Tinkercad dashboard, click on "Circuits" and then select "Create New Circuit."
### Step 2: 

Add Components to the Circuit
•	Arduino Uno: Drag an Arduino Uno board from the components panel onto the workspace.
•	LDR Sensor: Search for the Photoresistor in the components panel and drag it into the workspace.
•	Breadboard: Drag a small breadboard to the workspace to help with wiring connections.
•	Resistor (Optional): A resistor may not be necessary for this simple setup, but you can include it for more accurate readings.
•	Wires: Use wires to connect the components.

### Step 3: 
Connect the LDR Sensor to the Arduino
•	LDR Sensor Pins: The LDR has two terminals (pins).
•	One LDR Pin to 5V: Connect one terminal of the LDR to the Arduino 5V pin.
•	Other LDR Pin to Analog Input and Resistor:
o	Connect the other terminal of the LDR to one end of a fixed resistor (e.g., 10kΩ).
o	Also connect this same LDR terminal to an Arduino analog input pin (e.g., A1).
•	Resistor to GND: Connect the other end of the resistor to the Arduino GND pin.
•	Breadboard Setup (Optional):
o	Place the LDR and resistor on the breadboard forming a voltage divider between 5V and GND.
o	The middle point (between LDR and resistor) connects to the Arduino analog input pin.

### Step 4: Write the Arduino Code

•	Code Editor: Click on the "Code" button at the top of the Tinkercad workspace to open the code editor.
•	Set the Coding Mode: Ensure the editor is in "Text" mode to write your code in C/C++.
•	Enter the Code: Write the following code from the photoresistor

### Step 5: Simulate the Circuit

•	Start Simulation: Click the "Start Simulation" button at the top of the workspace to run the circuit and code.
•	Monitor Output: Open the serial monitor by clicking the "Serial Monitor" button to view the temperature readings in both Celsius and Fahrenheit.

### Step 6: Troubleshoot and Refine
•	Check Connections: Ensure that all connections are made correctly on the breadboard and the Arduino.
•	Adjust Code: If needed, tweak the code to improve accuracy or change the format of the output.

### Step 7: Save Your Work
•	Stop Simulation: Click "Stop Simulation" to end the simulation.
•	Save the Circuit: Click "Save" to keep your circuit design and code for future use.

## Code:
```
// Pins for LEDs
int led1 = 2;
int led2 = 3;
int led3 = 4;

// LDR pin
int ldrPin = A0;
int ldrValue = 0; // store sensor reading

// Light threshold (adjust based on your room light)
int thresholdValue = 500;

void setup() {
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  Serial.begin(9600); // For debugging
}

void loop() {
  ldrValue = analogRead(ldrPin); // read LDR value
  Serial.println(ldrValue); // check the value in Serial Monitor

  if (ldrValue < thresholdValue) {
    // It's dark → turn ON lights
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
  } else {
    // It's bright → turn OFF lights
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
  }

  delay(200); // small delay for stability
}

```


## Output:

https://github.com/user-attachments/assets/83de2366-077d-4582-ba46-67574b92a16d

## Result:
Automatic-street-light-systems-using-LDR-sensor using tinkercad is successfully executed.

