# PsychoPhysioCollector
Version: 2.0.4

Document version: 1.0.1 

Date: 07/18/2016

## What is the PsychoPhysioCollector for Android?
The PsychoPhysioCollector is an App for Android OS to collect physiological, kinematical data by internal and external sensors and subjective data by questionnaires. It supports:

* Zephyr BioHarness 3
* Shimmer R2 IMUs with Shimmer ECG-Modul and Shimmer Gyro-Modul

Additionally it provides questionnaires that can show up at the end of a session and optionally on certain time intervals.

## Using the PsychoPhysioCollector

### Supported Devices
* Android Devices with API 17 (4.2)+

### Supported Features
* Collect Data from internal sensors (Accelerometer, Gyroscope, Magnetometer, Linear Accelerometer, GPS)
* Collect Data from Zephyr BioHarness 3
   * RR-Interval and ECG-Data implemented
   * Accelerometer and Breathing available
* Collect Data from Shimmer R2 IMUs with Shimmer ECG-Modul and Shimmer Gyro-Modul
* Export collected data in seperated files with synchronized timestamps
* Display questionnaires that can be displayed at the end of a session and optionally on certain time intervals
* Display data of the Shimmer IMUs in realtime for checking the setup

### Documentation
Start the App and enable the Bluetooth. Open the option menu, search and add external sensors (see supported sensors). After establishing a connection by tapping on 'Connect Sensors', you are able to configure each sensor by tapping in the table activity. Use 'Settings' in the option menu to add the name of the participant, the name of the activity and to choose a questionnaire. In the 'Settings' you are able to configure also an interval contingent protocol with variable intervals from five to 60 minutes and interval variance from zero to 180 seconds. BEFORE equipping your participant with the Smartphone and start the session you can check the data of the Shimmer IMUs visually on the Smartphone by tapping on the table activity and choosing 'Show Graph'. Tap in option menu on 'Start Session' to start a session. If an interval contingent protocol is configured, the participant is prompted to answer a questionnaire based on the configured interval. By tapping and by the keyboard input the participant is able to answer the questions. Tap 'Stop Session' to stop the data collection. A last questionnaire will always displayed. Use another App or the android monitor to get the data of the Android file system (see psychophysiocollector/PARTICIPANT_NAME/ACTIVITY_NAME)

### Installation Instructions
Use the zipped and signed APK in the apks-directory and install it on your Smartphone. This latest version (2.0.4) has only one questionnaire -- the Flow-Short-Scale by Rheinberg et al. (2003). 

If you are a familiar with running the project via Android Studio on your Smartphone, you can use the following API to create your own questionnaires in JSON in the folders assets/questionnaires/LOCALISATION_CODE/ (e.g. en or de).

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

### Example Usage
The pilot deployment was successfully used in the research project Flow-Machines ("Flow-Machines: Body Movement and Sound", 2012-2015) at the University of Applied Sciences Bremen and funded by German Federal Ministry of Education and Research (BMBF; Förderkennzeichen: 03FH084PX2).

### Used Libraries
The Zephyr Development Tools have been used that can be found on [their site](http://www.zephyranywhere.com/zephyr-labs/development-tools).
Also the Shimmer Android driver has been used which is available on [their site](http://www.shimmersensing.com/shop/shimmer-android-id).

## Author and Contribution
As by the License this is free software released by the University of Applied Sciences Bremen. The authors (Simon Bogutzky and Jan Christoph Schrader) welcome external contributors to freely use and extend this software.

## Acknowledgement
This work is part of the research project Flow-Machines ("Flow-Machines: Body Movement and Sound", 2012-2015) at the University of Applied Sciences Bremen and funded by German Federal Ministry of Education and Research (BMBF; Förderkennzeichen: 03FH084PX2)
