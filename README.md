# Arduino-Timer [![Build Status](https://travis-ci.org/stejsoftware/Arduino-Timer.svg?branch=master)](https://travis-ci.org/stejsoftware/Arduino-Timer)

Simple software timer for the Arduino

## Installation
https://www.arduino.cc/en/Guide/Libraries

## Usage
```c++
void blinker()
{
  if( digitalRead(PIN) == HIGH )
  {
    digitalWrite(PIN, LOW);
  }
  else
  {
    digitalWrite(PIN, HIGH);    
  }
}
  
void setup() 
{
  // creates a Timer that will execute once a second
  Timer.repeat(blinker, 1000);
}

void loop() 
{
  // checks the timer and runs the handlers of expired timers.
  Timer.run();
}
```
