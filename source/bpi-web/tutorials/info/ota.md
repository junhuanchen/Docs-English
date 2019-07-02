# Hardware development board (update firmware)

If you have completed the initialization settings of the development board and also successfully connected to the Wi-Fi location, you can then prepare to update the firmware of the development board, or if you are using the editor installation version, you can no longer initialize the state. Next, complete the firmware update directly through the installation version.

## Update Firmware Method 1: Update with the installed version

Open the installation version on the computer (not sure what is the installation version, please refer to [editor] (../index.html#software)), connect the development board to the computer with a USB cable, and confirm that the installation version has been correctly read and developed. After the board (the device ID and version number of the development board will appear above), press `Ctrl + W` to open the toolbar, and select "*Tools > Update Firmware*" to start the update.

> *Special reminder! If the Device ID and version number* cannot be displayed, ** may need to manually update the board firmware**.
>
> Update the firmware method, please follow the steps below
>
> - [Initialization Method 2: Wire to the development board for initialization] (#step2)
> - [Update Firmware Method 2: Update via Wi-Fi Remote] (ota.md#step2)

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-01.jpg)

If the system detects a new version of the firmware, it will pop up a window prompt after connecting to the computer.

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-02.jpg)

If there is no pop-up window prompt, a message prompting for an update will appear in the message text above.

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-04.jpg)

After clicking the update, you will be prompted again not to close the program or remove the USB cable, and press the confirmation to start the update.

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-03.jpg)

The message text at the top of the update will show the progress of the update simultaneously.

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-05.jpg)

The current version number will be displayed after the update until 100%, indicating that the development board firmware has been updated. (The example below has been updated from 0.1.07_0105 to 0.1.09_0401_01)

![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-06.jpg)

## Update Firmware Method 2: Remote Update via Wi-Fi

Remote Update (OTA) After the development board is connected to the network, the remote server is updated to obtain the latest firmware version. The update steps are as follows:

- Step 1. Confirm that the development board is connected to WiFi normally. If not, please check the WiFi connection or re-initialize the settings.
- Step 2. Remove the power from the development board.
- Step 3. Connect the power supply to the development board. **When the white marquee light displays the text, press and hold button A, and keep pressing button A until the development board flashes red and the green light goes out. When you hear a slight sound from the buzzer, release the button A**.

  ![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-06.gif)

- Step 4. After completion, you will see the dot matrix of the development board. The first light starts to light blue, indicating that the update is started. * When the blue light is all on and then off, the update is completed*.

  ![Hardware (Update Firmware)](../images/zh-tw/docs/webbit/info/ota-07.gif)

- Step 6. After the update is completed, the development board will flash red light to automatically connect. After the connection is successful, the green light will be off and the green light will be off, indicating that the remote update is complete. At this time, the development board can also be connected via WiFi. Enter 192.168.4.1. In the setting screen, the version number of the development board will be changed to the new version at the bottom of the setting screen.

## Restore initial settings

If we want to restore the factory default settings, we can do this by means of a Wi-Fi remote update, as follows:

- Step 1. Remove the power from the development board.
- Step 2.** Press and hold buttons A and B simultaneously. **
- Step 3. Connect the power supply to the development board. ** Release the buttons A and B** after the buzzer sounds. The development board has been restored to the factory settings. (**Recovery settings will clear the custom Wi-Fi account, password, customized device SSID and password. This step will cause the development board to be unable to connect to the Wi-Fi** of the location)
- Step 4. Re-execute the initial settings, refer to: [Hardware (Initial Settings)] (setup.html)