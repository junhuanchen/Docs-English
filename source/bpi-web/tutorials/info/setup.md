#硬件开发板( Initialization setting)

Before use, the most important thing is to initialize the settings. The purpose of the initialization settings is to enable the development board to automatically access the Internet (Internet). With the initial settings, we can also customize the display name and password of the development board, and even connect to the internet. Remote update.

> Initialization settings** Only for Wi-Fi connection control**, if you simply use "USB Control", you do not need to initialize the settings.

## Initialization method 1: Initialize using the installation version

If you are using the installation version (it is not clear what is the installation version, please refer to [Editor] (../index.html#software)), you can directly initialize the settings by following the steps in the installation version of the tool.

### Step 1. Open the toolbar

After opening the installation version, the installation version of the "version number" and the "scan USB device" message will appear at the top. At this time, the hardware development board can be connected to the computer using a USB cable to allow the software to scan.

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-01.jpg)

After scanning to the development board, the Device ID and version number* of the development board will appear on the top of *, then press *`Ctrl + W`* on the computer keyboard to open the toolbar, and select "*Tools> Set WiFi*" with the mouse. Start the initial update.

> *Special reminder! If the Device ID and version number* cannot be displayed, ** may need to manually update the board firmware**.
>
> Update the firmware method, please follow the steps below
>
> - [Initialization Method 2: Wire to the development board for initialization] (#step2)
> - [Update Firmware Method 2: Update via Wi-Fi Remote] (ota.html#step2)

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-02.jpg)


### Step 2, Set Wi-Fi SSID and Password

After clicking Set WiFi, a dialog window will pop up asking for the WiFi base station SSID name and connection password to be connected. (Enter the account and password of your location, such as a company, school or home Wi-Fi base station)

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-03.jpg)

After the setting is completed, a dialog window will pop up asking if you want to close the USB connection. If you select “OK”, the development board will connect to the designated Wi-Fi base station via the Wi-Fi SSID and password you just set. Selecting "Cancel" will turn off the Wi-Fi connection and only use the USB connection.

If you choose to turn off the USB connection function, the development board will enter the restart and flash red. When the red light is off and the green light is on once, the Bit development board has been successfully connected to the WiFi base station* in the home or environment. (If the red light keeps flashing or steady light, please go back to step 2. If the red light flashes, the "blue light" will be illuminated instead of the green light, indicating that a new version can be downloaded and updated. Please refer to [Hardware (Updated and Tough) ()) (ota.html) article.)

> In simple terms, * With Wi-Fi connection control, you can use remote control* (such as moving the development board away from the computer, the development board at home or school control), and * controlling via USB The development board must be connected to the controlled computer*, although it cannot be remotely controlled, it can be operated without Wi-Fi.

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-04.jpg)


## Initialization Method 2: Wire to the development board for initialization

If you can't use the installation version to initialize, you can also connect to the development board to initialize the settings through a Wi-Fi connection computer or mobile device. The relevant steps are as follows:

### Step 1. Connect the power supply and enter the WiFi account password to connect.

Connect the power supply. At the beginning, the full-color LED dot matrix on the front of the development board will display a series of texts through the marquee (* preset is three English characters plus four digits*). This string corresponds to the computer. Or the SSID name in the WiFi search of the mobile device, for example, bit1234 is displayed. The name of bit1234 will be seen in the WiFi search. **Note that the string "No" controls the Device ID of the development board, which is the SSID for identification** !

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-05.gif)

Since the development board has not been initialized and set up, it will not be able to connect to the local area network, so the * will flash red at the beginning, or the red light will be steady*. In this case, please prepare a WiFi-enabled computer, laptop or mobile device. Use this device for Wi-Fi search. The device that you just saw as "bitXXXX" (search for bit1234 in the above example), after finding the device, Enter the default password *12345678* to connect.

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-06.jpg)


### Step 2, set the WiFi account password and display name

* After confirming that the connection is successful*, open the browser (recommended to use Chrome), and enter 192.168.4.1 in the address bar to connect to the setting screen of the Bit development board. The screen contains the following settings:

- **WiFi SSID, PWD**: Required, indicating which Wi-Fi base station the development board should connect to.
- **Device ID**: The unique identification code for each development board. The current version is preset to be a short ID. ( *If you see a long ID with an ID of 18 yards, you can click the Shorten the ID button to change to a short ID, or remotely update to automatically change to a "short ID"*, refer to [Hardware (Update Firmware)] ( Ota.md) )
- **Device SSID, PWD**: The name and password* displayed by the device* in the WiFi search. If not filled, the SSID and the default password 12345678 will be generated automatically.
- **MQTT Server**: The server to be connected to the development board, default Global, please select China for China.

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-07.jpg)

After the setting is completed, press SUBMIT to save. The word “SAVE OK” indicates that the storage is successful. At this time, the development board will restart and flash red. When the red light is off and the green light is on once, the Bit development board has been successfully connected to the home or environment. WiFi base station inside. (If the red light keeps flashing or steady light, please remove the power supply and restart steps 1 and 2. If the red light flashes, the “blue light” will be illuminated instead of the green light, indicating that a new version can be downloaded and updated. Refer to [Update Firmware] (ota.html).

![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-08.jpg)