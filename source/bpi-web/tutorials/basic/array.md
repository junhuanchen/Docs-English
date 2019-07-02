# Array

Arrays can combine numbers, literals, lists, or variables in order. These ordered collections are called arrays, an array can be subdivided into multiple elements, or an array contains other arrays for comparison. Complex operations are also implemented through the operation of the array.

## Array of building blocks

Array blocks include common functions such as building arrays, creating empty arrays, using arrays to create arrays, array values, and array editing.

![Array](../images/zh-tw/docs/webbit/basic/array-01.jpg)

## 空阵

The "empty array" building block creates an array container, which is an array that does not contain any elements.

![Array](../images/zh-tw/docs/webbit/basic/array-02.jpg)

If you want to use a variable to perform array operations, you must first define this variable as an array or an empty array, in order to add, delete, edit, etc. the array values ​​for this variable.

![Array](../images/zh-tw/docs/webbit/basic/array-03.jpg)

## Build an array

The "Build Array" building block can create an array with values ​​by placing the corresponding content in the specified location.

![Array](../images/zh-tw/docs/webbit/basic/array-04.jpg)

Click on the blue pinion to increase the gap in the content.

![Array](../images/zh-tw/docs/webbit/basic/array-05.gif)

Once the array is complete, you can tell the array through the little monsters (the array contents are separated by commas).

![Array](../images/zh-tw/docs/webbit/basic/array-06.jpg)

Or you can repeat the loop and repeat the contents of the array.

![Array](../images/zh-tw/docs/webbit/basic/array-07.gif)


## Creating a duplicate content array

The "Build Repetitive Content Array" building block can create a list of duplicate numerical repeats. Values ​​can be variables, text, numbers, or an array of arrays. When cooked into a gap, the array is created based on the number of times it is repeated.

![Array](../images/zh-tw/docs/webbit/basic/array-08.jpg)

For example, let the "Bale" text repeat five times and create an array, the green little monster will read the five guava words.

![Array](../images/zh-tw/docs/webbit/basic/array-09.jpg)

## Setting array content

The "Set Array Content" building block can perform three editing actions (set, insert, or remove) for the contents of the array (the first, last, first, last, and random).

![Array](../images/zh-tw/docs/webbit/basic/array-10.jpg)

For example, the original array has four kinds of fruit apples, willows, bananas, and guava. The first fruit element in the array is replaced with lotus fog by the "set array content" building block. The first array of green monsters speaks. The element becomes a lotus fog, then randomly removes one of the contents of the array, and the array of red monsters turns into only three fruits.

![Array](../images/zh-tw/docs/webbit/basic/array-11.jpg)

If you then use the "insert" peach element in the "last item", you can see that the array becomes four kinds of fruit, and the last one is peach.

![Array](../images/zh-tw/docs/webbit/basic/array-12.jpg)

## Get array content

The "Get Array Content" building block can take the value of an element in the array (the first, the last, the first, the last, and the random), or after removing the value of an element, remove the element.

![Array](../images/zh-tw/docs/webbit/basic/array-13.jpg)

If you simply get the value of an element, it will not affect the content and length of the original array, but if it is "removed after acquisition", the array will no longer contain this element, for example, there are four kinds of fruits at the beginning, if only Content, the array after the content is still four kinds of fruits, but if the content is removed after the acquisition, the array becomes only three kinds of fruits after the content is obtained.

![Array](../images/zh-tw/docs/webbit/basic/array-14.jpg)

## Looking for array content

The "Get Array Content" brick can find the location of a particular element from an array and return the number of that location.

![Array](../images/zh-tw/docs/webbit/basic/array-15.jpg)

By taking the array of blocks to get the fruit array, you can know that the apple is in the first position, the willow is in the second position, the banana is in the third position, and the baro is in the fourth position.

> Note that if you are "writing a program code" instead of using "building blocks", the first position is usually 0, and the second position is 1, because the first position in the program building block is displayed as usual. 1, the second position is 2, and so on.

![Array](../images/zh-tw/docs/webbit/basic/array-16.jpg)

## Array sorting

The "array sort" building block will sort the specified arrays by letters and numbers. After sorting, a new array will be formed, and * will not affect the sorting of the original array*.

![Array](../images/zh-tw/docs/webbit/basic/array-17.jpg)

As you can see from the example below, the green monster will tell the alphabet array (a, b, c, ...) after sorting by alphabet, while the red monster tells the original fruit array and is not sorted by the blocks. Impact.

![Array](../images/zh-tw/docs/webbit/basic/array-18.jpg)

If you choose alphabet sorting, it will be "* sorted first by letter, uppercase first, lowercase after, sorted by second letter* after sorting", if you choose not to be case sensitive, it will be sorted directly. * If the first letter is the same, use the second letter to sort *". In the example below, the uppercase A is sorted after the lowercase a, sorted, and then followed by 123, 456.

![Array](../images/zh-tw/docs/webbit/basic/array-19.jpg)

## Text and Array Conversion

The "Text and Array Conversion" building block converts text with "delimiters" (like blanks, commas, semicolons, etc.) into arrays, or merges arrays into a string of text.

![Array](../images/zh-tw/docs/webbit/basic/array-20.jpg)

If a string of text does not become an array, the second element will be the second word (the green monster will say "fruit"). If the text is split into an array, the second element will be in the array. The second content (the red little monster will say "Liu Ding").

![Array](../images/zh-tw/docs/webbit/basic/array-21.jpg)

Conversely, if you merge the array into text, you can leave the separator blank and you will see that the contents of the array become a whole string of text, without comma-separated characters. If you have a separator (such as a), you will see the combination. There is a in the middle of the text.

![Array](../images/zh-tw/docs/webbit/basic/array-22.jpg)

## Array length

The "array length" bricks can take the total number of elements in an array, and if it is an empty array, the array length is zero.

![Array](../images/zh-tw/docs/webbit/basic/array-23.jpg)

Because the array length represents the number of spaces in the array (how many elements can be placed in the array), if there are "spaces" but no elements are placed, the length of the array will still be affected, for example, an array of four spaces, but Only three kinds of fruit are put in, and the length of the array that is finally presented is 3.

![Array](../images/zh-tw/docs/webbit/basic/array-24.jpg)