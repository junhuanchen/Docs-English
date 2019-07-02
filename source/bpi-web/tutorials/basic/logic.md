# logic

In daily life, whether it is writing programs, mathematics, court offense and defense, or even traffic on the road, buying or selling things, or getting up, there are many "logic" components. The logic can do many conditions and judgments. Some conditions will perform something, such as hearing the alarm ringing, getting up, seeing the green light to travel, etc., etc., is a simple logical judgment.

## Logic building list

The logical building blocks are respectively composed of a main building block "If...execution..." (the building blocks with blue pinions in front), with nine logically judged building blocks (judgment, logical operator, digital type, empty Value, inclusion value, true and false value, etc.).

![Logic](../images/zh-tw/docs/webbit/basic/logic-01.jpg)

## Logic judgment

The "logical judgment" building blocks are pre-configured with two types of assembly "gap". The smaller one is "judgment condition", and the larger one is "execution content", which means * if the situation satisfies the judgment condition (decision back) Passing "true" or "true" will execute the corresponding content*.

![Logic](../images/zh-tw/docs/webbit/basic/logic-02.jpg)

Click on the *blue pinion* at the top left to add a logical judgment condition. Click to open it, then click it to close it.

![Logic](../images/zh-tw/docs/webbit/basic/logic-03.gif)

There are three kinds of logical judgment conditions: * "If" must be in the first layer, "Otherwise if" is in the middle, "Otherwise" must be in the last *, "Other" judgment condition means "If" and "Otherwise" If the conditions are not met, the "other" content will be executed.

![Logic](../images/zh-tw/docs/webbit/basic/logic-04.jpg)

If there are only * two conditions*, such as non-A or B, you can simply use "if" and "otherwise", or even "otherwise", so that no action will be taken outside the condition.

![Logic](../images/zh-tw/docs/webbit/basic/logic-05.jpg)

## Judging conditional

Judging conditional conditions are mainly placed in the logical "judgment condition" gap, providing logical judgments of different situations. The conditions for judgment are mainly divided into: equal to (=), not equal to (≠), less than (<), less than or equal to (≦ ), greater than (>), greater than or equal to (≧).

![Logic](../images/zh-tw/docs/webbit/basic/logic-06.jpg)

The method of use is as long as the building block of the judgment condition is placed in the gap of the judgment condition.

![Logic](../images/zh-tw/docs/webbit/basic/logic-08.jpg)

For example, you can first add a random integer with a variable a between 0 and 100, and let the green monster tell the number, and then use logic to judge if the variable a is greater than 60 (the return is judged as "true"). Let the red monster say "pass", otherwise it will say "fail", you can see the corresponding result after executing the program.

![Logic](../images/zh-tw/docs/webbit/basic/logic-09.jpg)

## Logical operator

The "Logical Operator" building block provides a more flexible judgment condition for logical judgment, including "* and *" and "* or *". If "and" is used, the conditional spaces judged at both ends must be satisfied. The action will be executed. If you use "or", the action will be executed as long as one of the conditional spaces is satisfied.

![Logic](../images/zh-tw/docs/webbit/basic/logic-10.jpg)

Usually, when "if not" appears in the logical judgment, the logical operator is used, and the logical operator is often used in conjunction with the building block of the judgment condition. (Sometimes you will encounter only "otherwise, if" with logical operators)

![Logic](../images/zh-tw/docs/webbit/basic/logic-11.jpg)

In the example just mentioned, it can be increased to four judgment conditions, namely 0, 1~59, 60~99 and 100. When the judgment condition is established, the little monster will be told the number and the corresponding text.

![Logic](../images/zh-tw/docs/webbit/basic/logic-12.jpg)

## Judging the number type

The "judge digital form" building block can help us quickly determine * odd, even, integer, number with decimal point, text or array *.

![Logic](../images/zh-tw/docs/webbit/basic/logic-13.jpg)

As far as usage is concerned, it can be placed directly into the gap of the judgment condition.

![Logic](../images/zh-tw/docs/webbit/basic/logic-14.jpg)

For example, we can set the variable a to divide by two random numbers, and then tell the integer or decimal through the little monster. (Divided building blocks use "multi-line input", you can right-click on the building block to select multi-line input, teaching reference: [programming block tips] (../info/interface.md#tips)

![Logic](../images/zh-tw/docs/webbit/basic/logic-15.jpg)

## Judging null values

The "judge empty value" building block is mainly for matching with the "array" building block. * If it is a null value, it returns true, otherwise it returns false*.

![Logic](../images/zh-tw/docs/webbit/basic/logic-16.jpg)

There are several cases where null values ​​are generated: "*no text, number 0, empty array, null value, false (false), variable with no value *", if it is judged whether these conditions are empty, it will return true. .

![Logic](../images/zh-tw/docs/webbit/basic/logic-17.jpg)

## Determine if text is included

"Judge whether text is included" blocks can check whether a * or a specified paragraph is included in a paragraph of text.

![Logic](../images/zh-tw/docs/webbit/basic/logic-18.jpg)

For example, if you check "You are my little apple" and there is "Find a small apple", the green monster will say "Little Apple", otherwise if it is "Little Lemon", the red monster will say " No small lemons."

![Logic](../images/zh-tw/docs/webbit/basic/logic-19.jpg)

## Not

"Non" blocks are literally "not what" and are usually used in conjunction with "true/false" or "null" blocks.

![Logic](../images/zh-tw/docs/webbit/basic/logic-20.jpg)

If the bricks are connected behind the "non" bricks, the state will be reversed. For example, the space will become non-empty, the truth will become false, the fake will become true, and so on.

![Logic](../images/zh-tw/docs/webbit/basic/logic-21.jpg)


## True / False

The "true/false" building blocks mainly represent the values ​​of ture (true) and false (false). The purpose is to make more judgments than numbers and texts when making judgments. It is also possible to submit ture and false to variables. It is also quite easy to use in some situations.

![Logic](../images/zh-tw/docs/webbit/basic/logic-22.jpg)

## None

When writing a program, sometimes a variable is encountered or a value becomes null ( null ). At this time, you can use the building block of the null value. The usage is similar to the usage of "true/false".

![Logic](../images/zh-tw/docs/webbit/basic/logic-23.jpg)

## Ternary logical operation

The "Ternary Logic Operator" building block is for "only two conditions*" and returns one of the "two expressions" according to the condition.

![Logic](../images/zh-tw/docs/webbit/basic/logic-24.jpg)

If you use the above-mentioned pass and fail examples, because there are only two conditions, you can easily achieve through the ternary logic operator, and you can use less building blocks to achieve the same result.

![Logic](../images/zh-tw/docs/webbit/basic/logic-25.jpg)