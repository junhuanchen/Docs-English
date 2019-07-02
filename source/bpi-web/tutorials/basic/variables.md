# variable

Variables, which are the basic elements used by all programs, give the variable a name before use, and then use this variable to represent text, numbers, arrays, colors, or logic. Why use variables? Because editors often encounter many "duplicate" parts, if you use variables or functions to load these duplicates, you can easily add, delete, or modify them "once".

For example, if an article has 50 "A", change "A" to "B". If you do not use the variable, you have to manually modify it 50 times (you can replace it without considering the search software). Function), but if we use "variable a equals A" today, we only need to do one action when modifying: "put variable a equal to B", you can replace all "A" with "B". The content will be introduced in depth.

## Adding variables

The first step in using the variable is to add a new variable, open the editor, drag the block of "*set variable to *" to the screen, select the "*new variable*" from the drop-down menu, and click the pop-up dialog window. , enter the name of the new variable and add a variable. (It is recommended to name the variable as "English + number" as much as possible)

![variables](../images/zh-tw/docs/webbit/basic/variables-01.jpg)

Add the corresponding value (value can be text, number, array, color, or logic) after the new variable. This variable is equivalent to this value. If no value is assigned, this variable is an empty variable.

![variable](../images/zh-tw/docs/webbit/basic/variables-03.jpg)

After adding a variable, you will also see the new variable building block in the variable directory of the left side building list.

> Note that if there is no building block with the setting variable XXX in the editing screen, the variable building block of XXX will not be seen in the building block list.

![variables](../images/zh-tw/docs/webbit/basic/variables-02.jpg)

## Setting variables

The setting variable indicates that the variable is assigned a value, and the usage is the same as the newly added variable. Since the programming language has the feature of "* followed by the front *", * if the variable name is the same, the value set later overrides the previously set value * In the example of the following figure, the last value of the variable apple is 456.

![variables](../images/zh-tw/docs/webbit/basic/variables-04.jpg)

## Rename variable

Different from "Add Variable", renaming a variable can rename all the variables in the screen at a time. For example, four apple variables appear in the screen. By renaming, you can replace all four apple variable names with ball.

![variables](../images/zh-tw/docs/webbit/basic/variables-05.gif)

## Changing variables

Change the variable to indicate "* how much the value of the variable changes *", assuming that the value of the original variable is 1, and after changing the variable 1, the variable will become 2. Similarly, if you use the change variable -1, then the variable will It becomes 0.

![variables](../images/zh-tw/docs/webbit/basic/variables-06.jpg)

Note that if it is a different type of change, for example, the original variable is the word "apple", but the quantity "1" is changed, and the result is "Apple 1". Similarly, if the variable is "1", The result of changing the text "Apple" is "1 Apple".

![variable](../images/zh-tw/docs/webbit/basic/variables-07.jpg)

## Using variables

After adding a new variable or setting a variable, you can use the variable in the editing area. The following figure is an example. First, set a variable to 1, b variable to 2, and then calculate a + b or a divided by b. Mathematical operations, or through logic to determine which values ​​a and b are relatively large, when the program logic becomes more and more complex, it has to be implemented by different variables.

![variables](../images/zh-tw/docs/webbit/basic/variables-08.jpg)