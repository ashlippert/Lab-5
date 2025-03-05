# Lab 5: The Brain - Microcontrollers

**Authors:**

Ashlyn Lippert and Seth Daniel

**Date:**

March 4th, 2025

## Introduction
   This lab explores the fundamentals of microcontrollers using the Arduino platform. The Arduino system, consisting of both hardware and software, allows for programming and control of various electronic components. The Arduino IDE is used to compile and upload code to a RedBoard microcontroller from the SparkFun inventor’s kit. The primary objective is to control an LED using pulse width modulation (PWM), which enables digital signals to mimic analog behavior by adjusting the duty cycle of an output signal. Additionally, a photoresistor, a sensor that changes resistance based on light exposure, will influence the LED’s behavior. This experiment provides hands-on experience in microcontroller programming, circuit design, and the practical application of PWM for analog signal simulation.

## Materials
1. Resistors: 330 Ω, 10 kΩ
2. Fluke 87 V DMM
3. Computer running Arduino IDE
4. Additional wires
5. Oscilloscope
6. Photoresistor
7. A 10 kΩ trimmer potentiometer
8. Flathead screwdriver
9. RedBoard
10. LED

## Assembly Methods
**Objective 1: Blinking an LED**

1. **LED Circuit Assembly**

   To begin, mount the RedBoard and breadboard onto the SparkFun base, then connect the RedBoard to a computer running the Arduino IDE. In the IDE, select the Arduino UNO board and the appropriate COM port. Next, connect a 330Ω resistor and an LED in series to pin 13 on the RedBoard, ensuring a proper ground connection. Figure 1 below shows the schematic for the RedBoard.

<div align= "center">
<img src="" alt "Schematic 1" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 1: LED circuit schematic. </figcaption>
</div>

<br>

   Once assembled, the RedBoard circuit created using schematic 1 should resemble what is shown in Figure 2 below.
   
<div align= "center">
<img src="" alt "Assembled LED circuit" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 2: Constructed LED circuit from Schematic 1. </figcaption>
</div>
<br>

**Objective 2: Controlling an LED with a Potentiometer**

**Potentiometer Controlled Circuit Assembly**

   Connect the potentiometer to 5V and Ground, with the variable resistance pin connected to A0. Keep the previous circuit intact while integrating the potentiometer into the setup. The schematic for this setup is given in Figure 3 below.

<div align="center">
<img src="" alt="Schematic 2" width="400">
<br/>

<figcaption style="font-size: 16px; text-align: center;"> Figure 3: Potentiometer controlled LED circuit schematic. </figcaption>
</div>   

<br/>
  Once assembled, the circuit should look resemble Figure 4 below.

   <div align="center">
  <img src="" alt="Assembled potentiometer controlled LED circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 4: Constructed potentiometer controlled LED circuit from Figure 3. </figcaption>
</div>
<br>

**Objective 3: Controlling an LED with a Photoresistor**

**Photoresistor Controlled Circuit Assembly**

  Replace the potentiometer in the previous circuit with a series circuit consisting of a photoresistor and a 10 kΩ resistor. Connect 5V to the photoresistor, Ground to the resistor, and A0 to the node between them. The schematic for this circuit is provided in Figure 5 below.

 <div align="center">
  <img src="" alt="Schematic 3" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 5: Photoresistor controlled LED circuit schematic. </figcaption>
</div>
<br>

   Once assembled, the RedBoard circuit should resemble what is shown in Figure 6 below.
   
<div align="center">
  <img src="" alt="Assembled photoresistor controlled LED circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 6: Constructed photoresistor controlled LED circuit. </figcaption>
</div>
<br>

**Part 4: LED Dimmer Using PWM**
   Return to the circuit used in Part 2 with the potentiometer. Change the LED pin to one that is PWM capable (Pin 10 was used for our circuit).

<div align="center">
  <img src="" alt="Assembled photoresistor dimmer controlled LED circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 7: Constructed photoresistor dimmer controlled LED circuit. </figcaption>
</div>
<br>

## Test Equipment

1. Fluke 87 V DMM
2. Computer with Arduino IDE
3. Oscilloscope
   
   
## Test Procedures

**Resistor Measurement**

   For this part of the experiment, the resistance each resistor was measured using a Digital Multimeter (DMM) and the results were compared to the expected values based on the resistor color codes. We recorded the expected resistance, the acceptable tolerance range, and the measured resistance in a table. Any resistors that fell outside the expected range were noted. The technique used for resistor measurement is shown in Figure 7 below.

 <div align="center">
  <img src="https://github.com/user-attachments/assets/fd70fd10-4528-41e1-9a64-bf901897e7e4" alt="Assembled differentiating op amp circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 7: Measuring Resistor Values. </figcaption>
</div>
<br>


**Part 1: Blinking an LED**
   
   Upload the Blink program (File > Examples > Basics > Blink) to the Arduino and verify that the LED blinks. Adjust the delay in the program to decrease the blinking speed until the LED appears to remain constantly illuminated. Figure 8 shows the ON LED.

<br>
<div align= "center">
<img src="" alt "LED Blink" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 8: Blinking LED Circuit with LED on. </figcaption>
</div>

<br>

   The code used for this portion of the lab is provided below:


**Part 2: Potentiometer Controlled Circuit**

   Upload the Analog Read Serial program (Examples > Basics > AnalogReadSerial) to the Arduino and open the serial monitor (Tools > Serial Monitor), ensuring the baud rate is set to 9600 bps. Adjust the potentiometer and observe the serial output. Modify the code to control the LED’s blinking time based on the potentiometer’s input, demonstrating how analog inputs can be converted into digital signals.

   The code used for this section of the lab is provided below:


**Part 3: Photoresistor Controlled Circuit**
   Run the same program from the previous section and observe how different lighting conditions affect the analog values. Implement an if-else statement to turn on the LED only when the brightness sensed by the photoresistor is low. Experiment with blocking the light source and analyze the circuit’s response time by observing whether the LED turns on and off immediately.

   The code used for this portion of the lab is provided below:

**Part 4: LED Dimmer Using PWM**
   Read the voltage from the potentiometer and map the voltage value,from 0 to 1023, to a value from 0 to 255 using the function map(value, fromLow, fromHigh, toLow, toHigh). Write the mapped
value to the LED pin using the function analogWrite(pin, mappedvalue).

## Test Results:

**Table 1: Resistor Values**

| Resistor # | Expected Resistance (Ohms) | Tolerance | Max Value (Ohms) | Min Value (Ohms) | Measured Resistance (Ohms) |
|------------|----------------------------|-----------|------------------|------------------|----------------------------|
| 1          | 330                        | 5%        | 346.5            | 313.5            | 325                        |
| 2          | 1000                       | 5%        | 1050             | 950              | 990                        |

**Table 2: LED Blinking Delay**

|               | Delay Setting | Blinking? |
|---------------|---------------|-----------|
| Original      | 1000          | Yes       |
| -14           | 500           | Yes       |
| -12           | 200           | Yes       |
| -5            | 100           | Yes       |
| 0             | 50            | Yes       |
| 5             | 30            | Yes       |
| 12            | 15            | Yes       |
| 14            | 10            | No        |

**Arduino IDE Code**
**Part 1: Blinking an LED**
<br/>

*Script: blink_arduino*
<br/>
// the setup function runs once when you press reset or power the board
<br>
void setup() {
<br>
  pinMode(LED_BUILTIN, OUTPUT);        // initialize digital pin LED_BUILTIN as an output.
  <br>
}
<br/>

// the loop function runs over and over again forever
<br>
void loop() {
<br>
  digitalWrite(LED_BUILTIN, HIGH);     // turn the LED on (HIGH is the voltage level) 
  <br>
  delay(10);                           // wait for a second
  <br>
  digitalWrite(LED_BUILTIN, LOW);      // turn the LED off by making the voltage LOW
  <br>
  delay(10);                           // wait for a second
  <br>
}
<br/>

**Part 2: Potentiometer Controlled Circuit**
<br>
*Script: AnalogReadSerial_Arduino_BlinkControl*
<br/>
/*
  AnalogReadSerial with LED Blink Control
<br>
  Reads an analog input on pin A0, prints the result to the Serial Monitor,
  and uses the value to set the blinking time of the built-in LED.
<br>
  Connect:
  <br>
  - The center pin of a potentiometer to A0.
  - One outer pin to +5V.
  - The other outer pin to GND.
<br>
*/
<br/>

// Define the pin for the LED
<br>
const int ledPin = LED_BUILTIN;            // Built-in LED pin (usually pin 10)
<br/>

// the setup routine runs once when you press reset:
<br>
void setup() {
<br>
  // Initialize serial communication at 9600 bits per second:
  <br>
  Serial.begin(9600);
  <br>
  // Set the LED pin as an output
  <br>
  pinMode(ledPin, OUTPUT);
  <br>
}
<br/>


**Part 3: Photoresistor Controlled Circuit
<br>
*Script: AnalogReadSerial_Arduino_PhotoResistor*
<br>
// Define the pin for the LED
<br>
const int ledPin = LED_BUILTIN;
<br>
const int sensorPin = A0; // Photoresistor is connected to A0
<br>

// the setup routine runs once when you press reset:
<br>
void setup() {
<br>
  // Initialize serial communication at 9600 bits per second:
  <br>
  Serial.begin(9600);
  <br>
  // Set the LED pin as an output
  <br>
  pinMode(ledPin, OUTPUT);
  <br>
}
<br/>

// the loop routine runs over and over again forever:
<br>
void loop() {
<br>
  // Read the input on analog pin A0:
  <br>
  int sensorValue = analogRead(sensorPin);
  <br>

  // Print out the value you read:
  <br>
  Serial.print("Photoresistor Value: ");
  <br>
  Serial.println(sensorValue);
  <br>

  // Set threshold for darkness
  <br>
  int threshold = 400;
  <br>

  // experimental value from placing coat over photoresistor
  <br>
  // does not work if covered by finger
  <br>
  // LED turns on and off immediately before and after being covered
  <br>

  // Turn LED on if brightness is low (sensorValue is below threshold)
  <br>
  if (sensorValue < threshold) {
  <br>
    digitalWrite(ledPin, HIGH);  // turn the LED on
    <br>
  } else {
  <br>
    digitalWrite(ledPin, LOW);   // turn the LED off
    <br>
  }
  <br>

  delay(100); // Small delay for stability
  <br>
}
<br/>

## Discussion:
Put code snippets in where necessary.

Open the blink program (File>Examples>Basics>Blink) and download it to the Arduino.
a. What does this program do?
b. What are the major sections of the computer program and what does each section do?

Your LED flashes with a delay from the uploaded code. Decrease this delay (after both write instructions)
until the LED just stops blinking—that is until the light is still blinking but appears to stay constantly
illuminated.
a. What is the value of your delay now?
b. What field may this “persistence of vision” play a greater role in?
c. Discuss this further in your lab report.

Part 2
What is the difference between an analog and a digital signal?
b. In your lab report, list a few examples of real-world examples that can be described by an analog
signal. Likewise, what are the two states which can be conveyed by a digital signal?
c. What happens to the Serial Monitor Refresh rate as you move the potentiometer to control the LED
blinking time?

Part 3
Try different objects to block the light on the photoresistor. What are the minimum and maximum analog
values you can detect with this circuit?
4. Discussion Question:
a. Does the LED turn on immediately after blocking the light? What about when you remove the object
blocking the light, does the LED turn off immediately? Why?

Part 4 – LED dimmer using PWM
3. Discussion Question:
Connect the oscilloscope to the LED pin and observe and record what happens to the signal and the LED
brightness when you turn the knob of the potentiometer.

## Conclusion:

