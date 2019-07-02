# Math

Mathematical building blocks contain many mathematical operations, from basic addition, subtraction, multiplication and division, to rounding, mean, median, etc., whether it is a simple program or a complex application, can be achieved through a variety of mathematical operations.

## Math Block List

The mathematical building blocks include common mathematical expressions such as numbers, arithmetic expressions, basic functions, sums, random numbers, and scale conversions.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-01.jpg)

## Specify a number

The "specified number" building block is used to enter numbers, either integers or floating point numbers with a decimal point, which are often used in arithmetic or judgment.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-02.jpg)

## Get a random integer in the range

The "Get random integers within range" block specifies a range of numbers from which a random integer is taken each time the block is executed.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-03.jpg)

With repeated infinite times and waiting for blocks, you can let the little monster say a random integer every second.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-05.gif)

## Get random scores

The "Get Random Score" building block randomly acquires a floating point number between 0 and 1 at each execution.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-04.jpg)

With repeated infinite times and waiting for blocks, you can let the little monster say a random floating point number every second.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-06.gif)

## computation

The "mathematical operation" building blocks can be added, cut, multiplied, divided, and sub-calculated for numbers.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-07.jpg)

If you use multiple mathematical operations, you need to be aware that * each computational building block will use parentheses in calculations. Similar expressions may result in different results*. For example, the following figure shows that the blocks are all 5 + 2 x 2, However, the results obtained are different because of the position of the brackets.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-08.jpg)

Mathematical operations can be used to add variables, in addition to variables. For example, the variable a is 5 and the variable b is 3. You can calculate a + b equal to 8 through mathematical operations.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-23.jpg)

## Get the remainder

The "mathematical operation" building block can take the remainder of the division of two numbers.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-09.jpg)

## Limiting the range of numbers

The "Limited Number Range" block sets the maximum and minimum values ​​and limits the number to this specified range.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-12.jpg)

## Rounded

The "rounding" building block can round off, unconditionally round, or unconditionally carry numbers with floating point numbers, and can also choose to round or carry to the first decimal point.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-10.jpg)

The result of rounding off, the number that needs to be rounded off, is placed behind the rounded blocks.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-11.jpg)

## Scale conversion

The "scale conversion" building block can convert the value in a certain scale interval to the corresponding value of another interval scale.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-13.jpg)

For example, 0.5 is the value of the 0~1 scale interval, and the result obtained by converting to the 0~100 scale interval is 50.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-14.jpg)

Scale-converted building blocks can help us with many of the more complex scale conversions. For example, 0.5 is between -5 and 5, and the value converted to between 250 and 400 is 332.5.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-15.jpg)

Scale conversion blocks are often used in conjunction with rounded blocks. * It is recommended to place the rounded blocks in front of the scale conversion blocks*, since the scaled values ​​may have decimal points, and rounding them up to get a more accurate answer.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-16.jpg)

## Array Operations

The "array operation" building block can be used to add, extract the minimum value, take the maximum value, calculate the average value, obtain the median, obtain the comparison mode, calculate the standard deviation, and calculate the random extraction for the array composed of numbers.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-17.jpg)

After the array operation is connected to the array block, you can start row value or operation.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-18.jpg)

## Common Math Functions

"Common Math Functions" provides commonly used mathematical calculation blocks. Common mathematical functions include the following: root number, absolute value, negative number (-), logarithmic function (ln), log10 function (log10), exponential function (e^) And 10 times (10^).

![Mathematics](../images/zh-tw/docs/webbit/basic/math-19.jpg)

## Trigonometric function

The "trigonometric function" building provides two trigonometric functions, namely the angle ( sin, cos, tan ) and the diameter ( asin, acos, atan ), and the trigonometric function can be switched from the pull-down menu.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-20.jpg)

Note that because of the JavaScript page language feature, in some cases when using a trigonometric function, the decimal point will become an infinite loop 9999, for example, sin(30) should be equal to 0.5, but it will become 0.49999..., when this happens, you need to use The rounding approach can deliver the expected results.

![Mathematics](../images/zh-tw/docs/webbit/basic/math-21.jpg)


## constant

The "constant" building block will be a constant value that does not change. The constant contains the following types: pi (π), exponent (e), golden ratio (φ), sqrt(2), sqrt(1⁄2), and infinity. Big (∞).

![Mathematics](../images/zh-tw/docs/webbit/basic/math-22.jpg)