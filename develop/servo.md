The new servo code (v2) will be used for the boards that will be shipped.

## What is a servo motor?
A servo motor is a rotary actuator that allows for precise control of angular position. It consists of a motor coupled to a sensor for position feedback. It also requires a servo drive to complete the system. The drive uses the feedback sensor to precisely control the rotary position of the motor.
Ref: https://www.kollmorgen.com/en-us/products/motors/servo/servo-motors/#:~:text=A%20servo%20motor%20is%20a,rotary%20position%20of%20the%20motor. 

## The problems.

- Rough rotation.
- Check the potentiometer connection status.

## Solutions.

- Smoother rotation.
- The led tells the potentiometer connection status.
- It does not allow to go to the limits.
- It does not change the rotation in the middle of the current one. 

## Task Brief.

The servo code v2 is written to be uploaded in the current servo modules.
The main problems were the rough rotation and not knowing if the potentiometer value was 0V or it weren't connected at all.
Some changes that are made in the code is to limit the rotation of the servo 1 degree bellow the servo limits, this will make the servo to be more stable while its being operated.
If the user change the direction of the potentiometer the servo won't stop in the middle of the rotation, but it will complete the whole first step the it will continue to the second one, with this the servo won't get block in the function.
The last feature is to check if the potentiometer is giving the 0V as input or there is nothing connected. The board led will light up when it's first connected to the power supply, and it will be off, after there is input coming from the potentiometer, for each step the servo will turn the led will blink, to let the user know that the module is working correctly, after the rotation is completed the led will go off again. With the led the user will know if there is input coming from the potentiometer or a mistake is make in the connection.

The code is in the GitHub repository: https://github.com/Ardit-Labbox/Labbox_Embedded_Systems.git
In the name servo_labbox/Servo_motor_code_v2.ino

