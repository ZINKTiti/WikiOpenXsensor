# Understanding and Configuring OpenXsensor #

## DATA Sent settings ##

![OXSC_DATA_01](images/OXSC_DATA_01.png)

This tab allows you to determine which and how sensors data are sent to the receiver and so to the TX.

### OXS measurement list ###

![OXSC_DATA_02](images/OXSC_DATA_02.png)

This dropdown list shows all the data that are possible to get from OXS, but you need to have the corresponding sensors.


---


### Telemetry data list ###

![OXSC_DATA_03](images/OXSC_DATA_03.png)

This dropdown list allows you to choose how/where the OXS measurement will be seen on the TX side.

#### DEFAULT parameter usage: ####

Generally, it's simplest to use DEFAULT parameter whenever it's possible.

![OXSC_DATA_04](images/OXSC_DATA_04.png)


---


### Modification parameters ###

![OXSC_DATA_05](images/OXSC_DATA_05.png)

As theirs names imply, you can multiply, divide and offset OXS measurements to your liking.

Click and drag right or left in the field to alter the value, only integers are available.


---


### Writing the configuration file ###

![OXSC_DATA_06](images/OXSC_DATA_06.png)

When clicking on this button, the Configurator will perform a number of verifications and will warn you if there is a problem with your settings.

The file destination is determined by the [OXS directory](OXS_Configuration#OXS_directory) setting. If it's not defined, the file will be written to the root of the Configurator executable folder.


---

