// ---------------------------------------------------------------- //
// Arduino Ultrasonic Sensor HC-SR04
// Created by ArduinoGetStarted, https://arduinogetstarted.com
// Tutorial available here: https://arduinogetstarted.com/tutorials/arduino-ultrasonic-sensor.php
// Using Arduino IDE 1.8.13
// Wiring: Ultrasonic HC-SR04 Sensor -> Arduino:
// - VCC  -> 5VDC
//- TRIG -> Pin 12
//- ECHO -> Pin 11
//- GND  -> GND
// Tested Feb. 26th, 2021
// ---------------------------------------------------------------- //

 int trigPin = 12;    // connect TRIG pin to Arduino pin 12
int echoPin = 11;    // connect ECHO pin to Arduino pin 11

float duration_us, distance_cm;

void setup() {
  // begin serial communication with 9600 baudrate speed
  Serial.begin (9600);

  // configure the trigger pin to output mode
  pinMode(trigPin, OUTPUT);
  // configure the echo pin to input mode
  pinMode(echoPin, INPUT);
}

void loop() {
  // generate 10-microsecond pulse to TRIG pin
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  // measure duration of pulse from ECHO pin
  duration_us = pulseIn(echoPin, HIGH);

  // calculate the distance
  distance_cm = 0.017 * duration_us;// Speed of sound wave, 0.034m/us divided by 2

  // print the value to Serial Monitor
  Serial.print("distance: ");
  Serial.print(distance_cm);
  Serial.println(" cm");

  delay(500);
}
