<a href="https://www.tindie.com/products/onehorse/max32660-motion-co-processor/"><img src="extras/media/usfsmax.jpg" width=500></a>

This repository derives from Greg Tomasch's [code](https://github.com/gregtomasch/USFSMAX) for the Pesky Products
[USFSMAX motion coprocessor](https://www.tindie.com/products/onehorse/max32660-motion-co-processor/).  
See Greg's README for details.

Changes I made to Greg's version:

* Made a proper Arduino repository

* Eliminated globals and ```#define``` in C++ classes

* Added a simple [API](https://github.com/simondlevy/USFSMAX/blob/master/src/USFSMAX_Basic.h)
to basic functionality (scaled sensor readings)

* Moved all printout from classes to sketches

* Simplified arrays; e.g., ```gyroData[2][3]``` => ```gyroData[3]```

* Moved I<sup>2</sup>C support to
[CrossPlatformDataBus](https://github.com/simondlevy/CrossPlatformDataBus) to support multiple host types
(Arduino, RaspberryPi, NVIDIA Jetson); work in progress

I have tested this library on the following hosts:

* Teensy4.0

* TinyPICO ESP32

* Tlera Corporation Butterfly STM32L433
