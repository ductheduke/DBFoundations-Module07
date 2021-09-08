# SQL Functions

>Author: Duc Truong

>Date: September 8, 2021


## Introduction
This week, I learned more in depth about SQL Functions. The purpose of this memo is to document the use case of different types of SQL functions.

## When to Use a SQL UDF
A SQL UDF is a User Defined Function in SQL. It can be used to define a set of commands that will be repeated multiple times throughout the database so a UDF can be created to store and be called on to invoke those commands. A UDF can apply a set of SQL built-in functions to create a customized function for end users’ benefits.

## Differences between Scalar, Inline and Multi-Statement Functions
A Scalar UDF returns a single value as a result of performing the actions called by the function. Inline and Multi-Statement UDFs are two types of Table-Valued functions that return a table variable as a result of actions performed by the function, instead of returning a single value as in the case of a Scalar UDF. 

The difference between an Inline and a Multi-Statement Table-Valued functions is that an Inline function will only contain a single Select statement to output a table of values, while the Multi-Statement function will create a table variable and add values into that table via multiple insert and select statements so the table of values can be output after calling the function.

## Summary
When developing a UDF, the SQL developer should keep in mind the built-in functions within SQL Server that can be used to incorporate into their customized functions to fulfill the objective of their functions. Beside a Scalar UDF which only returns a single value, Inline and Multi-Statement table-valued functions are more complex in nature to output a table of values.
