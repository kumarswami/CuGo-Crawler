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



******************Pin Diagram***********************
    +---------------------+
    | Raspberry Pi Pico   |
    |                     |
    |    3.3V              |
    |    GND              |
    |                     |
    |    GPIO 0 (RX A)    |--- Receiver Pin A
    |    GPIO 1 (RX B)    |--- Receiver Pin B
    |    GPIO 2 (RX C)    |--- Receiver Pin C
    |    GPIO 3 (RX D)    |--- Receiver Pin D
    |    GPIO 4 (RX E)    |--- Receiver Pin E
    |    GPIO 5 (RX F)    |--- Receiver Pin F
    |    GPIO 6 (RX G)    |--- Receiver Pin G
    |    GPIO 7 (RX H)    |--- Receiver Pin H
    |    GPIO 9 (Servo)   |--- Servo Signal Wire
    |    GPIO 10 (ESC L)  |--- Left ESC Signal Wire
    |    GPIO 11 (ESC R)  |--- Right ESC Signal Wire
    |    GPIO 12 (Left Dir)|--- Left Motor Direction Control
    |    GPIO 13 (Left Brake)|--- Left Motor Brake Control
    |    GPIO 14 (Left Stop)|--- Left Motor Stop Control
    |    GPIO 15 (Right Dir)|--- Right Motor Direction Control
    |    GPIO 16 (Right Brake)|--- Right Motor Brake Control
    |    GPIO 17 (Right Stop)|--- Right Motor Stop Control
    |                     |
    |    GND              |
    |    5V / Power       |
    +---------------------+









***********Explanation:*********

Channel B (Speed Control): Adjusts the speed of both left and right motors.
Channel C (Direction Control): Determines whether the robot turns left or right based on the joystick position:
Turn Right: Left motor reverses, right motor moves forward.
Turn Left: Left motor moves forward, right motor reverses.
Straight: Both motors move in the same direction as set by Channel B.
Adjust the pulse width ranges (1500 and 1000) in the if conditions based on your specific joystick and motor behavior.
