# iRemote Project
iRemote is an ESP32-powered smart controller for **Vesc** based ESCs. Developed in **C/C++** using **ESP-IDF** and **FreeRTOS**, featuring a round display for real-time telemetry, **ESPNOW**, **CAN Bus**, intuitive UI, OTA, Fail safe recovery, Hall effect sensor, Haptic feedback, 6DoF IMU, battery management IC and much more!
The first batch of these remotes was done and sent to various testers around the world. The products are now availale to purchase from [https://wavrx.com](https://wavrx.com)

#### Youtube preview
<a href="http://www.youtube.com/watch?feature=player_embedded&v=e35iLuC0cjM
" target="_blank"><img src="http://img.youtube.com/vi/e35iLuC0cjM/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="480" height="360" border="1" /></a>

#### Project photos
![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote%2BiLogger.jpg "") ![alt-text-2](https://github.com/wavrx/iRemote/blob/main/media/iRemotePuck.jpg "") ![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_Grey.jpg "")
 ![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_Trigger-2.jpg "")  ![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_grey2.jpg "")  ![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_handle.jpg "") ![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iremote.jpg "")

---

The project consists of two components:

## iRemote
### Hardware
Custom-designed PCB is powered by ESP32 Wrover. It has soft power latching, battery management IC, Haptic Feedback driver, Haptic feedback disk motor, Tone buzzer, magnetic charging port, 240x240 round IPS display, Hall effect sensor for throttle input, an extra momentary button for lights/horn, and a 6DoF IMU.
### Software
Software is written in C/C++ using ESP-IDF and FreeRTOS. The most notable operating system features are:
* Fast Real-time telemetry screen, showing speed, remote battery voltage, board battery voltage, Watts usage, ESC temperature, Throttle input, status icons for wifi, input lock, faults, etc...
* Intuitive UI with scrolling menus, animations, alert messages notifications...
* Adjustable power management settings 
* Trip ride summary page with elapsed time, total traveled distance, average speed, and average efficiency.
* Raise to wake 
* Hassle-free OTA
* Support for pairing up to 4 different transceivers 
* Programmable extra button for safety lock, trigger digital output on the transceiver
* Automatic core dump capture for unhandled errors
* Fail-safe factory reset recovery
* Haptic and Tone notifications with various settings.
* More features coming soon

### Housing Shell
The remote was designed with flexibility in mind to provide the maximum possible housing styles while re-using the same base internals.
Complete .step files are to be released once considered finished.
Mockup .stl files are available to download to test the feel and dimensions of each design. 
There are currently three styles:
#### Round Puck style
![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_Puck_Mockup.jpg "")
* Download Mockup: [iRemote_Puck_Mockup.stl](https://github.com/wavrx/iRemote/blob/main/Mockup%20STL%20files/iRemote_Puck_Mockup.stl)
#### Tail Handle style
![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_Handle_Mockup.jpg "")
* Download Mockup: [iRemote_Handle_Mockup.stl](https://github.com/wavrx/iRemote/blob/main/Mockup%20STL%20files/iRemote_Handle_Mockup.stl)
#### Trigger style
![alt-text-1](https://github.com/wavrx/iRemote/blob/main/media/iRemote_Trigger_Mockup.jpg "")
* Download Mockup: [iRemote_Trigger_Mockup.stl](https://github.com/wavrx/iRemote/blob/main/Mockup%20STL%20files/iRemote_Trigger_Mockup.stl)

## CAN Transceiver
### Hardware
CAN Transceiver is a standalone module powered by an ESP32. It has a CAN Transceiver for reliable and fault tolerant communication with Vesc variants.
The module also has two digital output pins controller from the remote.
### Software
Software is written in C/C++ using ESP-IDF and FreeRTOS. All communications are implemented over CAN BUS, using Vesc communication protocol layout.
There is no difference in the setup process between using this vs other standard receivers, except for the convenience that you get to use one cable for both controls and telemetry, plus the added bonus of automotive-grade reliability.
