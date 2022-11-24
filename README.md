# engn1650_3Dpen

## subrepos
### engn1650-3Dpen-mcu
#### https://github.com/jluke1764/engn1650-3Dpen-mcu

MCU code: converts user action to signals
* input: motion, sensed by imu —> i2c 
* input: button presses
* output: orientation of pen, speed of pen, what light is being tracked, buttons pressed
  * may need to do integration of imu and magnetometer

### engn1650-3Dpen-pc
#### https://github.com/jluke1764/engn1650-3Dpen-pc

PC code: converts MCU signals to usable variables
* input: output of MCU → usb
  * requires driver
  * IMU algorithm (separated magnetometer)
  * Mac vs PC ? 
  * C/C++
* input: camera data → usb
  * maybe requires driver? may come with its own driver
  * image processing
  * edge detection (pixel contrast tracking of light and dark)
  * ken’s algorithm for distance
  * ken’s algorithm for ellipse correction
  * how to get info from camera in real time?
* output: pen x, y, z position; speed of pen; button presses

### engn1650-3Dpen-app
#### https://github.com/jluke1764/engn1650-3Dpen-app

Application code: converts usable variables to display
* input: output of PC
* test input: csv file of coordinates/pen inputs over time
* output: displayed 3D image ( renders in real time)
  * plotting dots in an isometric view in 3D space (can be our own code)* 
* output into Unity (3D game engine)
  * may need to look into Unity library for assets, etc. 
* how motion is converted into display is determined by the application
* Python/C#
* with a different driver for windows, Ken can also use the pen with his openGL library

