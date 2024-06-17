POWER BI DAX FUNCTIONS
ADDCOLUMNS 
It adds the calculated columns to the given table or table expression.
syntax    ->ADDCOLUMNS(<TABLE>,<>NAME>,<EXPRESSION>,[<NAME>,<EXPRESSION>]...)
table->it returns a table.
name->the name specifies the column.
expression->Dax expression that needs to perform on each row.
return value
a table it's original columns with added columns.
------------------------------------------------------------------------------------------
AVERAGE
It returns the arithmetic mean of the column.
syntax -> AVERAGE(<COLUMN>)
column -> the column which you want the average.
return value
it returns a decimal value.
note:
1.if there are any blank or logical values it will ignore them.
2.if any cell contains 0. it will take for the calculation.
3.suppose, in table if there are no values present then function will return blank. and if there are values and it does not meet the criteria the it returns the 0.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
AVERAGEA
It returns the average of the values in a column. handles the text and non-numeric values.
syntax -> AVERAGEA(<COLUMN>)
return value
it returns a decimal number.
note:
1.value that evaluates to TRUE is 1.
2.value that evaluates to FALSE is 0.
3.values that contains nonnumeric text also 0.
4.empty text counts as 0.
---------------------------------------------------------------------------------------------------------------------------------------------------------------------
AVERAGEX
It returns the average of a set of expressions evaluated over a table.
syntax-> AVERAGEX(<TABLE>,<EXPRESSION>)
Return value
it returns a decimal number 
note:
it is also same as the average function it does not accept the null values and non numeric values.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
COUNT
It counts the number of cells in a column which contains numeric values or numbers.
syntax-> COUNT(<COLUMN>).
Return value
it returns the whole number.
note:
->IT DOES NOT SUPPORT THE BOOLEAN VALUES.
1.The count function counts the rows that contain the following values
     ->numbers.
     ->dates.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 COUNTA 
It returns the number of cells containing not only numeric values but also text,non-blank values etc.,
it supports all data types.
syntax-> COUNTA(<COLUMN>)
return value
it returns a whole number.
note:
When the function does not find any rows to count, the function returns a blank. When there are rows, but none of them meet the specified criteria, then the function returns 0.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
COUNTAX
It counts nonblank results when evaluating an expression over a table, it just works like countax function. but when counting the non-blank cells the empty cells are also counted.
syntax-> COUNTAX(<table>,<expression>)
return value
It returns the whole number.
note:
1. it supports the boolean values.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
COUNTX
Counts the number of rows that contains a number or expression evaluates to a number over a table.
syntax->COUNTX(<TABLE>,<EXPRESSION>)
return value
it returns a whole number.
note:
1. it does not support for the boolean values.
2. parameters that are logical or text cannot be counted.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 COUNTBLANK
Counts the no of blank cells in a column.
syntax-> COUNTBLANK(<COLUMN>)
Return value
a whole number.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
COUNTROWS
IT IS USED TO COUNT NO OF ROWS IN A TABLE OR EXPRESSION THAT GIVES A TABLE.
syntax-> COUNTROWS(<TABLE>)
RETURN VALUE
it returns a whole number.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
CROSSJOIN
it is used to create single table from combining different tables together.
syntax->CROSSJOIN(<TABLE1>,<TABLE2>,<TABLE3>...)
return value 
a table containing all columns of combining parameter tables.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
DISTINCTCOUNT
It counts the distinct values from column.
syntax-> DISTINCTCOUNT(<COLUMN>)
return value
it returns the whole number.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MAX
it returns the largest value of the column.
syntax-> MAX(<COLUMN>)
Return value
a whole number.
note:
1. it supports only numeric values and dates.
2. empty cells, logical values and text are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MAXA
It returns the largest value from the column. 
syntax->MAXA(<COLUMN>)
return value
a decimal number.
note:
1. numbers ,dates and logical values are considered.
2. empty values are ignored.
3. if column contains no values MAXA returns 0.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MAXX 
Evaluates an expression for each row of a table and returns the largest numeric value.
syntax->MAXX(<TABLE>,<EXPRESSION>).
return value
returns a decimal number.
note:
1. it supports only numeric values and dates.
2. empty cells, logical values and text are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MIN
It returns the minimum value from the given column.
syntax-> MIN(<COLUMN>).
return value
a decimal number.
note:
1. it works only for dates and numeric values.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MINA
It returns the smallest from the column including any logical values or number written as text.
syntax->MINA(<COLUMN>)
return value
returns a decimal number.
note:
1. it supports for numeric values and dates.
2. supports for text that can be converted to numeric values.
3. it also supports for logical values.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MINX
it returns the minimum number from the given column over the given expression.
syntax->MINX(<COLUMN>)
return value
a decimal number.
note:
1. only numbers are counted. other than that if there are any values, MINX returns 0.
2. logical values ,text and empty cells are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 PRODUCT
It returns the product of numbers in a column.
syntax->PRODUCT(<COLUMN>).
return value
it returns the decimal number.
note:
1. blank,text and logical values are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
PRODUCTX
It returns the product of numbers in a column from an expression evaluated for each row in a table.
syntax->PRODUCTX(<TABLE>,<EXPRESSION>).
return value
it returns the decimal number.
note:
1. blank,text and logical values are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
ROW 
Returns the single row containing values resulted from the expression.
syntax->ROW(<NAME>,<EXPRESSION>).
return value
a decimal value.
note:
parameters must always come in pair of name and expression.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SELECTCOLUMNS
Adds the calculated column to the given table or table expression.
syntax->SELECTCOLUMNS(<TABLE>,<NAME>,<EXPRESSION>).
return value
a table with same number of rows same as original table. the returned table has only one column.
note:
SELECTCOLUMNS is similar to ADDCOLUMNS, and has the same behavior except that instead of starting with the table specified, SELECTCOLUMNS start with an empty table before adding columns.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SUM
It returns the sum of the column values.
syntax->SUM(<COLUMN>).
return value
a decimal number.
note:
if any non numeric values are present , blanks are returned.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------
SUMX
it returns the sum of all values in a column over an expression.
syntax->SUMX(<TABLE>,<EXPRESSION>).
return value
a decimal value
note:
Blanks, logical values, and text are ignored.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------












