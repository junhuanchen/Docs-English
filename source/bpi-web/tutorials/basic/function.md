#函

Functional building blocks can help us simplify or manage more complex program logic, because when writing a program, we often encounter code that needs to be written and executed repeatedly. If we have to rewrite it once every time, it will inevitably cause the whole program. The complexity of the logic, through the function of the centralized management of these repeated procedures, you need to use the call function, you can execute the corresponding content.

## Functional building blocks list

The function building block is pre-configured with three blocks, which are to establish a function, to establish a function with a return value, to judge within the function, and to return the value.

![Function](../images/zh-tw/docs/webbit/basic/function-01.jpg)

##Build function

The "Building Function" building block can be used to package a number of program blocks that are used repeatedly.

![Function](../images/zh-tw/docs/webbit/basic/function-03.jpg)

Using the building function * does not execute the function *, because the function is * defines "content to be executed" *, after the completion of the function building block content, in the directory of the function building block, the corresponding * Execute the function building block*, using this building block to indicate the execution of this function.

![Function](../images/zh-tw/docs/webbit/basic/function-02.jpg)

After the two functions a and b are created, use the *call functions a and b*. After the web page is executed, the green monster will say the apple, and the red monster will say the banana. (*If you simply create a function without calling, nothing will happen after execution*)

![Function](../images/zh-tw/docs/webbit/basic/function-05.jpg)

In addition to simply using the function, we can also create a "variable* in the * function" and click on the pinion in front of the building block to add a variable.

![Function](../images/zh-tw/docs/webbit/basic/function-06.gif)

After adding a variable in the function, you will also see the gap in the value of the variable when you execute the function. (There are several gaps in variables in several functions)

![Function](../images/zh-tw/docs/webbit/basic/function-07.jpg)

The variables in the function add a lot of flexibility to the program, and can also reduce a lot of heavy code. For example, through the function and the variables in the function, you can make a value by adding the value of the variable. formula.

![Function](../images/zh-tw/docs/webbit/basic/function-08.jpg)

## Creating a function with a return value

The "Build a function with a return value" building block can make the executed function a simple value, which is quite helpful for some complex program applications.

![Function](../images/zh-tw/docs/webbit/basic/function-09.jpg)

If you are using "Build a function with a return value", you will find that there is one more shape in front of the building block for the combination. (The following figure shows the function of creating a variable with a function before extending the previous section)

![Function](../images/zh-tw/docs/webbit/basic/function-10.jpg)

Through the variables in the function and the values ​​returned by the function, different values ​​(x and y different values) can be obtained according to the variables provided, and different results are produced.

![Function](../images/zh-tw/docs/webbit/basic/function-11.jpg)

## Function to judge and return value

The "Judgement and return value in the function" block must be matched with the building block of "Build a function with a return value", mainly used to determine what value to return. (This brick must also be placed in the function to function properly)

![Function](../images/zh-tw/docs/webbit/basic/function-12.jpg)

Through this building block, with the variables in the function, you can pass the value of the variable passed in, and finally return the larger result of x and y.

![Function](../images/zh-tw/docs/webbit/basic/function-13.jpg)

Because the "judge and return value in the function" building block has the function of logical judgment, you can also use the logical building block plus a variable to make the judgment, you can make the same effect.

![Function](../images/zh-tw/docs/webbit/basic/function-14.jpg)