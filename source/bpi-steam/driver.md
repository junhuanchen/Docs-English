# install driver

## Connecting boards

This product uses CH340 / CH341 serial port driver chip, which can easily install drivers automatically under Windows, Linux and other systems.

> [CH341SER related system driver] (http://www.wch.cn/download/CH341SER_ZIP.html)

Connect the board to your computer via the MicroUSB cable. The following is an example of Windows 10.

![](driver/connect.png)

## View driver

Enter **Device Manager** Confirm whether the serial port driver (Serial) is installed. The entry method is as follows.

- (Right click) on this computer -> Properties -> **Device Manager**
- Start menu -> (input)**Device Manager**
- Control Panel -> (Search)**Device Manager**

![](driver/error.png)

You can see that the device displays **USB2.0-Serial**, indicating that **Driver** is not installed. If the driver has been installed before, you can skip to step 5.

## install driver

Click here to get the [Serial CH341] (http://www.wch.cn/downloads/file/5.html) driver and install the driver as follows.

Open the downloaded **CH341SER.ZIP** zip file, go to the **CH341SER** folder, open **SETUP.EXE**, you can see the following picture.

![](driver/install.png)

Click **INSTALL** (install) and wait a few moments to complete the installation.

## Confirm serial port

Check if the board is connected successfully.

![](driver/success.png)

You can see that the original **USB2.0-Serial** disappeared and replaced by **USB-SERIAL CH340(COM3)**, which means that you have successfully installed the driver and got the board serial port name as (** COM3**), you can use a variety of serial port tools to view the information transmitted from the serial port name (COM3) board.

## Other systems

- At this point, the board connection is successful. For Linux or Mac systems, you need baidu or Google.