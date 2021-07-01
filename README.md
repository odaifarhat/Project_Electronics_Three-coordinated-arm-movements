# Project_Electronics_Three-coordinated-arm-movements

Robot arms Left &amp; Right.  Define a start for each engine.  Programming three coordinated arm movements robot arms.

#  Component:

Arduino Uno R3.

6_ Servo Motor.

Breadboard.

Wires.

# Circuit connection steps:

Step_1, Connect from arduino ground and power (5v) Breadboard.

Step_2, Connect ServoMotorsLeft pin signal (1 & 2 & 3) to digtal(pwm) in arduino pin 5 & 6 & 7.

Step_3, Connect ServoMotorsRight pin signal (4 & 5 & 6) to digtal(pwm) in arduino pin 9 & 10 & 11.

See the picture:

![Robot arms Left _Right](https://user-images.githubusercontent.com/56201060/124162853-9e96ab00-daa7-11eb-9a98-1f14224ae046.png)

# Code:

/*

june 29/6/2021

By Eng.Odai Farhat.

Robot arms Left & Right.

Define a start for each engine.

Programming three coordinated arm movements robot arms.


*/

#include <Servo.h>

int pos = 0;  // Angle 

Servo servoLeft1,servoLeft2,servoLeft3,servRight4,servRight5,servRight6;  // create servo object to control a servo



/**********************************/

void setup() {
  
servoLeft1.attach(5);     //attaches the servo on pin 5 to the servo object 
servoLeft2.attach(6);     //attaches the servo on pin 6 to the servo object
servoLeft3.attach(7);     //attaches the servo on pin 7 to the servo object
  
servRight4.attach(11);    //attaches the servo on pin 11 to the servo object
servRight5.attach(10);    //attaches the servo on pin 10 to the servo object
servRight6.attach(9);     //attaches the servo on pin 9 to the servo object
  
}

void loop() {
   
          /* First movement*/
  
  {
    
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 0; pos <= 180; pos += 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
    
  }

  for (pos = 180; pos >= 0; pos -= 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(5); // Wait for 15 millisecond(s)
  }
    
  }
     delay(2000);
  

            /* Second movement */
  
  {
    
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 60; pos <= 180; pos += 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
    
  }
  

  for (pos = 180; pos >= 60; pos -= 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(5); // Wait for 15 millisecond(s)
  }
    
  }
     delay(2000);
  
            /* Third movement */
  
  {
    
  // sweep the servo from 0 to 180 degrees in steps
  // of 1 degrees
  for (pos = 120; pos <= 180; pos += 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(15); // Wait for 15 millisecond(s)
    
  }
  

  for (pos = 180; pos >= 120; pos -= 1) {
    
    // tell servo to go to position in variable 'pos'
    servoLeft1.write(pos);
    servoLeft2.write(pos);
    servoLeft3.write(pos);
    servRight4.write(pos);
    servRight5.write(pos);
    servRight6.write(pos);
    // wait 15 ms for servo to reach the position
    delay(5); // Wait for 15 millisecond(s)
  }
    
  }
     delay(2000);
} 
  

/* END */
 

