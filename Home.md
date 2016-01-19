![OXS_Logo](https://github.com/openXsensor/openXsensor/wiki/images/OXS_Logo.png)

# [News](OXS_News) - [Downloads](OXS_Downloads) - [Documentation](OXS_Documentation) #

## Introduction ##

OpenXsensor is the evolution of [OpenXvario](https://code.google.com/p/openxvario/) and extends it to multi-sensing applications.

Discussion about this project: http://openrcforums.com/forum/viewforum.php?f=86

Based on an [Arduino](http://arduino.cc/) platform, it connects to different sensors and transmits the measurements via several telemetry capabilities.

It is compatible with :
  * The Multiplex receivers
  * The Frsky receivers : *D series* (HUB protocol) and *X series* (Smart Port protocol).
  * The Graupner receivers (Hott protocol)

##Functionalities provided at your choice :##

  * Altimeter / Variometer _(like FrSky Variometer low/high precision sensor)_
    * Can use a second barometric sensor and switch with TX while flying
  * Air Speed
    * Can also be used by oXs to compensate vertical speed measurements (dTE)
  * GPS
    * Can be connected to a GPS (NEO6/NEO7) and transmit collected data
  * Accelerometer/gyroscope
    * Can be connected to a MPU6050 sensor
    * Can calculate vertical speed based on acceleration + baro (faster reaction of vario)
  * Up to 6 voltages measurements
    * Battery voltage measurements _(like FrSky FBVS-01)_
    * Lipo battery cell measurements _(like FrSky FLVS-01 or FLVSS)_
    * ...
  * RPM sensor
  * Current sensor _(like FrSky FAS or FCS)_
    * Can calculate the consumed current
  * Can use any sensor outputting voltage
    * Temperature sensor
    * ...
  * Can calculate glider ratio to improve glider setup while flying
  
Note: more details about the way to configure oXs are given in the file oXs_config_description.h 

