# LINE Chat Control

Editor preset LINE Instant messaging related function, in addition to support LINE Notify push, you can also receive LINE chat messages, control the development board through chat or interact with small monsters.

## LINE Chat Control Block List

The LINE chat-controlled building blocks include LINE Notify blocks for push-casting, LINE Chat blocks for chat, and three blocks for receiving messages, returning messages, and emoji.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-01.jpg)

## LINE Notify

LINE Notify is a very convenient push service provided by LINE. Everyone can use the LINE account. Before using it, you must go to the LINE Notify website ([https://notify-bot.line.me/zh_TW /](https://notify-bot.line.me/zh_TW/#_blank) ), log in with your own LINE account and apply for the LINE Notify token.

> For more details, please refer to: [Self-built LINE Notify Message Notification] (https://www.oxxostudio.tw/articles/201806/line-notify.html#_blank)

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-02.jpg)

After logging in, move your mouse over the personal account above and select "Personal Page".

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-03.jpg)

The "scepter" can be issued on the personal page. The role of the token is to enable the "linked service" to send a message notification via LINE Notify. The issued token and its name will appear in the list above. It is the linkage notice of IFTTT, and you will find the service with IFTTT above.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-04.jpg)

Click on "Distribution Scepter" to specify the name of the token (the name that is displayed when the notification message is sent), and whether the selection is to be received one-to-one or that the group can also receive notifications.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-05.jpg)

Click "Issue", there will be a token code, because this code "** will only appear once **", please copy this code first, find a notebook or file to save this code, you can click below The button "Close".

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-06.jpg)

Upon completion, a customized service will appear in the linked service.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-07.jpg)

At the same time, the LINE message will also receive a message that LINE Notify has issued the "Published Individual Access Scepter". At this point, LINE Notify has been set and the message can be started.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-08.jpg)

Go back to the editor, use the LINE Notify building block, fill in the token code just generated in the Token location, fill in the message you want to send at the location where the message is sent, and your LINE will receive the LINE Notify message after execution.

> "LINE Notify" is the type of "* will continue to execute the program after sending the message*" (click on the small question mark in the front) will be prompted. When there is this brick in the editing screen, * when the program encounters this The block will pause until the message is sent before continuing.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-10.jpg)

With the development board, you can also send A by pressing the A switch and B when you press the switch B.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-11.jpg)

If you want to send an image, just fill in the image URL and send it. With the development board, you can also send a picture of Pikachu by pressing the A switch.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-13.jpg)

If you want to send emoticons, you can use the "Emoji Map" blocks. There are three types of emoticons (three presets when you first install LINE). Each texture is divided into an emoticon (STKID) and an emoticon (STKPKGID). ](https://devdocs.line.me/files/sticker_list.pdf#_blank)Query the corresponding number, enter the specified number, and send the emoticon after execution. For example, with the development board, press the A switch Send an angry pattern and press the B switch to send a happy pattern.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-12.jpg)

## LINE Chat Chat Control

The "LINE Chat" building block allows us to receive messages sent from LINE via "chat" and interact with the editor or development board via messages.

> LINE Chat Blocks are blocks that are "one to one". You can receive a message in order to respond to a message. You can't send a message as LINE Notify blocks, or receive a message and return multiple messages.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-14.jpg)

To use the LINE Chat feature, you must first join Webduino Bot as a friend of LINE, * use LINE to scan the QRCode below to join a friend*.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-15.jpg)

When you join a friend, you will receive a welcome message with three tips:

> - Enter two English letters "id" to get the channel name (not your id).
> - Enter "newid" to generate a new channel name.
> - Enter the "id: name" custom channel name (may be repeated).

According to the instructions, input i and d two English letters, you will receive the name of the chat channel assigned by the system. If it is the channel name assigned by the system, each person's chat channel is different. If it is a custom channel name, then It may be duplicated with someone else's name, and may receive someone else's message.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-16.jpg)

Put the LINE Chat block on the edit screen. When the message is received, let the little monster say the LINE message. After the execution, you can use LINE to send the message to Webduino Bot. When the message is received, the little monster will say the message.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-17.jpg)

If you want to return the message, you only need to put the backhaul message, write the returned content (support text, expression map and picture, please refer to the above LINE Notify teaching), after receiving, you will receive the message. After returning the corresponding message, the example in the following figure will return the same message after receiving the message.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-18.jpg)

In addition to simply receiving messages, you can also use LINE Chat to control the development board. Through logical judgment, you can receive the "lights on" text and light the LED. When you receive the "red" command, it will emit red light to realize the real thing. Networked application scenarios.

![LINE Chat Control](../images/zh-tw/docs/webbit/extension/line-19.jpg)