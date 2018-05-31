# unTill(r) Driver Development Kit

A toolkit for creating unTill(r) drivers based on [unTill(r) Driver API](https://github.com/untillpro/untill-driver-api2). 

## Creating New Project

To prepare a project for a new unTill(r) driver, follow the next steps:

Clone devkit to your local directory using command line:
```
git clone https://github.com/untillpro/untill-driver-devkit
```

Open `settings.gradle` file for editing, and specify your project name, package and class name instead of default ones:

```
rootProject.name = 'my-driver'
gradle.ext.mainClassPackage = 'com.mycompany.mypackage'
gradle.ext.mainClassName = 'MyDriver'
```

_Project name will be a part of driver distribution folder_

Create project structure using command line:
```
gradlew eclipse
```

The project for your new driver is created now. You can import this project into Eclipse IDE and start developing driver as it described in [unTill(r) Driver API](https://github.com/untillpro/untill-driver-api2).

## Building Driver 

By running gradle in the existing project it prepares driver distribution folder which can be used in unTill(r) installations:

```
gradlew
```

Now you can find your driver distribution in `build/distributions/my-driver-folder`. Copy distribution folder to the `UNTILL_HOME/plugins/drivers` folder, and restart unTill(r) JServer.

## Changing Driver Version

Driver version is automatically included into driver distribution file name. Also, version is displayed in unTill(r) Backoffice in driver selection list.

You assign version to your driver manually, by editing `build.gradle` file:
```
version = '0.0.0-SNAPSHOT'
```

## Using JAR libraries in Your Driver

Put any JAR libraries you want to use into `lib`  folder in your driver project structure. Running `gradlew eclipse` from command line will update classpath in your project file. Those libraries will be automatically included in driver distribution.

## Using Your Driver in unTill(r)

In unTill(r) Backoffice open your PC settings in `Common Data / Hardware / Computers`, go to "Devices" tab and click "New". Select "Driver" in "Kind" dropdown list. Your driver should appear in "Driver" dropdown list. 
