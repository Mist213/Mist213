## About Me

I am a first-year computer engineering student at LSU, and I want to get a Master's degree in ECE.  Through the robotics lab I'm working in, I am getting experience with embedded C++, working with motor control, and researching as a team.  Computer architecture interests me, and a dream job for me would be working at NVIDIA in computer chip design. My next project will be making an 8-bit ALU.

## Projects

### Robotic Manipulator

Our team is building a five-joint robotic arm controlled by an Arduino Mega 2560. 
**My contribution**

- Moved step-pulse timing from the Arduino’s main loop() to a Timer1 hardware interrupt. This lets the controller maintain pulse timing while the main loop listens for serial commands, including stop requests.
- Added independent speed settings for all five joints so the operator can command each joint in degrees per second. The firmware converts each setting into a motor pulse rate using the joint’s gear ratio.
- Implemented acceleration and deceleration ramps so each joint gradually changes speed at the start and end of a move. For short moves, the joint begins slowing down before reaching the requested speed.
- Added a yes/no confirmation to the disable command so the operator can cancel before the selected motors lose holding torque.

[View the team's robotic manipulator code](https://github.com/Mist213/robotic-manipulator)
