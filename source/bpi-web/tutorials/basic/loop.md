#重复

In the field of programming, repetition (loop) is a basic function that is often used. Repeating the name is the process of repeated execution. It can also put the code that needs to be executed repeatedly in the loop, and can specify the number of times, delay time, or none. Exhaustive execution.

## Repeating list of blocks

The duplicate blocks have a "waiting" building block, five different repeating pattern blocks and a "stop repeating" building block.

![repeat](../images/zh-tw/docs/webbit/basic/loop-01.jpg)

## Waiting

The "waiting" building block allows us to pause the program for a specified period of time. When the waiting block is encountered in the program building block, it will wait for the specified time before proceeding.

![repeat](../images/zh-tw/docs/webbit/basic/loop-23.jpg)

In the following example, if you don't wait, the four little monsters will say hello at the same time. If you wait for 1 second, the four little monsters will say hello every second.

> Note that the so-called "simultaneous" above is for the human eye. For the program, it is still in order, but the interval is very short, so short to the human eye can not distinguish it.

No waiting for building blocks

![repeat](../images/zh-tw/docs/webbit/basic/loop-02.jpg)

Plus plus waiting blocks

![repeat](../images/zh-tw/docs/webbit/basic/loop-03.gif)

## Repeated several times

The "Repeat execution" block can specify the number of times the block program in the loop is repeated, the preset number of times is 10.

![repeat](../images/zh-tw/docs/webbit/basic/loop-06.jpg)

By repeating ten times, you can make the little monster rotate 100 degrees.

![repeat](../images/zh-tw/docs/webbit/basic/loop-04.jpg)

Continuing the wait described earlier, if you don't wait in the repeat, you will see the monster rotate 100 degrees in an instant. If we add a block waiting for 0.5 seconds, we will see the monster rotate 10 degrees every 0.5 seconds, rotate. ten times.

![repeat](../images/zh-tw/docs/webbit/basic/loop-05.gif)

## Counting

The "count" building block is somewhat similar to the advanced version of the "repeated execution" block. The difference is that the counting block uses a variable. By changing the value of this variable, you decide how many times to repeat, how to repeat, and the interval between repetitions.

> Because there is a variable in it, when there are counted blocks in the edit screen, a corresponding variable will appear in the variable directory.

![repeat](../images/zh-tw/docs/webbit/basic/loop-07.jpg)

Use "Counting Blocks with Waiting" to let the green monster tell the value of the variable i every 0.5 seconds. This variable i will be incremented or decremented by the value of the starting value, final value and interval we specify. In the example of the figure, the variable i is summed every 1 until it becomes 10 (and 1234...10 will be read in order).

> Note that * If you want to read the numbers "in order", you must add the waiting blocks *, or you will present the last number.

![repeat](../images/zh-tw/docs/webbit/basic/loop-08.gif)

## Repeat unlimited times

The "repeated infinite" building blocks will continue to execute the loop content indefinitely, and the repeated events will stop unless you use "stop repeating".

![repeat](../images/zh-tw/docs/webbit/basic/loop-09.jpg)

Continuing the wait described above, adding "waiting" to the infinite number of blocks, with the rotation of the little monster, allows the little monster to rotate continuously.

![repeat](../images/zh-tw/docs/webbit/basic/loop-10.gif)

## Judging as true, repeating unlimited times

"If the judgment is true, repeat it indefinitely." The building block is equivalent to the "repeated infinite" building block plus the "logical" judgment. * As long as the logic in the space is judged as "true" (true), infinite repetition* will begin.

![repeat](../images/zh-tw/docs/webbit/basic/loop-11.jpg)

For example, we can first set a variable a to a number between 2 and 9. By judging if a is an even number, let the little monster start to rotate, otherwise it will not rotate.

![repeat](../images/zh-tw/docs/webbit/basic/loop-12.gif)

The above example can also use "logic" with "repeated infinite times" to achieve the same effect.

![repeat](../images/zh-tw/docs/webbit/basic/loop-13.jpg)

## Take out array elements and execute

Different from the above repeated method, the "removing array elements and executing" building blocks is based on the length of the array as the basis of the number of repetitions. Therefore, the array blocks must be placed in the spaces. After the web page is executed, the array contents are sequentially taken out and the corresponding actions are performed.

![repeat](../images/zh-tw/docs/webbit/basic/loop-14.jpg)

We can set the variable a to an array with five fruit names, then set a variable i, let the variable i equal the fruit name, and let the little monster speak the fruit name and rotate it.

![repeat](../images/zh-tw/docs/webbit/basic/loop-15.gif)

## Background execution

"Background execution" is a function option in all the repeating blocks. Due to the execution order of the program code, "** The previous program cannot be executed until the previous program has not been completed**", and therefore * most of the cases are on the screen. Only one repeat loop* can be executed at the same time. However, background execution** allows repeated actions to enter the background, and multiple repeat loops** can be used at the same time.

![repeat](../images/zh-tw/docs/webbit/basic/loop-17.jpg)

For example, if we use two "repeated ten times" blocks, *do not check the background execution*, the first one is placed into the little monster to rotate, the second is placed into the small monster to move, after the web page is executed, See the little monster * rotate and move * first.

![repeat](../images/zh-tw/docs/webbit/basic/loop-18.gif)

If we repeat the above example, * check the background to execute *, after the web page is executed, you will find that the little monster * rotates while moving *.

![repeat](../images/zh-tw/docs/webbit/basic/loop-19.gif)

Whether there is background execution, it is easier to find the difference in the case of "repeated infinite times", **If there are two loops in the screen that are repeated infinitely, if the background execution is not checked, because the behavior stays in the previous repeat Unlimited times, indefinitely after the repetition will not execute **.

![repeat](../images/zh-tw/docs/webbit/basic/loop-20.gif)

## Stop repeating

All of the above repetitive behaviors can be stopped by the "stop repeating" building block, and the repetition is divided into "*stop all repeats on the screen*", or "* is placed in the repeating loop, and the repetition of the position is stopped*".

![repeat](../images/zh-tw/docs/webbit/basic/loop-16.jpg)

For example, if you add the "Small monster rotation angle greater than 90 degrees* stop this repetition*" in the "Repeat Unlimited" building block, it will stop repeating when the small monster angle is greater than 90 degrees, and continue to execute the following speech program.

![repeat](../images/zh-tw/docs/webbit/basic/loop-21.gif)


If there are multiple repetitions, you can also use Stop All Repeats to stop. For example, if the small monster rotates more than 90 degrees, all repetitions will be stopped. (The background execution is checked here, please refer to "[Background Execution] (loop.html#loop07)")

![repeat](../images/zh-tw/docs/webbit/basic/loop-22.gif)