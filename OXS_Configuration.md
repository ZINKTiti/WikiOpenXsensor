# Understanding and Configuring OpenXsensor #

OXS is using an [Arduino](http://arduino.cc/) board, so download the [Arduino IDE](http://arduino.cc/en/Main/Software#toc2) to use it.

Then, you have to **[download the latest versions](OXS_Downloads)** of OpenXsensor and OXS Configurator.

Decompress the archives, then place the folder "openXsensor" in your arduino project directory. You can put the folder "OXS\_Configurator\_vx.y" where you want.


---


## About OpenXsensor Configurator ##

OpenXsensor can do a lot of different measurements (that you can combine as you want) therefore it needs a rather dense configuration file.

That's why the **OpensXsensor Configurator** has been created, it helps setting all the OXS functionalities more easily. The documentation below will only make use of the OXS Configurator.


---


## OXS Configurator Title ##

![OXSC_01](images/OXSC_01.png)

On the top right logo corner you've got an "About" button, on the bottom left, you'll see the compatible OpenXsensor version and in the bottom right, the Configurator version.

All along the program, you can hover the mouse on the controls and a tooltip should appear with a breve description and/or the default value.


---


## General settings ##

### OXS directory ###

![OXSC_02](images/OXSC_02.png)

Here you can set the OpenXsensor directory so that the config file could be written in the right place.

Unfortunately, the text field doesn't support copy pasting, but you can manually type the path or click the button "..." at the right and navigate to the OXS folder.


---


### DATA output settings ###

![OXSC_03](images/OXSC_03.png)

The serial output pin number is the Arduino digital pin to connect to the receiver telemetry data input:
  * Pin labelled "Rx" on the D series receivers ![D8R_Side](images/D8R_Side.png)

  * Pin labelled "S" from the Smart Port connector on the X series receivers ![X8R_topSP](images/X8R_topSP.png)

The Sensor ID choice is only relevant with a Smart Port capable receiver (X series), it doesn't have any effect with D series receivers.

  * In S.Port protocol, there may be several sensors connected on the same bus (e.g. a GPS) but each sensor must have a different Sensor ID. So, you have to define a Sensor ID for your OXS that is different from sensor ID of other sensors.
  * Just stay with the default setting unless you've got a good reason ;)


---


### Voltage reference ###

![OXSC_04](images/OXSC_04.png)

**! Never connect a voltage > VCC to an Ax Arduino analog pin !**

Voltages can be measured compared to VCC or an 1.1V internal reference:

  * If VCC is very stable, it is probably more accurate and easier to measure voltages based on VCC. Still, this requires that the voltage applied on Arduino "RAW" pin is regulated, or at least always more than 5.5V for a 5V Arduino or 3.7V for a 3.3V Arduino (headroom needed for the Arduino board regulator).
  * If voltage on "Raw" pin is less than 5.5V or 3.7V depending on the Arduino used, and unstable (e.g. due to servo consumption or low battery), then voltage measurements will be wrong.
  * If VCC can't be very stable (e.g. Arduino is powered by a battery), then it is possible to measure based on the Arduino 1.1V internal reference.

To measure a voltage greater than VCC or 1.1V depending on the option you choose, you need to use a [voltage divider](https://learn.sparkfun.com/tutorials/voltage-dividers).

This will be discussed in details when we'll talk about voltage sensors.


---


### Save data to EEPROM ###

![OXSC_05](images/OXSC_05.png)

If checked, current consumption will be stored in EEPROM (Arduino memory) every 10 seconds.

This value will be restored every power up, so you will keep data continuity even if the model is turned off between flights.

![OXSC_06](images/OXSC_06.png)

With this option enabled and the corresponding pin number set, you can use a button (connected to the digital Arduino pin previously chosen) to reset the current consumption.


---


### Sensors selection ###

![OXSC_07](images/OXSC_07.png)

Tick the sensors connected so that OXS can use them.

_Note: The second barometric sensor (Vario 2) can only be used if Vario 1 is activated._
_The 2 varios both share the same configuration._


---


### Preset management ###

![OXSC_08](images/OXSC_08.png)

You can load and save preset settings for your different OpenXsensor configurations.

The "Preset" folder in the Configurator root is opened by default, but you can put them where you want.


---


**next** --> [Vario settings](OXS_Conf_Vario)