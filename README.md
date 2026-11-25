## About Me

I’m a first-year computer engineering student at LSU. In LSU’s iCORE Stein Lab, I work on embedded C++ firmware that controls stepper motors for a five-joint robotic arm. I’m especially interested in computer architecture and digital chip design.

## Projects

### Robotic Manipulator

Our team is building a five-joint robotic arm controlled by an Arduino Mega 2560. 
**My contribution**

- Moved step-pulse timing from the Arduino’s main loop() to a Timer1 hardware interrupt. This lets the controller maintain pulse timing while the main loop listens for serial commands, including stop requests.
- Added independent speed settings for all five joints so the operator can command each joint in degrees per second. The firmware converts each setting into a motor pulse rate using the joint’s gear ratio.
- Implemented acceleration and deceleration ramps so each joint gradually changes speed at the start and end of a move. For short moves, the joint begins slowing down before reaching the requested speed.
- Added a yes/no confirmation to the disable command so the operator can cancel before the selected motors lose holding torque.

[View the team's robotic manipulator code](https://github.com/Mist213/robotic-manipulator)
