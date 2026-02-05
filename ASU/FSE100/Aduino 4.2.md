Page

of 2

FSE100 Study Guide: Using a Distance Sensor with Arduino  
Introduction  
This study guide reviews FSE100 Lecture Video: Using a Distance Sensor with Arduino. It  
is divided into 4 sections: Lecture Summary, Main Concepts, Key Points, Key Terms &  
Definitions.  
Lecture Summary  
The tutorial guides learners through the process of setting up and programming an  
ultrasonic distance sensor with Arduino. By understanding the working of the HCSR04  
sensor and implementing appropriate wiring and coding practices, users can effectively  
measure distances. The key takeaway is the practical application of timing ultrasonic  
pulses and converting time intervals into measurable distances using the speed of sound.  
This technology has various applications, including robotics, automotive safety, and  
obstacle detection systems.  
Main Concepts  
Ultrasonic Distance Sensor (HCSR04)  
Pins Overview  
- VCC: Powered by 5V input.  
- GND: Ground pin.  
- Trig: Trigger pin to emit ultrasonic sound.  
- Echo: Receives the reflected sound.  
Working Principle  
The sensor emits a sound via the Trig pin, which travels, reflects off an obstacle, and is  
then captured by the Echo pin. The time taken for the sound to travel to the obstacle and  
back is calculated and used to determine distance.  
Arduino Connection  
Wiring  
- VCC to 5V on Arduino.  
- GND to ground on Arduino.  
- Trig to digital pin 12.  
- Echo to digital pin 11.  
Arduino Code Basics  
- Initializing pins using pinMode().  
- Using digitalWrite() to control Trig pin.  
- pulseIn() function to measure the reflected sound time.

- Calculating distance using the speed of sound.  
Key Points  
Sensor Setup  
- The sensor requires a 5V power supply and a ground connection.  
- The Trig pin emits the ultrasonic pulse, and the Echo pin captures the reflected signal.  
Timing the Pulse  
- Properly timing the emission and reception of the pulse is critical. The difference in  
timing is used to calculate distance.  
Calculating Distance  
- Use the duration from the pulseIn() function to determine how long the pulse took to  
reflect back.  
- Apply the formula: Distance = (Time * Speed of Sound) / 2 to calculate the actual  
distance.  
Arduino Code Implementation  
- Loop function continually triggers the sensor and reads the response.  
- Uses serial communication to display the distance.  
Key Terms and Definitions  
VCC: Voltage at the common collector, used to power the sensor.  
GND: Ground pin, used for the electrical return path.  
Trig Pin: The pin on the sensor used to trigger the emission of the ultrasonic pulse.  
Echo Pin: The pin used to receive the reflected ultrasonic pulse.  
pulseIn(): A function in Arduino programming that measures the time duration a pin stays  
high or low.  
Serial.begin(): Initializes serial communication at a specified baud rate.  
Speed of Sound: Approx. 343 meters per second at room temperature in air.