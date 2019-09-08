# Testing electronics

## Requirements

* windows: HTerm
* linux: moserial

## Programmer

### Mainboard code
https://os.mbed.com/users/Reiko/code/ut_bbr_2018/ (new)
https://os.mbed.com/users/Reiko/code/ut_bbr/ (old)

![Mainboard](mainboard.jpg?raw=true "Mainboard")
![Programmer](programmer.jpg?raw=true "Programmer")

1. Compile the code, get binary file (bin)
2. Upload the bin using the programmer
3. The lights on the programmer will flash during uploading
4. After uploading the bin file will be automatically removed from the programmer

## Motor controllers
![Motor controller](motor_controller.jpg?raw=true "Motor controller")

1. Check for short circuits using a multimeter - check resistances, should be around M-Ohms
2. Connect a power source with 12V and 100mA, check if the LED lights up
3. If it does not light up, then check the board for defects

## Wheel motor
![Mainboard and motor assemble](mainboard_motor_assemble.jpg?raw=true "Mainboard and motor assemble")

1. Connect the motor to the motor controller
2. Connect the motor controller to the mainboard
3. Use a serial terminal to connect to the mainboard (USB)
4. Write `gs` in the terminal and manually rotate the wheel to test the motor encoder
5. Connect a power source with 12V and a few Amperes
6. Send eg `sd:10:0:0:0` to set motor 0 speed to 10

## Thrower motor
![Mainboard and thrower motor assemble](mainboard_thrower_motor_assemble.jpg?raw=true "Mainboard and motor assemble")

1. Connect the motor controller to M3 on the mainboard
2. Use a serial terminal to connect to the mainboard (USB)
3. Connect a power source with 16V, 10-20A
4. Send `d:{speed}` to set motor speed
