# API List

## Constants

<table>
    <tr>
        <th>Constant Name</th>
        <th>Value</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>CHAR_FLASH_TIME</td>
        <td>0.3</td>
        <td>Character Flash time</td>
    </tr>
    <tr>
        <td>CONNECTION_SERVER_CLOSED</td>
        <td>"Error: Request to device failed"</td>
        <td>Error strings</td>
    </tr>
    <tr>
        <td>NO_CONNECTION</td>
        <td>"Error: The device is not connected"</td>
        <td>Error strings</td>
    </tr>
    <tr>
        <td>DISTANCE_FACTOR</td>
        <td>117/100</td>
        <td>Calculations after receiving the raw values for Hummingbird</td>
    </tr>
    <tr>
        <td>SOUND_FACTOR</td>
        <td>200/255</td>
        <td>Calculations after receiving the raw values for Hummingbird</td>
    </tr>
    <tr>
        <td>DIAL_FACTOR</td>
        <td>100/230</td>
        <td>Calculations after receiving the raw values for Hummingbird</td>
    </tr>
    <tr>
        <td>LIGHT_FACTOR</td>
        <td>100/255</td>
        <td>Calculations after receiving the raw values for Hummingbird</td>
    </tr>
    <tr>
        <td>VOLTAGE_FACTOR</td>
        <td>3.3/255</td>
        <td>Calculations after receiving the raw values for Hummingbird</td>
    </tr>
    <tr>
        <td>BATTERY_FACTOR</td>
        <td>0.0406</td>
        <td>Scaling factors for Finch</td>
    </tr>
    <tr>
        <td>TEMPO</td>
        <td>60</td>
        <td>General constant for musical tempo</td>
    </tr>
</table>

## Classes

### Microbit

<table>
    <tr>
        <th>Method Name</th>
        <th>Input</th>
        <th>Input Type</th>
        <th>Output Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>__init__</td>
        <td>device</td>
        <td>String</td>
        <td>None</td>
        <td>Called when the class is initialized.</td>
    </tr>
    <tr>
        <td>isConnectionValid</td>
        <td>None</td>
        <td>None</td>
        <td>Boolean</td>
        <td>This function tests a connection by attempting to read whether or not the micro:bit is shaking.</td>
    </tr>
    <tr>
        <td>isMicrobit</td>
        <td>None</td>
        <td>None</td>
        <td>Boolean</td>
        <td>This function determines whether or not the device is a micro:bit.</td>
    </tr>
    <tr>
        <td>clampParametersToBounds</td>
        <td>input, inputMin, inputMax</td>
        <td>Integer, Integer, Integer</td>
        <td>Integer</td>
        <td>This function checks whether an input parameter is within the given bounds.</td>
    </tr>
    <tr>
        <td>process_display</td>
        <td>value</td>
        <td>String</td>
        <td>String</td>
        <td>Convert a string of 1's and 0's into true and false.</td>
    </tr>
    <tr>
        <td>__constrainToInt</td>
        <td>number</td>
        <td>Float</td>
        <td>Integer</td>
        <td>Utility function to ensure number is an integer.</td>
    </tr>
    <tr>
        <td>setDisplay</td>
        <td>LEDlist</td>
        <td>List</td>
        <td>None</td>
        <td>Set Display of the LED Array on microbit with the given input LED list of 0's and 1's.</td>
    </tr>
    <tr>
        <td>print</td>
        <td>message</td>
        <td>String</td>
        <td>None</td>
        <td>Print the characters on the LED screen.</td>
    </tr>
    <tr>
        <td>setPoint</td>
        <td>x, y, value</td>
        <td>Integer, Integer, Integer</td>
        <td>None</td>
        <td>Choose a certain LED on the LED Array and switch it on or off.</td>
    </tr>
    <tr>
        <td>playNote</td>
        <td>note, beats</td>
        <td>Integer, Integer</td>
        <td>None</td>
        <td>Make the buzzer play a note for certain number of beats.</td>
    </tr>
    <tr>
        <td>getAcceleration</td>
        <td>None</td>
        <td>None</td>
        <td>Tuple</td>
        <td>Gives the acceleration of X, Y, Z in m/sec2.</td>
    </tr>
    <tr>
        <td>getCompass</td>
        <td>None</td>
        <td>None</td>
        <td>Integer</td>
        <td>Returns values 0-359 indicating the orientation of the Earth's magnetic field.</td>
    </tr>
    <tr>
        <td>getMagnetometer</td>
        <td>None</td>
        <td>None</td>
        <td>Tuple</td>
        <td>Return the values of X, Y, Z of a magnetometer.</td>
    </tr>
    <tr>
        <td>getButton</td>
        <td>button</td>
        <td>String</td>
        <td>Boolean</td>
        <td>Return the status of the button asked.</td>
    </tr>
    <tr>
        <td>getSound</td>
        <td>None</td>
        <td>None</td>
        <td>Integer</td>
        <td>Return the current sound level as an integer between 1 and 100.</td>
    </tr>
    <tr>
        <td>getTemperature</td>
        <td>None</td>
        <td>None</td>
        <td>Integer</td>
        <td>Return the current temperature as an integer in degrees Celsius.</td>
    </tr>
    <tr>
        <td>isShaking</td>
        <td>None</td>
        <td>None</td>
        <td>Boolean</td>
        <td>Return true if the device is shaking, false otherwise.</td>
    </tr>
    <tr>
        <td>getOrientation</td>
        <td>None</td>
        <td>None</td>
        <td>String</td>
        <td>Return the orientation of the micro:bit.</td>
    </tr>
    <tr>
        <td>stopAll</td>
        <td>None</td>
        <td>None</td>
        <td>None</td>
        <td>Stop all device outputs (e.g., Servos, LEDs, LED Array, Motors, etc.).</td>
    </tr>
</table>

### Hummingbird

<table>
    <tr>
        <th>Method Name</th>
        <th>Input</th>
        <th>Input Type</th>
        <th>Output Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>__init__</td>
        <td>device</td>
        <td>String</td>
        <td>None</td>
        <td>Class initializer. Specify device letter A, B, or C.</td>
    </tr>
    <tr>
        <td>isHummingbird</td>
        <td>None</td>
        <td>None</td>
        <td>Boolean</td>
        <td>This function determines whether or not the device is a Hummingbird.</td>
    </tr>
    <tr>
        <td>isPortValid</td>
        <td>port, portMax</td>
        <td>Integer, Integer</td>
        <td>Boolean</td>
        <td>This function checks whether a port is within the given bounds.</td>
    </tr>
    <tr>
        <td>calculate_LED</td>
        <td>intensity</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Utility function to covert LED from 0-100 to 0-255.</td>
    </tr>
    <tr>
        <td>calculate_RGB</td>
        <td>r_intensity, g_intensity, b_intensity</td>
        <td>Integer, Integer, Integer</td>
        <td>Tuple</td>
        <td>Utility function to covert RGB LED from 0-100 to 0-255.</td>
    </tr>
    <tr>
        <td>calculate_servo_p</td>
        <td>servo_value</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Utility function to covert Servo from 0-180 to 0-255.</td>
    </tr>
    <tr>
        <td>calculate_servo_r</td>
        <td>servo_value</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Utility function to covert Servo from -100 - 100 to 0-255.</td>
    </tr>
    <tr>
        <td>setLED</td>
        <td>port, intensity</td>
        <td>Integer, Integer</td>
        <td>None</td>
        <td>Set LED of a certain port requested to a valid intensity.</td>
    </tr>
    <tr>
        <td>setTriLED</td>
        <td>port, redIntensity, greenIntensity, blueIntensity</td>
        <td>Integer, Integer, Integer, Integer</td>
        <td>None</td>
        <td>Set TriLED of a certain port requested to a valid intensity.</td>
    </tr>
    <tr>
        <td>setPositionServo</td>
        <td>port, angle</td>
        <td>Integer, Integer</td>
        <td>None</td>
        <td>Set Position servo of a certain port requested to a valid angle.</td>
    </tr>
    <tr>
        <td>setRotationServo</td>
        <td>port, speed</td>
        <td>Integer, Integer</td>
        <td>None</td>
        <td>Set Rotation servo of a certain port requested to a valid speed.</td>
    </tr>
    <tr>
        <td>getSensor</td>
        <td>port</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Read the value of the sensor attached to a certain port.</td>
    </tr>
    <tr>
        <td>getLight</td>
        <td>port</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Read the value of the light sensor attached to a certain port.</td>
    </tr>
    <tr>
        <td>getSound</td>
        <td>port</td>
        <td>String/Integer</td>
        <td>Integer</td>
        <td>Read the value of the sound sensor attached to a certain port.</td>
    </tr>
    <tr>
        <td>getDistance</td>
        <td>port</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Read the value of the distance sensor attached to a certain port.</td>
    </tr>
    <tr>
        <td>getDial</td>
        <td>port</td>
        <td>Integer</td>
        <td>Integer</td>
        <td>Read the value of the dial attached to a certain port.</td>
    </tr>
    <tr>
        <td>getVoltage</td>
        <td>port</td>
        <td>Integer</td>
        <td>Float</td>
        <td>Read the value of the dial attached to a certain port.</td>
    </tr>
</table>

### Finch

<table>
    <tr>
        <th>Method Name</th>
        <th>Input</th>
        <th>Input Type</th>
        <th>Output Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>__init__</td>
        <td>device</td>
        <td>String</td>
        <td>None</td>
        <td>Class initializer.</td>
    </tr>
    <tr>
        <td>__isFinch</td>
        <td>None</td>
        <td>None</td>
        <td>Boolean</td>
        <td>Determine whether or not the device is a Finch.</td>
    </tr>
    <tr>
        <td>setBeak</td>
        <td>redIntensity, greenIntensity, blueIntensity</td>
        <td>Integer, Integer, Integer</td>
        <td>None</td>
        <td>Set beak to a valid intensity. Each intensity should be an integer from 0 to 100.</td>
    </tr>
    <tr>
        <td>setTail</td>
        <td>port, redIntensity, greenIntensity, blueIntensity</td>
        <td>String/Integer, Integer, Integer, Integer</td>
        <td>None</td>
        <td>Set tail to a valid intensity. Port can be specified as 1, 2, 3, 4, or all.</td>
    </tr>
    <tr>
        <td>setMove</td>
        <td>direction, distance, speed</td>
        <td>String, Integer, Integer</td>
        <td>None</td>
        <td>Move the Finch forward or backward for a given distance at a given speed.</td>
    </tr>
    <tr>
        <td>setTurn</td>
        <td>direction, angle, speed</td>
        <td>String, Integer, Integer</td>
        <td>None</td>
        <td>Turn the Finch right or left to a given angle at a given speed.</td>
    </tr>
    <tr>
        <td>setMotors</td>
        <td>leftSpeed, rightSpeed</td>
        <td>Integer, Integer</td>
        <td>None</td>
        <td>Set the speed of each motor individually.</td>
    </tr>
    <tr>
        <td>stop</td>
        <td>None</td>
        <td>None</td>
        <td>None</td>
        <td>Stop the Finch motors.</td>
    </tr>
    <tr>
        <td>resetEncoders</td>
        <td>None</td>
        <td>None</td>
        <td>None</td>
        <td>Reset both encoder values to 0.</td>
    </tr>
    <tr>
        <td>getLight</td>
        <td>direction</td>
        <td>String</td>
        <td>Integer</td>
        <td>Read the value of the right or left light sensor.</td>
    </tr>
    <tr>
        <td>getDistance</td>
        <td>None</td>
        <td>None</td>
        <td>Integer</td>
        <td>Read the value of the distance sensor.</td>
    </tr>
    <tr>
        <td>getLine</td>
        <td>direction</td>
        <td>String</td>
        <td>Integer</td>
        <td>Read the value of the right or left line sensor.</td>
    </tr>
    <tr>
        <td>getEncoder</td>
        <td>direction</td>
        <td>String</td>
        <td>Float</td>
        <td>Read the value of the right or left encoder.</td>
    </tr>
    <tr>
        <td>getAcceleration</td>
        <td>None</td>
        <td>None</td>
        <td>Tuple</td>
        <td>Gives the acceleration of X, Y, Z in m/sec2, relative to the Finch's position.</td>
    </tr>
    <tr>
        <td>getCompass</td>
        <td>None</td>
        <td>None</td>
        <td>Integer</td>
        <td>Returns values 0-359 indicating the orientation of the Earth's magnetic field, relative to the Finch's position.</td>
    </tr>
    <tr>
        <td>getMagnetometer</td>
        <td>None</td>
        <td>None</td>
        <td>Tuple</td>
        <td>Return the values of X, Y, Z of a magnetometer, relative to the Finch's position.</td>
    </tr>
    <tr>
        <td>getOrientation</td>
        <td>None</td>
        <td>None</td>
        <td>String</td>
        <td>Return the orientation of the Finch.</td>
    </tr>
</table>
