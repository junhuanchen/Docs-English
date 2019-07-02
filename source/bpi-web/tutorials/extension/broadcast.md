#网络广播

The network broadcast function not only allows the development board to interact with each other, but also realizes a variety of control scenarios such as one-to-many, many-to-one, virtual and real interaction, remote broadcast, etc. Can make the application of the Internet of Things to the extreme.

## Broadcast Block List

The broadcast block consists of a block that is responsible for transmitting broadcast signals, a block that receives broadcast signals, and a block that displays broadcast signals.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-01.jpg)

## Sending a broadcast message

The "send broadcast message" building block can specify a channel name and the message text to be sent to this channel. As long as the channel name is the same, all devices or personnel on the channel can receive broadcast messages. * Sending broadcast messages is not restricted. Only physical devices can send, whether it is a physical device, a virtual device, a program without a development board, etc., can send a message* to a designated channel.

> The "send broadcast message" building block belongs to the type of "* send the completion of the program after the completion of the program*" (click on the small question mark in the front of the question icon), when the block has the block in the edit screen, * when the program encounters this Block bricks will pause until the broadcast message is sent before continuing.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-02.jpg)

## Receiving broadcast messages

The "receive broadcast message" building block can specify a channel name to continuously listen to changes in the channel. As long as someone or the development board sends a message to this channel, it can display through the building blocks of the broadcast message. * Receiving broadcast messages does not limit only physical devices. Can receive, whether it is a physical device, a virtual device, a program without a development board, etc., can receive the message of the specified channel*.

> The "Receive Broadcast Message" building block belongs to the type of "*Uninterrupted Listening Channel*" (click on the small question mark in the front) and you don't need to put it in the repeating loop, you will continue to listen to the channel message yourself.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-03.jpg)

For example, user A can send a broadcast signal to channel test while "clicking on the little monster", while users B and C are responsible for listening to the test channel, and if so, let the little monster display the received broadcast. Signal.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-04.gif)

Or you can use the button switch of the development board, send the text A to the test channel when you press A, and send the text B when you press B.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-05.jpg)

The development board listening to the test channel can write a logical judgment, displaying a red A when A is received and a blue B when receiving B.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-06.jpg)

After the two development board programs are executed, click the button switch of the development board responsible for sending the broadcast, and you can see that another development board displays the corresponding signal.

![Webcast](../images/zh-tw/docs/webbit/extension/broadcast-07.gif)