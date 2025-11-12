                    Smart Obstacle Avoiding Car (Arduino Project)
 Project Overview: 

 This is a fully autonomous robot car built with Arduino Uno, ultrasonic sensor, and a servo motor.
It detects obstacles ahead and decides whether to turn left or right based on distance readings.

This project was made by Mansur Isah (SmartSense) to demonstrate intelligent movement and real-time object detection.

Components Used:
| Component                   | Quantity | Description                                          |
| --------------------------- | -------- | ---------------------------------------------------- |
| Arduino Uno                 | 1        | Main controller                                      |
| L293D Motor Driver          | 1        | Controls motor direction and speed                   |
| Ultrasonic Sensor (HC-SR04) | 1        | Measures distance to obstacles                       |
| Servo Motor                 | 1        | Rotates the ultrasonic sensor to scan left and right |
| DC Motors                   | 2        | Drive the robot car                                  |
| Wheels                      | 2        | Connected to DC motors                               |
| Chassis                     | 1        | Base of the robot car                                |
| Jumper Wires                | Several  | Connections                                          |
| Power Source                | 1        | 9V or battery pack                                   |


Working Principle: 

1. The ultrasonic sensor measures the distance in front of the robot.

2. If the distance is less than 30 cm, the robot:

  - Stops.

  - Moves backward slightly.

  - Rotates the servo to check left and right distances.

3. It compares both sides and turns toward the side with more space.

4. If no obstacle is detected, it keeps moving forward.


ibraries Used:

Before uploading the code, install the following libraries:

- Servo.h (already included in Arduino IDE)

- NewPing.h (install from Library Manager → search NewPing)


Circuit Connections: 
| Component          | Arduino Pin | Description         |
| ------------------ | ----------- | ------------------- |
| Servo Signal       | D3          | Servo control       |
| Ultrasonic Trigger | D11         | Sensor trigger pin  |
| Ultrasonic Echo    | D12         | Sensor echo pin     |
| Right Motor Enable(A) | D5          | Motor speed control |
| Right Motor IN1    | D7          | Motor direction     |
| Right Motor IN2    | D8          | Motor direction     |
| Left Motor Enable(B)  | D6          | Motor speed control |
| Left Motor IN3     | D9          | Motor direction     |
| Left Motor IN4    | D10         | Motor direction     |


Power Supply:

Use 9V battery or 2x 18650 Li-ion cells (7.4V)

Do not power both motors directly from Arduino — use the motor driver’s VCC pin for motor voltage


Robot Behavior Summary:
| Condition          | Action                       |
| ------------------ | ---------------------------- |
| No obstacle        | Move forward                 |
| Obstacle detected  | Stop → Reverse → Check sides |
| Left side clearer  | Turn left                    |
| Right side clearer | Turn right                   |


Credits:

Designed and developed by Mansur Isah (SmartSense).
