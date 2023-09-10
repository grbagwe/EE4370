# Instructions on how to setup and install jetson nano
https://developer.nvidia.com/embedded/learn

## What is Jetson nano


## Setup 
https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit#write

Download the image using the following link https://developer.nvidia.com/jetson-nano-sd-card-image

Extract the image. 

Next depending on the type of OS, follow the instructions and write the image on the SD card.

Follow the instructions to create account and password

## Set up internet 

The kit should have a USB WiFi adapter, connect it one of the free USB ports.

### find the MAC address
open a terminal and run the following command


```
$ ip a 


It should give an output as:
'''
4: wlan0: ....
    link/ether xx:yy:zz:tt:uu:xx brd ...
    ...

Copy the MAC address and register it on https://clearpass.tc.mtu.edu/

<span style="color:red">Remember to remove/disable when your done using it.</span>

Next, connect to MichiganTechOpen

## Test Camera

Connect the Pi camera.

Clone this github repo https://github.com/JetsonHacksNano/CSI-Camera.git

```
$ git clone https://github.com/JetsonHacksNano/CSI-Camera.git

Go to the directory 

``` 
cd CSI-Camera.git


Run the following command

```
gst-launch-1.0 nvarguscamerasrc sensor_id=0 ! nvoverlaysink

Ctrl+C to exit/stop the render



