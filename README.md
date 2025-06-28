This repository contains all the materials needed to create "Raúl," an autonomous robot designed by the Brotherhood of Steel. This robot will participate in the WRO Future Engineers 2025 competition. The members of the "Brotherhood of Steel" team are:

Mora Contreras, Luis Guillermo

Perez Farkas, Alejandro

Veliz Miguel Antonio 

Introduction

Humans have a need to continually improve, and robotics is part of this improvement process, a fundamental area in processes necessary for the advancement of the future of society, which directly affects different disciplines such as medicine, industry, agriculture, and the home, among others. In this context, the project to create the robot "Raúl," in addition to arising from the purpose of competing in the WRO Future Engineers competition, also arose from our desire to innovate and face new challenges. Likewise, as second-semester computer engineering students at the Andrés Bello Catholic University, we saw it as an opportunity to develop and put our programming skills into practice. as well as learning and experimenting in the field of robotics, all in pursuit of our desire to study the new mechatronics course recently opened at this university upon completing our current degree. It's important to note that this initiative has had the support of the university since its inception, especially from the social department, which motivates us to continue making the most of the resources it offers.

Materials 

Our model is built primarily with components and parts from the Nezha inventor's kit for Micro:bit, as well as some Lego pieces. 


Electronic parts

1 Nezha expansion board. 

1 Micro:bit board  Programming: The Nezha board supports MakeCode, Javascript, Python, and C++ programming.

3 PLANETX ultrasonic sensors 

4 RJ11 cables 

1 Micro:bit Smart AI Lens camera 

1 900mA rechargeable battery 


Mechanical parts

1 RED DC motor for traction 

1 360-degree gray servomotor for steering 

2 wide wheels for the rear 

2 thin wheels for the front 

Various Lego and Nezha V2 building blocks compatible with Lego 


Mobility management: 

Traction system: rear traction. 
Our vehicle owes its mobility to a red DC motor connected to two wide rear wheels through two axles, one on each side of the motor. In addition, it has two narrower front wheels 


Steering system: front axle. 
The steering uses a gray servomotor connected to the board, through a 3-pin cable, which controls its turns in degrees. A central axle surrounded by a gear (circular, like a pinion), arranged on a rack (toothed bar) is connected to the servo, which moves the front wheels allowing the vehicle to be steered. 


Transmission and suspension system: 4 rubber wheels. 
The rear wheels are wider than the front ones, emulating F1 vehicles. This primarily provides greater grip and traction when accelerating and cornering, because the engine's power is transmitted through the rear wheels, and greater contact with the track helps transfer said power more effectively. 


Power management: 
All electrical components are connected to a built-in 900mAh lithium battery. This battery provides power to the micro:bit and connected components, and it is designed with protection against overcurrent, short-circuits, and electrostatic discharge. The Nezha board also features a USB Type-C charging port, supporting a 5V/3A charging input. 

Battery Capacity: 900mAh
Battery Type: Lithium battery
Charging Input: 5V (via USB Type-C port)
Charging Current: 3A
Charging Time: Approximately 50 minutes
Protection: Overcurrent, short-circuit, and electrostatic discharge protection
Operating Voltage: The Nezha breakout board V2 has a maximum operating voltage of 8.4V, a rated voltage of 7.4V, and a minimum voltage of 6.4V.

![batery nheza](https://github.com/user-attachments/assets/8ea9b1cd-e281-46eb-8538-0eb31927bee5)



Sensor system: 


Ultrasonic sensors
Our model has 3 ultrasonic sensors on the front of the vehicle, one is arranged to see straight ahead and the other two are arranged at each corner of the front of the vehicle, diagonally, allowing the car to have a 180-degree view forward, thus emulating the vision that a driver of any vehicle without rearview mirrors would have. 

The ultrasonic sensor is part of the Planet X sensor series, the model HC-SR04 sensor, a distance sensor that uses ultrasound to measure distances between 2 and 450 cm with an accuracy of up to 3 mm. It works by emitting ultrasonic pulses and measuring the time it takes for the reflected signal to return, allowing the distance to the object to be calculated.

HC-SR04 Ultrasonic Sensor Specifications:
Operating Voltage: 5V DC.
Quiescent Current: <2mA.
Working Current: 15mA.
Measuring Range: 2 - 450 cm.
Accuracy: +/- 3 mm.
Aperture Angle: 15°.
Ultrasonic Frequency: 40 kHz.
Minimum Trigger Pulse Duration (TRIG): 10 μs.
Output ECHO Pulse Duration: 100-25000 μs.
Dimensions: 45 x 20 x 15 mm.
Minimum waiting time between measurements: 20 ms (50 ms recommended).
Others: Resistant to sunlight and black objects, although soft materials may hinder detection.

![image](https://github.com/user-attachments/assets/bd67bc18-7205-4451-b744-63509dfda577)




Color sensor
Additionally, We use a color sensor Model EF05006, part of the Planet X sensor series, too. This color sensor based on the TCS3200 chip, enabling it to detect and identify colors. This sensor filters RGB data from light sources and converts it into a square wave frequency that's proportional to the light intensity. By analyzing the ratios of red, green, and blue light, the sensor can determine the color of an object. 

Specifications:
Sensor Type: The color sensor utilizes the TCS3200 chip, which is a programmable color light-to-frequency converter. 
Color Detection: It detects and filters red, green, and blue light using photodiodes and provides a frequency output proportional to the intensity of each color. 
Output: The output is a square wave with a frequency that corresponds to the intensity of the selected color. 
Control Pins: The sensor has control pins (S0, S1, S2, S3) that allow you to select the output frequency scaling and the color filter (red, green, or blue). 
Microcontroller Interface: The digital output of the sensor allows for direct interfacing with a microcontroller like the micro:bit. 

How it works: 
The sensor receives light from an object.
It filters the light into red, green, and blue components.
Each color component is converted into a frequency signal.
The micro:bit reads these frequencies and calculates the color based on the ratios of red, green, and blue.

![Untitled](https://github.com/user-attachments/assets/1070aa13-36ad-4a3d-8174-7158571ed60b)




Smart AI Lens camera
Finally, our robot has a Smart AI Lens camera model EF05045, programmed to recognize the colors red, green, and magenta, so it can recognize them and turn right or left according to the rules or park. This AI Smart Lens camera is equipped with a remarkable 90-degree ultra-wide angle lens, providing an expansive field of view.

Technical data
Name: micro:bit Smart AI Lens
Core IC: V831
Lens: 90 degree wide-angle lens
Resolution: 240x240
Screen: 1.3 inch
Compatibility: Lego
Housing material: Fire-retardant ABS
Connections: micro USB, RJ11
Communication protocol: IIC
Size: 92mm x 145mm x 40mm

![Smart AI Lens camera](https://github.com/user-attachments/assets/0b243bd1-42a3-4a46-bd90-e18cd401f6dc)


Modules that make up the code: Within our code, there are different modules in charge of controlling the following components: 

Red DC motor, which is responsible for traction and power to the rear wheels to propel the vehicle. This component was adjusted to develop 30% of its force. 

Gray servomotor: Responsible for steering, therefore it applies torque to an axis that moves the gears that rotate on a rack, at different angles depending on the case. 

AI camera: Detects objects or obstacles on the road and is conditioned to that if it detects a green object, the vehicle's steering will turn left, and if the object is red, it will turn right. 

Ultrasonic sensors: Send sound signals that bounce off objects and return to the sensor, allowing it to detect the distance to said object. This emulates the echolocation system of bats.


Process for building, compiling, and uploading the code to the vehicle controllers

The code we used for our model was built on the microbit website, in an environment that uses Python as the programming language. Once the code is designed, it is downloaded to the computer and then transferred to the Micro:bit board, connected to the computer via a data transfer cable with USB/microUSB connectors. This board is then inserted into the Nezha expansion board slot, which is responsible for executing the code and compiling the data from the vehicle components.
