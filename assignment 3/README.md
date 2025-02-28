# Assignment #3: Interactive Light Prototype

## Introduction

This project is an interactive light prototype that uses an RGB LED strip and a PWM-controlled LED to create dynamic lighting effects based on user interaction. The idea is to have the light change states depending on the contact of copper tape acting as a button.

- **Concept:**  
  - **OFF State:** The light is off.  
  - **YELLOW State:** When the copper tape contacts (input activated), the LED strip turns yellow for 3 seconds.  
  - **BREATH State:** After 3 seconds, a breathing (pulsing) effect is activated via a PWM-controlled LED until the copper tape is released.

- **Concept Sketches & State Diagram:**  
  ![Concept Sketch](images/sabrina_light sketch&diagram.png)

## Hardware Components

The hardware components used in this project include:

 - **M5 ATOM S3**
 - **ATOMIC PORTABC EXTENSION BASE**
 - **GROVE CABLE**
 - **USB TYPE C TO C CABLE**
 - **DIGITAL RGB LED**
 - **COPPER TAPE**
 - **PAPER & CHOPSTICKS**

## Firmware

The firmware is written in MicroPython. Below is the main code that controls the interactive behaviors of the prototype. The code first turns the NeoPixel strip yellow for 3 seconds upon activation, then uses PWM on a separate LED to create a breathing effect until the input (copper tape) is released.

```python
from machine import Pin
from neopixel import NeoPixel
from time import sleep_ms

print('NeoPixel strip example')

np = NeoPixel(Pin(7), 30)
for i in range(30):
    np[i] = (0, 0, 0)
np.write()


btn = Pin(1, Pin.IN, Pin.PULL_UP)


state = "OFF"


def set_color(color):
    for i in range(30):
        np[i] = color
    np.write()


while True:
    if state == "OFF":      
        set_color((0, 0, 0))
        if btn.value() == 0:
            sleep_ms(200)
            state = "YELLOW"
    
    elif state == "YELLOW":
        set_color((255, 255, 0))
        sleep_ms(3000)
        state = "BREATH"
    
    elif state == "BREATH":
        while state == "BREATH":
            # Increase brightness: fade in.
            for b in range(0, 256, 5):
                if btn.value() == 1: 
                    state = "OFF"
                    break
                set_color((b, b, 0))
                sleep_ms(20)
            if state != "BREATH":
                break
            # Decrease brightness: fade out.
            for b in range(255, -1, -5):
                if btn.value() == 1:
                    state = "OFF"
                    break
                set_color((b, b, 0))
                sleep_ms(20)
```

## Project Outcome

Here's a photo of the finished prototype:

![Project Outcome](images/IMG_9038.JPG)

You can also view a short video demonstration of the prototype here:  
[View Project Video](IMG_9040.MOV)


  

