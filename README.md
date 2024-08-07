# CuGo-Crawler
Create 2BLDC_ZS-X11H_1Servo_Pico
ZS-X11H ESC to Raspberry Pi Pico:

Left Motor Signal Wire (Yellow) → GPIO 10 (Pico pin 14)
Right Motor Signal Wire (Yellow) → GPIO 11 (Pico pin 16)
Ground Wire (Black) → GND (Pico pin 38)
Power Wire (Red) → 5V or appropriate power source (Pico pin 36 or an external power supply)
Raspberry Pi Pico Connections for Control:

Receiver Pin A → GPIO 0 (Pico pin 1)
Receiver Pin B → GPIO 1 (Pico pin 2)
Receiver Pin C → GPIO 2 (Pico pin 4)
Receiver Pin D → GPIO 3 (Pico pin 5)
Receiver Pin E → GPIO 4 (Pico pin 6)
Receiver Pin F → GPIO 5 (Pico pin 9)
Receiver Pin G → GPIO 6 (Pico pin 10)
Receiver Pin H → GPIO 7 (Pico pin 11)
Servo Signal → GPIO 9 (Pico pin 12)
Control Pins for Direction, Brake, and Stop:

Left Motor Direction Control Wire → GPIO 12 (Pico pin 17)
Left Motor Brake Control Wire → GPIO 13 (Pico pin 18)
Left Motor Stop Control Wire → GPIO 14 (Pico pin 19)
Right Motor Direction Control Wire → GPIO 15 (Pico pin 20)
Right Motor Brake Control Wire → GPIO 16 (Pico pin 21)
Right Motor Stop Control Wire → GPIO 17 (Pico pin 22)

![image](https://github.com/user-attachments/assets/4aa27b49-58f3-47f6-b937-e8891eb3cba5)





***********Explanation:*********

Channel B (Speed Control): Adjusts the speed of both left and right motors.
Channel C (Direction Control): Determines whether the robot turns left or right based on the joystick position:
Turn Right: Left motor reverses, right motor moves forward.
Turn Left: Left motor moves forward, right motor reverses.
Straight: Both motors move in the same direction as set by Channel B.
Adjust the pulse width ranges (1500 and 1000) in the if conditions based on your specific joystick and motor behavior.
