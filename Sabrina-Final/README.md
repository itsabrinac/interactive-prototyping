# TeaTalk: Interactive Tea-Drinking Discussion Experience

## Introduction
TeaTalk transforms the traditional tea-drinking ritual into an interactive social experience. During the 3-minute brew time, a digital screen guides participants through a series of prompts. Lifting the teapot, pouring tea, and lifting/placing teacups trigger questions, voice recording, and a dynamic “speech bubble” display of responses.

**Context & Audience**  
- **Context:** Living room, office lounge, or gallery installation  
- **Use Case:** Ice-breaker sessions, team-building exercises, social gatherings  
- **Audience:** Friends, coworkers, exhibition visitors

![Concept Sketch 1](images/concept-sketch-1.jpg)  
![Concept Sketch 2](images/concept-sketch-2.jpg)

---

## Implementation

TeaTalk consists of hardware sensors integrated with firmware (MicroPython) running on an ESP32 (ATOM board), and software visuals created in ProtoPie. User interactions are detected via pressure and light sensors, translating physical actions into on-screen conversation prompts and animations.

### State Diagram
  
Include a state diagram (flowchart) to explan the interactive behaviors of the prototype you created.  Indicate which parts of the diagram represent hardware/firmware functionality (code on the ATOM board) and which parts are computer software (ProtoPie, etc.)   
  
### Hardware

List all the separate hardware components used in your project and briefly explain what they do.  To create a list with markdown syntax, use `-`, `*`, or `+` characters with each line of text:  
* item 1  
* item 2   
* etc.  

Include image(s) showing your hardware wiring in detail.  This could be several close-ups photos with the goal of showing the wiring connections are made between the ATOM board and each hardware component.  
  
### Schematic or Wiring Diagram

Create a diagram or sketch to represent how all the hardware components of your project are connected together.  Each separate component can be represented as a labeled box and the wire connection between them as lines labeled with numbers indicating the specific pin connections on the ATOM board.  

### Firmware   

Upload your MicroPython code and explain the important parts that make your prototype work.  Most likely you should explain the inputs/outputs used in your code and how they affect the behavior of the prototype.

To include code snippets, you can use the code block markdown, like this:

``` Python  
if(sensor_val > 100):  # sensor value higher than threshold
   led_pin.on()  # turn on LED
```

### Software   

Explain the software components of your project, such as your ProtoPie project or p5.js sketch.  Include screenshots that show the relevant details of software implementation.  

### Integrations   

Add screenshots and describe any communication components used in your project, like your ProtoPie Connect setup, Adafruit IO feeds, dashboards, IFTTT applets, etc.   

### Enclosure / Mechanical Design   

Explain how you made the enclosure or any other physical or mechanical aspects of your project with photos, screenshots of relevant files such as laser-cut patterns, 3D models, etc. (it’s great if you’re willing to share the editable source files too!)

## Project outcome  

Summarize the results of your final project implementation and include some photos of the prototype and a video walkthrough showing it working.  

Note that GitHub has a small size limit for uploading files via browswer (25Mb max), so you may choose to use a link to YouTube, Google Drive, or another external site.

## Conclusion  

As you wrap up the project, reflect on your experience of creating it.  Use this as an opportunity to mention any discoveries or challenges you came across along the way.  If there is anything you would have done differently, or have a chance to continue the project development given more time or resources, it’s a good way to conclude this section.

## Project references  

Please include links to any online resources like videos or tutorials that you may have found helpful in your process of implementing the prototype. If you used any substantial code from an online resource, make sure to credit the author(s) or sources.  
