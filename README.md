# Getting Started with the Raspberry Pi on The Edge and .NET 5 

The IoT Edge Version of .NET 5 Sample app:  https://github.com/IoT-Hands-On-Labs-ZA/RaspberryPiDotNet

![Breadboard](images/DHT11.png)

## IoT Central

Create an Application in IoT Central 
[IoT Central](https://apps.azureiotcentral.com/)

## IoT Edge Simulated Iot Edge Sensor Tutorial

Tutorial on how to create an IoT Edge device in IoT Central 
[IoT Central Simulated Sensor](https://docs.microsoft.com/en-us/azure/iot-central/core/tutorial-add-edge-as-leaf-device)

## Setting up your Physical Pi to connect to IoT Central

Update the **PiDHTEnvMonitorManifest.json** file with the credentials to your Container Repository.

![Container Repository Credentials](images/manifestcredentials.png)

Create a new Device Template \ IoT Edge Device within IoT Central abd provide the **PiDHTEnvMonitorManifest.json** file.
![New IoT Edge Device Template](images/CreateTemplate.png)

Create Interface within the Device Template
![Create IoT Edge Device Interface](images/AddInheritedInterface.png)

Import Interface with the provided **DeviceTemplateInterface.json** file

![Import Interface](images/ImportInterface.png)

The Interface is imported.

![Import Interface](images/ImportedInterface.png)

Publish the Template

![Publish Template](images/publishtemplate.png)

Create a new Device with created template

![Create Device](images/AddNewDevice.png)

Save new device

![Save Device](images/savenewdevice.png)

Choose Device

![Save Device](images/choosedevice.png)

View Connection information

![Save Device](images/viewconnection.png)


Note down Device Information 

![Device Connection](images/deviceconnection.png)

## Install IoT Edge Runtime on Raspberry Pi

Tutorial on how to Install IoT Edge Runtime on the Raspberry Pi
[Iot Edge Runtime Install](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-install-iot-edge?view=iotedge-2018-06&tabs=linux)


## Configure IoT Edge Runtime on Raspberry Pi for IoT Central

Edit **/etc/iotedge/config.yaml** file.  

![Edit Config.yaml](images/editconfigyaml.png)

Insert the previously noted down connection values for **scopeid**, **deviceid** and **primary key**

![Config.yaml](images/configyaml.png)

Restart IoT Edge Runtime

![Restart IoT Edge](images/restartiotedge.png)