# EXP 11 Raspberry Pi GPIO Interfacing Using Python – LED, Push Button and Sensor
## AIM:

To interface an LED, push button, and sensor with a Raspberry Pi using GPIO pins and control/read the connected devices using a Python program.

## REQUIREMENTS:

Raspberry Pi
LED
220Ω resistor
Push button
10kΩ resistor (if required)
Sensor (IR/PIR sensor)
Breadboard
Jumper wires
Raspberry Pi power supply
Python 3


# BLINKING LED
## PROCEDURE
1. Open Wokwi and create a new Raspberry Pi/Pico Python project.
2. Add an LED and a 220 Ω resistor to the circuit.
3. Connect the LED to a suitable GPIO pin through the resistor.
4. Connect the other terminal of the LED to GND.
5. Open the Python code editor.
6. Configure the selected GPIO pin as an output.
7. Write a Python program to turn the LED ON and OFF with a time delay.
8. Start the simulation by clicking the Run button.
9. Observe the LED blinking continuously at regular intervals.
10. Stop the simulation after verifying the operation
## PROGRAM:
```
from machine import Pin
from time import sleep

led = Pin(15, Pin.OUT)

while True:
    led.value(1)
    sleep(2)
    led.value(0)
    sleep(1)
```
##OUTPUT:
<img width="1919" height="1199" alt="Screenshot 2026-08-24 102357" src="https://github.com/user-attachments/assets/947a338a-3143-4a14-9336-411d5c167c88" />

# PUSH BUTTON
## PROCEDURE 
PROCEDURE

1. Open the Wokwi online simulation platform and create a new Raspberry Pi/Pico Python project.
2. Add an LED, 220 ohm resistor, and push button to the circuit.
3. Connect the LED to a suitable GPIO output pin through the resistor.
4. Connect the other terminal of the LED to GND.
5. Connect the push button to a suitable GPIO input pin and GND.
6. Configure the push button GPIO as an input using a pull-up or pull-down configuration.
7. Configure the LED GPIO as an output.
8. Write the Python program to read the push button input.
9. Start the simulation.
10. Press the push button and observe that the LED turns ON.
11. Release the push button and observe that the LED turns OFF.
12. Stop the simulation after verifying the operation.
## PROGRAM:
```
from machine import Pin
from time import sleep

led = Pin(15, Pin.OUT)
button = Pin(14, Pin.IN, Pin.PULL_UP)

while True:
    if button.value() == 0:
        led.value(1)
    else:
        led.value(0)

    sleep(0.05)
```
## OUTPUT:
<img width="1919" height="1199" alt="Screenshot 2026-08-24 104329" src="https://github.com/user-attachments/assets/269ae4ec-f4a3-41c9-a8a1-0bdd54cd93f0" />

# BUZZER SENSOR
## PROCEDURE 

1. Open the Wokwi online simulation platform and create a new Raspberry Pi/Pico Python project.
2. Add a suitable sensor and buzzer to the circuit.
3. Connect the sensor VCC and GND to the appropriate power and ground connections.
4. Connect the sensor output pin to a suitable GPIO input pin.
5. Connect the buzzer to a suitable GPIO output pin and GND.
6. Configure the sensor GPIO as an input.
7. Configure the buzzer GPIO as an output.
8. Write the Python program to continuously monitor the sensor output.
9. Start the simulation.
10. Activate the sensor and observe that the buzzer turns ON.
11. Deactivate the sensor and observe that the buzzer turns OFF.
12. Stop the simulation after verifying the operation.

## PROGRAM:
```
from machine import Pin
from time import sleep

buzzer = Pin(15, Pin.OUT)

while True:
    buzzer.on()
    sleep(1)

    buzzer.off()
    sleep(1)
```
## OUTPUT :
<img width="1919" height="1199" alt="Screenshot 2026-08-24 105057" src="https://github.com/user-attachments/assets/4acec25d-4fc5-482e-9ba3-1d3879bddd9c" />

## RESULT :

Thus, the Python program was successfully executed in the Wokwi simulator and the LED interfacing, push button and sensor with buzzer  was verified successfully.



