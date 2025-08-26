# Basic-Heater-controller
# Heater Control System Using Arduino

## Overview
This project implements a basic heater control system using an Arduino microcontroller. It uses a DS18B20 temperature sensor (simulated here with a mock temperature), an LCD display for user interface, three push buttons for threshold adjustment and system control, an LED to indicate heater status, and a buzzer for alerting when the temperature threshold is reached.

## Features
- Temperature threshold setting with increment, decrement, and start buttons.
- Visual feedback on a 16x2 LCD display, showing current temperature and threshold.
- Simulated temperature increase for easy testing without hardware sensor.
- Heater ON/OFF indication using an LED.
- Buzzer alert for when temperature threshold is reached.
- Debounced button inputs to avoid erroneous readings.

## Hardware Components
- Arduino Uno (or compatible)
- DS18B20 temperature sensor (or simulation code for testing)
- 16x2 LCD Display
- 3 Push Buttons (Increase Threshold, Decrease Threshold, Start Heating)
- LED (Heater indicator)
- Buzzer (Alert)

## Pin Configuration
| Component         | Arduino Pin |
|-------------------|-------------|
| Increase Button   | 3           |
| Decrease Button   | 6           |
| Start Button      | 13          |
| Heater LED       | 4           |
| Buzzer           | 5           |
| LCD RS           | 12          |
| LCD EN           | 11          |
| LCD D4           | 10          |
| LCD D5           | 9           |
| LCD D6           | 8           |
| LCD D7           | 7           |
| DS18B20 Data Pin | 2           |

## Usage Instructions
1. Power the Arduino and open the Serial Monitor (baud rate 9600).
2. Adjust the temperature threshold using the Increase and Decrease push buttons.
3. Press the Start button to begin heating.
4. The temperature will simulate rising gradually.
5. The heater LED turns ON while heating.
6. When the simulated temperature reaches the threshold, the buzzer sounds for 2 seconds then the heater turns OFF.
7. After heating stops, you can set a new threshold and start again.

## Code Structure
- The main logic is in `loop()`, managing button reading, threshold adjustment, temperature update, and actuator control.
- Debounce handling ensures reliable pushbutton inputs.
- Mock temperature simulates environment temperature gradually rising.
- LCD updates with current status every iteration.
- Serial output logs all system states and values for debugging.

## Future Work and Enhancements
- Replace mock temperature with real DS18B20 sensor reading.
- Add overheating safety cutoffs with additional sensors.
- Implement multiple heating profiles selectable by user.
- Integrate remote monitoring via BLE/WiFi.
- Use FreeRTOS or timer interrupts for efficient periodic tasks.

