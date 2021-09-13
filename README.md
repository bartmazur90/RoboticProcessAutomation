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

## Documentation

### Image recognition based automations
Based on well-known *PyAutoGui* lib. <br />
Ready to use functionalities, with a lot of additional parameters. <br />
Predefined with values, evaluated by me as good starting point for most cases.

* #### click_img()
  ```
  # IT WOULD TRY TO CLICK 3-TIMES, 100PX TO THE RIGHT FROM THE CENTER OF AN IMAGE_1:

  rpa.click_img('path/image1.png', off_x=100, target_retries=3)
  ```

  <strong>target</strong>: (str) - path to the img. <br />
  <strong>target_region</strong>: (tuple) - img region rectangle in [pixels] (x,y,width,height) <br />
  <strong>target_confidence</strong>: (float) - treshold for img recognition, 0.01 - ultra low 0.99 - high <br />
  <strong>target_retries</strong>: (int) - how many retries would be performed for click img <br />
  <strong>click_type</strong>: (str) - supported ones: single,double,right <br />
  <strong>off_x</strong>: (int) - x axis offset applied to click action, from center of the target img  <br />
  <strong>off_y</strong>: (int) - y axis offset applied to click action, from center of the target img  <br />
  <strong>mode</strong>: (str) <br />
  &nbsp; F -> return False  <br />
  &nbsp; E -> return Exception /default/ <br />
  <strong>wait_before_retry</strong>: (int) - how long it would wait until each retry. <br />
  <strong>click_before_retry</strong>: (tuple) - (x,y) to focus before retry <br />

* #### wait_img_appear()
  ```
  # IT WOULD WAIT UNTIL IMAGE_1 WOULD APPEAR ON THE SCREEN WITHIN (100,100,400,500) RECTANGLE
  # IT WOULD RETURN FALSE IF AFTER TIMEOUT, IMAGE_1 IS STILL NOT VISIBLE
  
  rpa.wait_img_appear('path/image1.png', target_region = (100,100,400,500), mode = "F")
  ```
  <strong>target</strong>: (str) - path to the img. <br />
  <strong>target_region</strong>: (tuple) - img region rectangle in [pixels] (x,y,width,height) <br />
  <strong>target_confidence</strong>: (float) - treshold for img recognition, 0.01 - ultra low 0.99 - high <br />
  <strong>timeout</strong>: (int) - how long it would wait for apperance [seconds]  <br />
  <strong>mode</strong>: (str) <br />
  &nbsp;  F -> return False <br />
  &nbsp;  E -> return Exception /default/ <br />


### Send keys based methods

### Environment prep

### Trace logs

## License
MIT
