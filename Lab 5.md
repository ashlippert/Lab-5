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


## Test Equipment

1. Fluke 87 V DMM
2. Computer with Arduino IDE
3. Oscilloscope
   
   
## Test Procedures

**Resistor Measurement**

   For this part of the experiment, the resistance each resistor was measured using a Digital Multimeter (DMM) and the results were compared to the expected values based on the resistor color codes. We recorded the expected resistance, the acceptable tolerance range, and the measured resistance in a table. Any resistors that fell outside the expected range were noted. The technique used for resistor measurement is shown in Figure 13 below.

 <div align="center">
  <img src="https://github.com/user-attachments/assets/fd70fd10-4528-41e1-9a64-bf901897e7e4" alt="Assembled differentiating op amp circuit" width="400">
      <br/>
  <figcaption style="font-size: 16px; text-align: center;"> Figure 13: Measuring Resistor Values. </figcaption>
</div>
<br>


**Part 1: Blinking an LED**
   
   Upload the Blink program (File > Examples > Basics > Blink) to the Arduino and verify that the LED blinks. Adjust the delay in the program to decrease the blinking speed until the LED appears to remain constantly illuminated. Figure 7 shows the ON LED.

<br>
<div align= "center">
<img src="" alt "LED Blink" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 7: Blinking LED Circuit with LED on. </figcaption>
</div>

<br>


**Part 2: Potentiometer Controlled Circuit**

   Upload the Analog Read Serial program (Examples > Basics > AnalogReadSerial) to the Arduino and open the serial monitor (Tools > Serial Monitor), ensuring the baud rate is set to 9600 bps. Adjust the potentiometer and observe the serial output. Modify the code to control the LED’s blinking time based on the potentiometer’s input, demonstrating how analog inputs can be converted into digital signals.
   
<br>
<div align= "center">
<img src="https://github.com/user-attachments/assets/0343927d-d9eb-4dce-98fa-5275dc572136" alt "Function Generator" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 16: Function Generator for increasing frequency to find the op amp frequency limit. </figcaption>
</div>


**Part 3: Photoresistor Controlled Circuit**
   Run the same program from the previous section and observe how different lighting conditions affect the analog values. Implement an if-else statement to turn on the LED only when the brightness sensed by the photoresistor is low. Experiment with blocking the light source and analyze the circuit’s response time by observing whether the LED turns on and off immediately.

<br>
<div align= "center">
<img src="https://github.com/user-attachments/assets/70fde8c2-5680-46c5-9098-d5371c6bb318" alt "Sine wave Circuit 5" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 17: Sine wave output for integrating op-amp circuit. </figcaption>
</div>

## Test Results:

**Table 1: Resistor Values**

| Resistor # | Expected Resistance (Ohms) | Tolerance | Max Value (Ohms) | Min Value (Ohms) | Measured Resistance (Ohms) |
|------------|----------------------------|-----------|------------------|------------------|-----------------------------|
| 1          | 330                        | 5%        | 346.5            | 313.5            | 325  
                       |
| 2          | 1000                       | 5%        | 1050             | 950              | 990
                       |
**Part 1 Results:**

**Table 2: Unity Gain Inverting Op Amp Voltages**

| Target Vi (V) | Measured Vi (V) | Measured Vo (V) |
|---------------|-----------------|-----------------|
| -15           | -14.98          | 14.25           |
| -14           | -13.99          | 13.96           |
| -12           | -12.02          | 12              |
| -5            | -5.01           | 5.002           |
| 0             | 0.001           | 0.018           |
| 5             | 4.997           | -4.97           |
| 12            | 12.02           | -11.97          |
| 14            | 14              | -12.92          |
| 15            | 14.99           | -12.91          |

**Table 3: Moderate Gain Inverting Op Amp Oscilloscope Readings**

| Channel 1 (Vi) (mV) | Channel 2 (Vo) (mV) |   Gain   |
|---------------------|---------------------|----------|
| 101.6               | 4.2                 | 41.33    |

**Table 4: High Gain Inverting Op Amp Oscilloscope Readings**

| Channel 1 (Vi) (mV) | Channel 2 (Vo) (mV) |   Gain   |
|---------------------|---------------------|----------|
| 32.4                | 16.56               | 511.11   |

**Part 2 Results:**

**Table 5: Voltage Follower Op Amp Oscilloscope Readings**

| Channel 1 (Vi) (mV) | Channel 2 (Vo) (mV) |   Gain   |
|---------------------|---------------------|----------|
| 1.088               | 160                 | 0.147    |

**Table 6: Voltage Follower Op Amp Frequency Limit**
| Frequency Limit (mHz) |
|-----------------------|
| 4.3                   |

**Table 7: Integrating Op Amp Oscilloscope Readings**

| Channel 1 (Vi) (mV) | Channel 2 (Vo) (mV) |   Gain   |
|---------------------|---------------------|----------|
| 1.088               | 160                 | 0.147    |

**Table 8: Differentiating Op Amp Oscilloscope Readings**

| Channel 1 (Vi) (mV) | Channel 2 (Vo) (mV) |   Gain   |
|---------------------|---------------------|----------|
| 1.088               | 160                 | 0.147    |



## Discussion:

Part 1.1: 

describe performance curve for potentiometer. you will need to plot this on the excel and add the figure after Table 8.
Prepare a graph showing the lab data as scattered points around the line for the expected gain
(consider actual resistor values


<br>
<div align= "center">
<img src="https://github.com/user-attachments/assets/ce586e1d-b791-4319-a63a-db7b605d4bc1" alt "Vo vs. Vi" width="400"/>
<br>
<figcaption style="font-size: 16px; text-align: center;"> Figure 27: Vo vs. Vi. </figcaption>
</div>

We analyzed the performance curve for the potentiometer by plotting the measured Vi vs. Vo values from Table 2. The graph demonstrates a nearly linear relationship, confirming that the unity gain inverting amplifier behaves as expected within its operational range. However, as the input voltage approaches the saturation limits of the op-amp, the output deviates from the ideal linear response due to the inherent voltage limitations of the LM741. This behavior aligns with the expected characteristics of an operational amplifier nearing saturation. The plotted data was included in Excel and placed after Table 8.

Rest of Part 1: 

Compare the performance of each amplifier circuit to its expected theoretical performance with
regard to gain.

We compared the experimental gain values for the moderate and high-gain inverting op-amp circuits with the theoretical values calculated using resistor ratios. The theoretical gain for the moderate gain circuit, based on the expected resistor values, was approximately -68, but our measured gain was 41.33. Similarly, the high-gain circuit had an expected gain of -1500 but a measured gain of 511.11. These discrepancies can be attributed to component tolerances, parasitic resistances, and the limited open-loop gain of the LM741, which reduces its effectiveness at high gains.


b. Comment on the limits of op-amp circuits with respect to maximum output voltage.

We observed that the LM741 does not output its full power supply range due to internal design constraints. As shown in Table 2, the output voltage saturates at approximately ±12.9V rather than reaching the full ±15V supply rails. This behavior is a known limitation of the LM741, which typically has a voltage swing of about 2-3V less than the supply rails. This limitation must be considered in practical applications where maximizing the dynamic range is essential.


c. Are the LM741 op amps symmetric i.e. does the positive voltage performance equal the
negative voltage performance?

Our Vo vs. Vi graph indicates that the LM741 does not exhibit perfect symmetry in positive and negative voltage performance. While the output voltage generally follows the expected inverted relationship, we noticed minor differences in the absolute values of positive and negative outputs. These variations arise due to internal offsets, manufacturing tolerances, and asymmetrical sourcing and sinking capabilities of the output stage. Though small, these differences can impact precision applications.
Part 2.1: 


discuss frequency limit

We tested the voltage follower circuit to determine the frequency at which it could no longer maintain a stable output. The measured frequency limit was found to be 4.3 MHz, as recorded in Table 6. This result is unexpectedly high given that the LM741 has a typical gain-bandwidth product of approximately 1 MHz. The discrepancy is likely due to a user error in measurement, possibly from incorrect oscilloscope settings or a misunderstanding of the measuring procedure.

Rest of Part 2:

Did the integrating and differentiating circuits perform the mathematical operations expected?
Explain.

We analyzed the integrating and differentiating circuits using various input waveforms, including sine, square, and triangle waves. The integrating circuit successfully transformed:
- Sine waves into cosine waves (consistent with integration)
- Square waves into triangular waves
- Triangle waves into parabolic-like curves
  
Similarly, the differentiating circuit demonstrated expected behavior by converting:

- Sine waves into cosine waves
- Triangle waves into square waves
- Square waves into sharp spikes, characteristic of differentiation
  
These results confirm that our circuits performed their intended mathematical operations. However, at higher frequencies, distortions were observed, likely due to limitations in the LM741’s bandwidth and phase shifts introduced by non-ideal component characteristics. This highlights the importance of selecting op-amps with appropriate frequency response for high-speed applications.


## Conclusion:

This lab provided valuable hands-on experience in constructing and analyzing operational amplifier circuits. By building and testing inverting amplifiers, a voltage follower, and integrating and differentiating circuits, we gained insight into the performance limitations of the LM741 op-amp.

Our results demonstrated that real-world op-amp behavior deviates from ideal theoretical models due to factors such as component tolerances, voltage saturation limits, and bandwidth constraints. The observed gain discrepancies, output voltage clipping, and frequency response issues highlight the practical challenges in designing amplifier circuits. Additionally, while the LM741 showed minor asymmetry between positive and negative outputs, it remained functional within acceptable limits for most applications.

Despite a potential user error in measuring the frequency limit of the voltage follower, the lab successfully reinforced the fundamental principles of op-amp operation and circuit analysis. Future improvements could include using higher precision components and verifying measurements through repeated trials to minimize inconsistencies. Overall, this experiment deepened our understanding of operational amplifiers and their practical applications in signal processing and electronics.

