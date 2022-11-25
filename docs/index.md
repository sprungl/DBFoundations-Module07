Name: Lauren Sprung
Date: 11/25/2022
Course: Foundations of Databases & SQL Programming
https://github.com/sprungl/DBFoundations-Module07
Assignment 7 – Functions

#H1 Introduction

In this week’s module, I learned about functions, both user defined and SQL Server functions. I practiced using a combination of SQL Server functions to create reporting views. I also practiced creating user defined functions with parameters. 
When to Use a SQL User Defined Function (UDF)
User defined functions are useful when there are not already existing SQL functions that can do the desired operation. In particular, UDFs are useful when you want to return a scalar that can be used in the Select clause of a Select statement or if you want to return a table based on user inputted parameters. Unlike views, a function can return a single (scalar) value. This allows them to be used is the Select clause, whereas a view can only be used in the From clause of a Select statement. Figure 1.1 shows an example of using a User Defined function fMultiply, that returns the value of the two input parameters multiplied together, in the Select clause. 
 
Figure 1.1 Code showing the use of a User Defined function fMultiply in the Select clause. 
Another use of a UDF is to return tables based on user inputted parameters. Views do not take input parameters and stored procedures cannot be used as a table in a From clause, making a function the right choice in this case. Figure 1.2 shows the creation of the function fMultiply used in figure 1.1. 
 
Figure 1.2 Code creating the UDF fMultiply
Differences between Scalar, Inline, and Multi-Statement Functions
As discussed above, a scalar function is a function that returns a single value. These functions will usually take a parameter and return the corresponding value after the function is executed using that parameter. Scalar functions are unique in that they can be used in the From clause of a Select statement or as a check constraint for a column. Figures 1.2 and 1.1 show the creation and use of a scalar function, respectively. 
Unlike scalar functions, inline and multi-statement functions both return tables. Inline Functions are single statement functions. Figure 2.2 shows the code to create an inline function. For an inline function, the Begin/ End keywords are not required. 
 
Figure 2.1 Code to create an inline SQL function with parameters
Like the name suggests, a multi-statement function can have more that one statement. Figure 2.2 shows the code to create a multi-statement function. In a multi-statement function, the Begin/ End keywords are required. It is also required to explicitly specify the structure of that table that is returned after the Returns keyword. Lastly, the Return keyword is called after the function statements and before the End keyword. 
 
Figure 2.2 Code to create a multi-statement SQL function with parameters
Summary
In this module, I dived deeper into SQL Functions. I practiced using built-in SQL functions and created my own functions. I learned about scenarios where you would use each type of user-defined function. I look forward to next week to dive deeper into stored procedures. 
