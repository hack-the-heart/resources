# Integrating iOS Apps with Sensors & Devices

## Overview

### HealthKit ([more info](https://developer.apple.com/library/ios/documentation/HealthKit/Reference/HealthKit_Framework/index.html#//apple_ref/doc/uid/TP40014707))
The easiest way to integrate your app with device data is through HealthKit. If a device and it's companion app supports HealthKit, then your app can read that data through HealthKit.

However this is not always the most user friendly way. Users will have to use the companion app to initiate the device recordings, have the companion app write to health kit, and then they will be able to use your app.

### Core Bluetooth
If you wanted your app to read from the device directly then you will have to find a device that supports standard BLE protocols. See this [link](https://www.raywenderlich.com/52080/introduction-core-bluetooth-building-heart-rate-monitor) on connecting a standard heart rate monitor over BLE. While this option does allow your app direct access to device data, it is a little more complicated to implement and debug.

### Devices' Cloud
If you have no way of integrating with a device directly or gathering that device's data through HealthKit, then you have the option of connecting to the device's cloud infrastructure (e.g. [Withings Cloud](http://oauth.withings.com/api)), if it exists. This method, while it being easier to implement, might not be user friendly. As the user would have to use the device's companion app to collect data from the device and send it to the cloud.

## Using HealthKit
See our starter-ios repo to see an example of reading data from HealthKit, storing it locally, and sending it to the cloud.

### Authorization
Your app must be granted access to HealthKit data from the user. If your user does not allow access to certain health data records, then you will not be able to read/write to those records.

### Notifications in the Background
You can register your app to get notifications in the background when data in HealthKit has been updated. See the starter-ios app for more information.
