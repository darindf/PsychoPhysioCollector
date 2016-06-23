# PsychoPhysioCollector
Version: 2.0

Document version: 1.0 

Date: 23.06.2016

## What is the PsychoPhysioCollector for Android
The PsychoPhysioCollector is an App for Android OS to collect physiological, kinematical data by internal and external sensors and subjective data by questionnaires. It supports:

* Zephyr BioHarness 3
* Shimmer R2 IMUs with Shimmer ECG-Modul and Shimmer Gyro-Modul

Additionally it provides questionnaires that can show up at the end of a session and optionally on certain time intervals.

## Using the PsychoPhysioCollector

### Supported Devices

* Android Devices with API 17 (4.2)+

###Supported Features

* Collect Data from internal Sensors (Accelerometer, Gyroscope, Magnetometer, Linear Accelerometer, GPS)
* Collect Data from Zephyr BioHarness 3
   * RR-Interval and ECG-Data implemented
   * Accelerometer and Breathing available
* Collect Data from Shimmer R2 IMUs with Shimmer ECG-Modul and Shimmer Gyro-Modul
* Export collected data in seperated files with synchronized timestamps
* Display questionnaires that can be displayed at the end of a session and optionally on certain time intervals
* Display data of the Shimmer IMUs in realtime for checking the setup

#### Questionnaire Types
* Rating

```
#!json

{
   "type": "rating",
   "stars": 7,
   "question": "The Question.",
   "ratings": ["Low", "High"]
}
```

* Hidden (will not be displayed but appears in output file with "N/A")

```
#!json

{
   "type": "hidden"
}
```

* Text

```
#!json

{
   "type": "text",
   "question": "The Question."
}
```

* True/False

```
#!json

{
   "type": "truefalse",
   "question": "The Question."
}
```

### Used Libraries
The Zephyr Development Tools have been used which can be found on [their site](http://www.zephyranywhere.com/zephyr-labs/development-tools).
Also the Shimmer Android driver has been used which is available on [their site](http://www.shimmersensing.com/shop/shimmer-android-id).

## Author and Contribution
As by the License this is free software released by Simon Bogutzky. The authors (Simon Bogutzky and Jan Christoph Schrader) welcome external contributors to freely use this software.

## Acknowledgement
This work is part of the Flow-Maschinen-Project ("Flow-Maschinen: Körperbewegung und Klang") at the University of Applied Sciences Bremen and funded by the BMBF (Förderkennzeichen: 03FH084PX2)
