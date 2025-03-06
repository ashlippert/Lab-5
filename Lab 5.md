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

   To begin, mount the RedBoard and breadboard onto the SparkFun base, then connect the RedBoard to a computer running the Arduino IDE. In the IDE, select the Arduino UNO board and the appropriate COM port. Next, connect a 330Ω resistor and an LED in series to pin 13 on the RedBoard, ensuring a proper ground connection. Figure 1 below shows the schematic for the circuit.

<div align= "center">
<img src="" alt "Schematic 1" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 1: LED circuit schematic. </figcaption>
</div>

<br>

   Once assembled, the RedBoard circuit created using schematic 1 should resemble what is shown in Figure 2 below.

<div align= "center">
<img src="https://github.com/user-attachments/assets/d035d937-2607-494d-9e97-8ce2f591d9b5" alt "Assembled LED circuit" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 2: Constructed LED circuit from Schematic 1. </figcaption>
</div>
<br>

**Objective 2: Controlling an LED with a Potentiometer**

**Potentiometer Controlled Circuit Assembly**

   Connect the potentiometer to 5V and Ground, with the variable resistance pin connected to A0. Keep the previous circuit intact while integrating the potentiometer into the setup. The schematic for this setup is given in Figure 3 and 4 below.


<div align="center">
<img src="https://github.com/user-attachments/assets/4cec5b73-a503-4f8a-9187-81eadedb0bf6" alt="Schematic 2" width="400">
<br/>

<figcaption style="font-size: 16px; text-align: center;"> Figure 3: Potentiometer controlled LED circuit schematic. </figcaption>
</div>   

<br/>

<div align="center">
<img src="https://github.com/user-attachments/assets/f5ad3cd8-12cb-47c6-9d8f-ee0798607954" alt="Schematic 2" width="400">
<br/>

<figcaption style="font-size: 16px; text-align: center;"> Figure 4: Potentiometer controlled LED circuit layout. </figcaption>
</div>   

<br/>

  Once assembled, the circuit should look resemble Figure 5 below.

   <div align="center">
  <img src="" alt="Assembled potentiometer controlled LED circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 5: Constructed potentiometer controlled LED circuit from Figure 3. </figcaption>
</div>
<br>

**Objective 3: Controlling an LED with a Photoresistor**

**Photoresistor Controlled Circuit Assembly**

  Replace the potentiometer in the previous circuit with a series circuit consisting of a photoresistor and a 10 kΩ resistor. Connect 5V to the photoresistor, Ground to the resistor, and A0 to the node between them. The schematic for this circuit is provided in Figure 5 below.

 <div align="center">
  <img src="https://github.com/user-attachments/assets/2d1a3739-0cca-4c5f-8fb9-16fd0eecc990" alt="Schematic 3" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 6: Photoresistor controlled LED circuit schematic. </figcaption>
</div>
<br>

 <div align="center">
  <img src="https://github.com/user-attachments/assets/e0e26917-4999-4354-8292-89b97e9d5812" alt="Schematic 3" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 7: Photoresistor controlled LED circuit layout. </figcaption>
</div>
<br>

   Once assembled, the RedBoard circuit should resemble what is shown in Figure 6 below.
   
<div align="center">
  <img src="https://github.com/user-attachments/assets/bdb131cb-9715-411e-a1f5-6af3f370975d" alt="Assembled photoresistor controlled LED circuit" width="400">
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

<br>
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

   Upload the Analog Read Serial program (Examples > Basics > AnalogReadSerial) to the Arduino and open the serial monitor (Tools > Serial Monitor), ensuring the baud rate is set to 9600 bps. Adjust the potentiometer and observe the serial output. Modify the code to control the LED’s blinking time based on the potentiometer’s input, demonstrating how analog inputs can be converted into digital signals.

   The code used for this section of the lab is provided below:
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

**Part 3: Photoresistor Controlled Circuit**
   Run the same program from the previous section and observe how different lighting conditions affect the analog values. Implement an if-else statement to turn on the LED only when the brightness sensed by the photoresistor is low. Experiment with blocking the light source and analyze the circuit’s response time by observing whether the LED turns on and off immediately.

   The code used for this portion of the lab is provided below:
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

**Part 4: LED Dimmer Using PWM**
   Read the voltage from the potentiometer and map the voltage value,from 0 to 1023, to a value from 0 to 255 using the function map(value, fromLow, fromHigh, toLow, toHigh). Write the mapped
value to the LED pin using the function analogWrite(pin, mappedvalue).

   The code used for this portion of the lab is provided below:

*Script: AnalogReadSerial_Arduino_Dimmer*
<br>
// Define the pins
<br>
const int potPin = A0;    // Potentiometer connected to A0
<br>
const int ledPin = 9;     // LED connected to PWM pin 9 (PWM capable)
<br/>

// Setup function runs once when the Arduino is powered on or reset
<br>
void setup() {
<br>
  Serial.begin(9600);     // Initialize serial communication at 9600 baud
  <br>
  pinMode(ledPin, OUTPUT); // Set LED pin as an output
  <br>
}
<br>

// Loop function runs repeatedly
<br>
void loop() {
<br>
  // Read the analog value from the potentiometer (0 - 1023)
  <br>
  int sensorValue = analogRead(potPin);
  <br/>

  // Map the sensor value to a PWM range (0 - 255)
  <br>
  int pwmValue = map(sensorValue, 0, 1023, 0, 255);
  <br>

  // Print values to Serial Monitor for debugging
  <br>
  Serial.print("Potentiometer Value: ");
  <br>
  Serial.print(sensorValue);
  <br>
  Serial.print(" -> PWM Value: ");
  <br>
  Serial.println(pwmValue);
  <br/>

  // Adjust the LED brightness using PWM
  <br>
  analogWrite(ledPin, pwmValue);
<br/>
  delay(10); // Small delay for stability
  <br>
}
<br/>

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



**Part 2: Potentiometer Controlled Circuit**



**Part 3: Photoresistor Controlled Circuit


## Discussion:
**Part 1: Blinking an LED**
<br>

The Blink program successfully made the LED connected to pin 13 turn on and off repeatedly. The code consists of two main sections: the *setup()* function, which initializes pin 13 as an output, and the *loop()* function, which continuously toggles the LED state with a delay.

When decreasing the delay time in the code, it was observed that at a delay of 10 milliseconds, the LED appeared to be constantly illuminated. This phenomenon occurs due to persistence of vision, where the human eye retains an image for a short duration after it disappears. This effect is widely used in display technologies such as LED screens, film projectors, and animations to create the illusion of continuous motion.

<br>

**Part 2: Potentiometer Controlled Circuit**


The difference between an analog and digital signal was demonstrated using a potentiometer. Analog signals can take continuous values, whereas digital signals are limited to two states: HIGH (1) and LOW (0). Examples of analog signals include sound waves, temperature variations, and light intensity. In contrast, digital signals are binary, representing ON or OFF states.

As the potentiometer was adjusted, the LED's blinking speed changed accordingly, which was reflected in the Serial Monitor. A lower resistance value resulted in a higher refresh rate, meaning the LED blinked faster, while a higher resistance slowed down the blinking and the Serial Monitor updates.

<br>

**Part 3: Photoresistor Controlled Circuit**


By using a photoresistor, it was possible to detect varying light intensities. The minimum analog reading was observed when the sensor was fully covered, approaching 0 (0V), while the maximum reading occurred under bright light, reaching close to 1023 (5V).

The LED turned on immediately upon blocking the light and turned off just as quickly when the obstruction was removed. This immediate response occurs because the circuit processes real-time analog values without incorporating hysteresis. If hysteresis were included, it would introduce a buffer zone to prevent rapid fluctuations and provide smoother transitions.

<br>

**Part 4: LED Dimmer Using PWM**


Using Pulse-Width Modulation (PWM), the brightness of an LED was controlled by adjusting the duty cycle. Observing the waveform on the oscilloscope, it was evident that increasing the duty cycle (longer HIGH time) resulted in a brighter LED, while decreasing the duty cycle (shorter HIGH time) dimmed it. At 100% duty cycle, the LED appeared fully illuminated, while at 0% duty cycle, it remained off.


This experiment demonstrated how PWM effectively simulates an analog output using digital signals, a principle used in applications such as motor speed control, LED dimming, and audio signal modulation.


## Conclusion:
This lab provided hands-on experience in microcontroller programming, sensor integration, and PWM signal control. The experiments demonstrated key principles of digital and analog signals, persistence of vision, and sensor-based input processing. The use of an oscilloscope to visualize PWM waveforms further reinforced the understanding of duty cycles and their effect on perceived LED brightness. These findings are essential for applications in embedded systems, electronic circuits, and real-world automation technologies.

