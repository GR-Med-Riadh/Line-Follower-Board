# Line-Follower-Board
JLCPCB is a company that constructs PCBs and prints 3D mechanical designs, they give us great offers with cheap prices for high quality precision PCBs. I would like to thank JLCPCB for their sponsorship and for supporting me in creating and innovating schematics, and improving my PCBs designs.

A line follower is a robot that can follow a black line in a white space or the opposite.
I designed a PCB for a line follower that can be used as the chassis of the robot. It’s divided into multiple parts being: the power supply, the microcontroller, the driver motor circuit and the infrared sensor circuit.

The power supply circuit consists of ams1117 5v and ams1117 3.3v regulators that can decrease the input voltage to 5v or 3.3v depending on need. It also contains a l293d  driver motor and its diodes to control the direction and speed of the motors.

This PCB also contains an IR circuit represented by an operational amplifier and some resistors. The operational circuit has 2 inputs, the first is the reference voltage and the second is the voltage received from the IR, the highest voltage between the two will be delivered to the output, this happens when we choose to receive digital data from the IR, otherwise we read data directly from the IRs to get analog data.
 
The brain of our circuit is the microcontroller, we chose the esp32 because it has a motor control peripheral used to synchronize motors and control their speed thanks to a timer attributed to each motor. The motor control depends on data received from the IR circuit. 

Jumpers are used to connect our motors with their driver and to connect the IR circuit to the esp32. There are 6 additional pins in case we would like to add some extra sensors.

link of jlcpcb: https://jlcpcb.com/HAR
