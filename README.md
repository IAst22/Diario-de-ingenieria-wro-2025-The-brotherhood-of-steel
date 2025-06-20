This repository contains all the materials needed to create "Raúl," an autonomous robot designed by the Brotherhood of Steel. This robot will participate in the WRO Future Engineers 2025 competition. The members of the "Brotherhood of Steel" team are:

Mora Contreras, Luis Guillermo

Perez Farkas, Alejandro

Veliz Miguel Antonio 

Introduction

Humans have a need to continually improve, and robotics is part of this improvement process, a fundamental area in processes necessary for the advancement of the future of society, which directly affects different disciplines such as medicine, industry, agriculture, and the home, among others. In this context, the project to create the robot "Raúl," in addition to arising from the purpose of competing in the WRO Future Engineers competition, also arose from our desire to innovate and face new challenges. Likewise, as second-semester computer engineering students at the Andrés Bello Catholic University, we saw it as an opportunity to develop and put our programming skills into practice. as well as learning and experimenting in the field of robotics, all in pursuit of our desire to study the new mechatronics course recently opened at this university upon completing our current degree. It's important to note that this initiative has had the support of the university since its inception, especially from the social department, which motivates us to continue making the most of the resources it offers.

Materials 

Our model is built primarily with components and parts from the Nezha inventor's kit for Micro:bit, as well as some Lego pieces. 


Electronic parts

1 Nezha expansion board 

1 Micro:bit board 

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
All electrical components are connected to a 900mA rechargeable battery, which is located inside the Nezha expansion board, included in the corresponding inventor's kit. It is charged through a micro USB connector. 


Sensor system: 
The model has 3 ultrasonic sensors on the front of the vehicle, one is arranged to see straight ahead and the other two are arranged at each corner of the front of the vehicle, diagonally, allowing the car to have a 180-degree view forward, thus emulating the vision that a driver of any vehicle without rearview mirrors would have. 
Additionally, our robot has a Smart AI Lens camera, programmed to recognize the colors red, green, and magenta, so it can recognize them and turn right or left according to the rules or park. 


Modules that make up the code: Within our code, there are different modules in charge of controlling the following components: 

Red DC motor, which is responsible for traction and power to the rear wheels to propel the vehicle. This component was adjusted to develop 30% of its force. 

Gray servomotor: Responsible for steering, therefore it applies torque to an axis that moves the gears that rotate on a rack, at different angles depending on the case. 

AI camera: Detects objects or obstacles on the road and is conditioned to that if it detects a green object, the vehicle's steering will turn left, and if the object is red, it will turn right. 

Ultrasonic sensors: Send sound signals that bounce off objects and return to the sensor, allowing it to detect the distance to said object. This emulates the echolocation system of bats.


Process for building, compiling, and uploading the code to the vehicle controllers

The code we used for our model was built on the microbit website, in an environment that uses Python as the programming language. Once the code is designed, it is downloaded to the computer and then transferred to the Micro:bit board, connected to the computer via a data transfer cable with USB/microUSB connectors. This board is then inserted into the Nezha expansion board slot, which is responsible for executing the code and compiling the data from the vehicle components.
