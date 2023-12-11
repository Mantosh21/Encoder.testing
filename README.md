# Encoder.testing
12V - 24 V Rotary Encoder To Raspberry Pi

Use the N version with NPN open collector output, and pull the output to 3V3 with a 10K resistor, and place an 1K resistor from the collector to the GPIO input.

Here's a step-by-step guide on how you can configure a 12V encoder with a Raspberry Pi:

1. Gather Components:

12V encoder
Raspberry Pi
Voltage level shifter or resistors
Breadboard and jumper wires
2. Identify Encoder Specifications:

Determine the specifications of your encoder, especially the output voltage levels. Some encoders have open-collector outputs that are easier to interface with different voltage levels.
3. Voltage Level Shifter:

If your encoder outputs a higher voltage (e.g., 12V), use a dedicated voltage level shifter (like a logic level converter) to convert the signal to 3.3V or 5V compatible with the Raspberry Pi GPIO. Connect the encoder output to the high-voltage side of the level shifter and connect the low-voltage side to the Raspberry Pi GPIO pins.

4. Resistor Divider (Alternative):
Choose resistor values that divide the 12V signal to a safe level for the Raspberry Pi GPIO pins (3.3V or 5V). Connect the encoder output to the resistor divider and connect the midpoint to the Raspberry Pi GPIO pin.
5. Connect Encoder to Raspberry Pi:

Connect the encoder outputs to the voltage level shifter or resistor divider, and then connect the converted signal to a GPIO pin on the Raspberry Pi.
6. Software Configuration:

Write a Python script or use a library to read the encoder pulses on the Raspberry Pi. Popular libraries for this include RPi.GPIO or pigpio.
7. Power Considerations:

Ensure that both the Raspberry Pi and the encoder have a common ground. Also, provide power to the encoder if needed.
8. Test:

Test the setup to ensure that the encoder signals are correctly received by the Raspberry Pi. You can use GPIO interrupts or polling depending on the library you choose.
Remember to consult the datasheets of your encoder and any additional components for accurate specifications and to ensure proper connections. Always be cautious about voltage levels to prevent damage to your Raspberry Pi.
