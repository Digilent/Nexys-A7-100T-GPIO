Nexys A7-100T GPIO Demo
==============

Description
--------------
This project is a Vivado demo using the Nexys A7-100T's switches, LEDs, RGB LED's, pushbuttons, seven-segment display, PWM audio output, PDM microphone and USB UART bridge, written in VHDL. When programmed onto the board, all sixteen of the switches are tied to their corresponding LEDs. Every time a switch is toggled, the LED directly above it will toggle with it. If the center push button is pressed, all the LEDs will be tied to ground. The two tri-color LEDs are set to gradually change colors at all times.

The seven segment display counts up from 0 to 9 as long as no buttons are pressed. As long as BTNU is pressed, the first digit on the seven segment display is turned off. In the same manner, BTNL turns off the second digit, BTNR turns off the third, and BTND turns off the fourth. BTNC turns off the entire display and resets the counter. The microphone which is next to Pmod connector JC, records audio data and sends it to the mono audio output located at J8. To listen to the mics output, you will need to plug in headphones or a speaker. 
 
To use the USB-UART bridge feature of this demo, the Nexys A7-100T must be connected to a serial terminal on the computer it is connected to over the MicroUSB cable. For more information on how to set up and use a serial terminal, such as Tera Term or PuTTY, refer to [this tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term). Whenever the reset button or BTNC is pressed, the Nexys A7-100T sends the line “Nexys A7-100T GPIO/UART DEMO!” to the serial terminal. Whenever one of the D-pad buttons other than BTNC is pressed, the line “Button press detected!” is sent.

| Button | Function                                                          |
| ------ | ----------------------------------------------------------------- |
| BTNC   | Turns off the entire seven-segment display and resets the counter |
|        | Prints "Nexys A7-100T GPIO/UART DEMO!" through theUSB-UART bridge    |
| BTNU   | Turns off the first digit on seven-segment display                |                               
|        | Prints "Button press detected!" through the USB-UART bridge       |
| BTNL   | Turns off the second digit on seven-segment display               |
|        | Prints "Button press detected!" through theUSB-UART bridge        |
| BTNR   | Turns off the third digit on seven-segment display                |
|        | Prints "Button press detected!" through the USB-UART bridge       |
| BTND   | Turns off the fourth digit on seven-segment display               |
|        | Prints "Button press detected!" through the USB-UART bridge       |
 
Requirements
--------------
* **Nexys A7-100T**:To purchase a Nexys A7-100T, see the [Digilent Store](FIXME)
* **Vivado 2018.2 Installation**:To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator Application**: For more information see the [Installing and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **Headphones/Speaker**
 
Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Nexys-A7-100T-GPIO/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Nexys-A7-100T-GPIO.xpr".
3. In the Flow Navigator panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug the Nexys A7-100T into the computer using a MicroUSB cable.
5. Open a serial terminal emulator (such as TeraTerm) and connect it to the Nexys A7-100T's serial port, using a baud rate of 9600.
6. In the green bar at the top of the Vivado window, click **Open target**. Select **Auto connect** from the drop down menu.
7. In the green bar at the top of the Vivado window, click **Program device**.
8. In the Program Device Wizard, enter "\<archive extracted location\>vivado_proj/Nexys-A7-100T-GPIO.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
9. The demo will now be programmed onto the Nexys A7-100T. See the Description section of this README to learn how to interact with this demo.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Nexys A7-100T's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-a7/start) to find more documentation, demos, and tutorials.

For technical support or questions, please post on the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)
