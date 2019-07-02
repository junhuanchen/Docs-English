# Date & time

The date and time building blocks can read the date and time of the computer and display it on the web page. It can be used with repeated loops, switches or keyboards... to make clocks, code tables, game timings, etc. .

## Get the current date and time

The "date" building block can get the current year, month, and day. The "time" building block can get the current hour, minute, and second. The hour is calculated in 24 hours. If it is 3 o'clock in the afternoon, it will display 15.

![Date & Time](../images/zh-tw/docs/webbit/detect/time-01.jpg)

## Clock

Because the date and time of the building block "* will only get once *" the current date and time, so if you want to continue detection, you can use the repeated loops, detect the time every second, the page will be able to display the clock effect after execution. .

![Date & Time](../images/zh-tw/docs/webbit/detect/time-02.gif)

## Alarm clock

An example of extending the clock, with logical building blocks, can perform an alarm function that alerts at a certain point in time after the web page is executed.

> After the judgment time has elapsed, you can stop the time by stopping the repeated blocks, and avoid the time to continue to display.

![Date & Time](../images/zh-tw/docs/webbit/detect/time-03.gif)