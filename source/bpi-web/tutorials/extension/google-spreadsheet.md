# Google Trial Balance

With the Google Spreadsheets feature of the editor, you can use the Google Spreadsheet as a repository to store the value of the signal received by the sensor or to display the data from the spreadsheet through the development board.

## Create and set trial balance permissions

Before using the editor to operate Google Spreadsheets, * you must first create a trial balance and set up your trial balance*, so first sign in to your Google Drive with your Google Account and create a brand new blank spreadsheet on your Drive.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-01.jpg)

After opening the trial balance, enter the spreadsheet name in the upper left to complete the action of creating a Google trial balance. * "Trial Balance" indicates the entire trial balance. Each trial balance can contain many "worksheets"*. Different names can be given separately.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-02.jpg)

Click "Share" in the upper right corner of the spreadsheet to set the permissions for the trial balance.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-03.jpg)

Open the sharing settings window and click "Advanced".

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-04.jpg)

Each newly created trial balance is "Private - only you can access", click on "Change" to set it.

![Google spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-05.jpg)

By setting the permission of the spreadsheet to * "any user who knows the link", you can "edit" *, press Save, and the permissions of the spreadsheet are set.

![Google spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-06.jpg)

## Google Trial Balance Checklist

Google spreadsheets include trial spreadsheet initialization, reading data, writing data, deleting columns or columns, adding columns or columns, and more.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-07.jpg)

## Trial Balance Initialization

The "Trial Balance Initialization" building block allows you to set the trial list's URL and worksheet name. Before you can run any function of the spreadsheet, you need to use the spreadsheet initialized by the spreadsheet.

> Note, please do not fill in the name of the "Trial Balance" in the name of the "Worksheet".

![Google spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-08.jpg)

## Write data

The "write data" brick can write data to the spreadsheet and can specify to write from the first column above or put the data in the last column.

> The data building block belongs to the type of "* will continue to execute the program after writing data*". When there is this building block in the editing screen, * when the program encounters this block, it will pause until the data is written. Will continue to *.

![Google spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-09.jpg)

Click on the blue pinion in front of the building block to increase the number of fields in which the data is written.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-10.gif)

First use the initialization spreadsheet to fill in the spreadsheet of your trial balance, and then put the building blocks of the data. After execution, you will see the time and text in the spreadsheet.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-11.jpg)

With the repeated loops, you can continuously write data to the spreadsheet.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-12.jpg)

## Specify the cell to write data

"Specify cell write data" can be used to write data to a specified cell. The format supports data in a two-dimensional array format in addition to a single value.

> The specified storage grid is written to the data type of "* will continue to execute the program after writing *". When there is this brick in the editing screen, * when the program encounters this block, it will pause until the data is executed. It will not continue until after writing.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-13.jpg)

In the example below, after execution, the word "write data" will be written in the b2 cell.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-14.jpg)

In addition to specifying a single cell, this building block also supports the "range" cell and the "two-dimensional array" data format*. For example, to write data to the range of `a1:b3`, you need to use `[ [a,b],[c,d],[e,f]]` Two-dimensional array data, *The first layer of the two-dimensional array is a column (1, 2, 3...), and the second layer is Horizontal bar (A, B, C...)*.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-15.jpg)

In the example below, after execution, a is written to A1, B1 is written to b, A2 is written to c, B2 is written to d, and so on.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-16.jpg)


## Reading data

The "Read Data" building block can read the number of a single cell, the entire worksheet, or the last column and the last column.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-17.jpg)

The "Read Data" building block belongs to the type of "*Reading will continue to execute the following program*" (click on the small question mark in the front of the question icon will be prompted), when there is this building block in the editing screen, * when the program encounters this The block will be suspended until the data is obtained.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-18.jpg)

First prepare a trial spreadsheet with information. The example below uses the title and name of the Avengers.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-19.jpg)

If you use the "Read Single Cell" block, you can let the little monsters tell the contents of the corresponding cell after reading the data.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-20.jpg)

If you need to read more data, it is recommended to use the "read all data" building block, the data read by the building block, * will be presented in a "two-dimensional array" *, so you can use the array of blocks to operate, The following example, with repeated loops, will allow the little monsters to read the names and names of the Avengers members in order after reading the data.

> The first layer of the two-dimensional array of data is the column (1, 2, 3...), and the second layer is the column (A, B, C...)*.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-21.gif)

In addition to the content of the data, the information obtained also includes the last column and the last column of the data. The corresponding number can be obtained through the relevant building blocks (the horizontal field is represented by numbers, a corresponds to 1, b corresponds to 2, and so on). For example, the contents of the Avengers member trial balance table, the last column obtained is 7, and the last column is 2.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-22.jpg)


## Deleting columns or columns

The "Delete column or column" block can delete a column or column of a range, the column number is represented by a number, and the column number is expressed in English.

> The column of the deleted column or column belongs to the type of "* will continue to execute the program after deletion*". When there is this block in the editing screen, * when the program encounters this block, it will pause until the column is deleted or It will not continue until after the column.

![Google Spreadsheet] (../images/zh-tw/docs/webbit/extension/google-spreadsheet-23.jpg)

## Add column or column

The "Add column or column" building block can add a column or column of the interval. The column can be selected to increase above or below, and the column can be selected to increase to the left or to the right.

> Increase the column of the column or column to be of the type "* will continue to execute the program after the increase*". When there is this block in the editing screen, * when the program encounters this block, it will pause until the column or column is added. It will not continue until after the column.

![Google Spreadsheet](../images/zh-tw/docs/webbit/extension/google-spreadsheet-24.jpg)