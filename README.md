# RoboticProcessAutomation
Some handy functions especially useful while building Robotic Process Automations with Python.

## Table of contents

[Instalation](#instalation) <br />
[Simple usage](#simple-usage) <br />
[Documentation](#documentation) <br />
&ensp; [Image recognition based automations](#image-recognition-based-automations) <br />
&ensp; [Send keys based methods](#send-keys-based-methods) <br />
&ensp; [Environment prep](#environment-prep) <br />
&ensp; [Trace logs](#trace-logs) <br />
[License](#license)

## Instalation
```
pip install RoboticProcessAutomation
```

## Simple usage
```
import RoboticProcessAutomation as rpa

rpa.click_img('path/image1.png')
```
To see more, please visit DOCS

## Documentation

### Image recognition based automations
Based on well-known *PyAutoGui* lib. <br />
Ready to use functionalities, with a lot of additional parameters. <br />
Predefined with values, evaluated by me as good starting point for most cases.

* #### click_img
```
# IT WOULD TRY TO CLICK 3-TIMES, 100pixels to the right from center of an image:
rpa.click_img('path/image1.png', off_x=100, target_retries=3)
```

target: (str) - path to the img.
target_region: (tuple) - img region rectangle in [pixels] (x,y,width,height)
target_confidence: (float) - treshold for img recognition, 0.01 - ultra low 0.99 - high
target_retries: (int) - how many retries would be performed for click img
click_type: (str) - supported ones: single,double,right
off_x: (int) - x axis offset applied to click action, from center of the target img 
off_y: (int) - y axis offset applied to click action, from center of the target img 
mode: (str) - F -> return False 
              E -> return Exception /default/
wait_before_retry: (int) - how long it would wait until each retry.
click_before_retry: (tuple) - (x,y) to focus before retry
   

  

### Send keys based methods

### Environment prep

### Trace logs

## License
MIT
