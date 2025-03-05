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
blink_arduino

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(10);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(10);                      // wait for a second
}

**Part 2:


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

