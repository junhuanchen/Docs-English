#文字

In addition to displaying meaningful vocabulary, the text building block can also combine texts by adding them, or find corresponding words or letters in a vocabulary, or even display the content of speech recognition or the status of the Internet of Things serial sensor. .

## Text Block List

Text blocks have common text functions such as specifying text, line feed, conversion case, creating string, text tool, text search, text substitution, text conversion, etc.

![Text](../images/zh-tw/docs/webbit/basic/text-01.jpg)

## Specify text

The "specified text" building block can input the specified text for use by other building blocks.

![Text](../images/zh-tw/docs/webbit/basic/text-02.jpg)

For example, after the little monster talks the building block, the specified text is entered, and hello is entered. After the web page is executed, the little monster will say hello.

![Text](../images/zh-tw/docs/webbit/basic/text-03.jpg)

## Wrap

A "wrap" block can wrap a piece of text from a specified position.

![Text](../images/zh-tw/docs/webbit/basic/text-04.jpg)

##Create a string

The "Build String" building block can combine different text blocks into a single paragraph of text.

![Text](../images/zh-tw/docs/webbit/basic/text-05.jpg)

Click on the blue pinion to increase the text gap by dragging and dropping.

![Text](../images/zh-tw/docs/webbit/basic/text-06.gif)

By inserting the specified text block or line-changing block in the text gap, you can combine the words to be displayed, and you can see the difference between the combined text and the single-line text.

![Text](../images/zh-tw/docs/webbit/basic/text-07.jpg)

The creation of a string can also be used to combine two variables. For example, the variable a is hello and the variable b is world. By constructing a string, the two variables can be combined into a hello world of the intermediate line break.

![Text](../images/zh-tw/docs/webbit/basic/text-08.jpg)

## Add text after the variable

"Adding text after a variable" can change the content of the original variable so that the text of the original variable is followed by additional text.

![Text](../images/zh-tw/docs/webbit/basic/text-09.jpg)

Because it is based on "variables", if you want the little monster to talk, it will be rendered using variables.

![Text](../images/zh-tw/docs/webbit/basic/text-10.jpg)


## replace text

The "Replace Text" block can quickly replace some words in a paragraph with other text. The drop-down menu allows you to choose to replace the first specified text, or all specified text. (Replacing text does not change the variable, but produces a new piece of text)

![Text](../images/zh-tw/docs/webbit/basic/text-11.jpg)

The example below can change only the first "Apple" to "Carambola" or replace all "Apple" to "Carambola".

![Text](../images/zh-tw/docs/webbit/basic/text-12.jpg)

## Find the position where the string appears

"Finding the position of the string" will return the position where the specified text appears in a piece of text. You can select the first occurrence or the last occurrence.

![Text](../images/zh-tw/docs/webbit/basic/text-13.jpg)

The position where the text appears is judged by the number of words. In the example below, the orange of the orange is in the fourth position of the entire paragraph, so the number appears as 4, and the apple appears in the 10th position. If it is changed to English, the o bit of orange is in the 10th position, and the b bit of banana is in the 16th position.

![Text](../images/zh-tw/docs/webbit/basic/text-14.jpg)

## Get the text of the specified location

The "Get Text at the Specified Position" block will retrieve the text at the specified position. The drop-down menu has five specified positions, which are the first, the last, the first, the last, and the random position.

![Text](../images/zh-tw/docs/webbit/basic/text-15.jpg)

In the example below, the fourth word is orange and the eleventh word is fruit.

![Text](../images/zh-tw/docs/webbit/basic/text-16.jpg)


## Get the text of the specified interval

The "Get the specified range of text" block will take out the text within a specified interval. Note that the * first space number is smaller than the number in the second space.

![Text](../images/zh-tw/docs/webbit/basic/text-17.jpg)

In the example below, the texts in the 3rd to 8th are ", orange, watermelon", and the text from the 8th to the last is "melon, apple, banana, watermelon".

![Text](../images/zh-tw/docs/webbit/basic/text-18.jpg)


## Convert case

The "convert case" block can convert the "English word" to the upper and lower case, including all uppercase, all lowercase, or initial capitalization.

![Text](../images/zh-tw/docs/webbit/basic/text-19.jpg)

In the example below, you can convert all to uppercase, or only the first A is uppercase.

![Text](../images/zh-tw/docs/webbit/basic/text-20.jpg)


## Eliminate spaces

The "Erase Space" block eliminates blank characters on the left, right, or left and right sides of a paragraph.

![Text](../images/zh-tw/docs/webbit/basic/text-21.jpg)

## carry conversion

The "carry conversion" building block converts numbers into binary, octal, decimal or hexadecimal characters.

![Text](../images/zh-tw/docs/webbit/basic/text-22.jpg)

For example, the conversion of the number 200 to binary is 11001000, the conversion to octal is 310, and the conversion to hexadecimal is c8.

![Text](../images/zh-tw/docs/webbit/basic/text-23.jpg)

## text length

The "text length" building block can get the total number of words in a string of characters. The more important thing to note is that the English word is in "letter" and the blank is also a character.

![Text](../images/zh-tw/docs/webbit/basic/text-24.jpg)

For example, the length of the text of "One Apple" is 4, and the length of the text is 8 because "An apple" contains spaces.

![Text](../images/zh-tw/docs/webbit/basic/text-25.jpg)