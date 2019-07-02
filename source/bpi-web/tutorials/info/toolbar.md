# Editor (Installation Toolbar)

The installed version of the editor is specially designed for environments without Wi-Fi. Just open the editor and connect the development board to the USB cable for control, update or related settings. This tutorial will introduce the toolbar function of the installation. . (The editor installation version is collectively referred to as the installation version below)

> Installation version download: [WebBitSetup.zip] (http://webduinoio.github.io/samples/content/bit-download/WebBitSetup.zip#_blank)

## Function Description

After opening the installation version, press *`Ctrl + W`* on the computer keyboard to open the toolbar. There are three main function lists in the toolbar: "*System*", "*Tool*" and "*Information*".

![editor (installation toolbar)] (../images/zh-tw/docs/webbit/info/toolbar-01.gif)

###系统 > Open with browser

Click "Open with browser", it will automatically open the computer's Chrome browser and link to [editor (web version)] (https://webbit.webduino.io#_blank), usually this function is not commonly used, However, if you use features that are not supported by the installation version (such as "Voice Reading", you can only send English voices in the installation version), you can use the web version to achieve.

### Tools > Close USB connection

If the development board is connected to the computer using a USB cable, the installation version can control the development board without Wi-Fi, but the development board also has "no Wi-Fi connection function", if you want to open the development board Wi-Fi To connect, you need to close the installation program or click the "Turn off USB connection" function.

> Note, * If you turn off the USB connection, the development board will use Wi-Fi connection mode, otherwise the USB connection will be turned off and the development board will turn off the Wi-Fi connection function*.

In operation, you can also use the pull-down menu to separate Wi-Fi control or USB connection control. (Detailed operation will be introduced in the following pages)

![editor (installation toolbar)] (../images/zh-tw/docs/webbit/info/toolbar-02.jpg)

### Tools > Setting WiFi

After clicking this option, we will be asked to enter the Wi-Fi SSID and password. This function will help us to set the Wi-Fi SSID and password of the "base station to be connected" to the development board, but if there is no Wi-Fi The function of the control does not use this function. (For detailed settings, please refer to [Initialization Method 1: Initialization with Installation Version] (setup.html#step1))


> *Special reminder! If this feature is not available*, ** may need to manually update the board firmware**.
>
> Update the firmware method, please follow the steps below
>
> - [Initialization Method 2: Wire to the development board for initialization] (#step2)
> - [Update Firmware Method 2: Update via Wi-Fi Remote] (ota.html#step2)


![Hardware (Initial setting)](../images/zh-tw/docs/webbit/info/setup-03.jpg)

### Tools > Update Firmware

If the board has a new version of firmware, you can click on this option to update the firmware. (For detailed settings, please refer to [Updating Firmware Method 1: Using Installation Version to Update] (setup.html#step1) )


> *Special reminder! If this feature is not available*, ** may need to manually update the board firmware**.
>
> Update the firmware method, please follow the steps below
>
> - [Initialization Method 2: Wire to the development board for initialization] (#step2)
> - [Update Firmware Method 2: Update via Wi-Fi Remote] (ota.html#step2)

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-04.jpg)

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-02.jpg)

###资讯 > Version, copy device ID, shortcut description

The version feature will display the current firmware version, the copy device ID will copy the board's Device ID to the scrapbook, and the shortcut will display the various shortcuts supported by the installer.

![editor (installation toolbar)] (../images/zh-tw/docs/webbit/info/toolbar-03.jpg)