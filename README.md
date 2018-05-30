# unTill(r) Driver Development Kit

A toolkit for creating unTill(r) drivers based on [unTill(r) Driver API](https://github.com/untillpro/untill-driver-api2). 

## Creating New Project

To prepare a project for a new unTill(r) driver, follow the next steps:

Clone devkit to your local directory using command line:
```
git clone https://github.com/untillpro/untill-driver-devkit
```

Open `settings.gradle` file for editing, and specify your project name, package and class name:

```
projectName = an-example-driver
package = com.my.package
className = MyExampleDriver
```

Now create project structure using command line:
```
gradlew
```

Now the project for your new driver is created. You can open it in IDE and start developing driver as it described in [unTill(r) Driver API](https://github.com/untillpro/untill-driver-api2).

## Building Driver 

By running gradle in the existing project it prepares ZIP file with driver distribution folder which can be used in unTill(r) installations:

```
gradlew
```

Now you can find your driver distribution in `build/distributions` folder of your driver project. Unzip and copy distribution folder to the `UNTILL_HOME/plugins/drivers` folder, and restart unTill(r) JServer.

## Using Your Driver in unTill(r)

In unTill(r) Backoffice open your PC settings in `Common Data / Hardware / Computers`, go to "Devices" tab and click "New". Select "Driver" in "Kind" dropdown list. Your driver should appear in "Driver" dropdown list. 
