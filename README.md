
# POWER BI DAX FUNCTIONS

 power bi dax functions notes list with explanations.



## Documentation

**ADDCOLUMNS** 

It adds the calculated columns to the given table or table expression.

**syntax** ->ADDCOLUMNS(<TABLE>,<>NAME>,<EXPRESSION>,[<NAME>,<EXPRESSION>]...)
- table->it returns a table.

- name->the name specifies the column.

- expression->Dax expression that needs to perform on each row.

return value

- a table it's original columns with added columns.

**AVERAGE**
It returns the arithmetic mean of the column.

**syntax** -> AVERAGE(<COLUMN>)

column -> the column which you want the average.

return value

it returns a decimal value.

note:

1.if there are any blank or logical values it will ignore them.

2.if any cell contains 0. it will take for the calculation.

3.suppose, in table if there are no values present then function will return 
blank. and if there are values and it does not meet the criteria the it returns the 0.

**AVERAGEA**

It returns the average of the values in a column. handles the text and non-numeric values.

**syntax** -> AVERAGEA(<COLUMN>)

return value

it returns a decimal number.

note:

1.value that evaluates to TRUE is 1.

2.value that evaluates to FALSE is 0.

3.values that contains nonnumeric text also 0.

4.empty text counts as 0.

**AVERAGEX**

It returns the average of a set of expressions evaluated over a table.

**syntax**-> AVERAGEX(<TABLE>,<EXPRESSION>)

Return value

it returns a decimal number 

note:

it is also same as the average function it does not accept the null values and non numeric values.

**COUNT**

It counts the number of cells in a column which contains numeric values or numbers.

syntax-> COUNT(<COLUMN>).

Return value

it returns the whole number.

note:

->IT DOES NOT SUPPORT THE BOOLEAN VALUES.

1.The count function counts the rows that contain the following values
     ->numbers.
     ->dates.

**COUNTA** 
It returns the number of cells containing not only numeric values but also text,non-blank values etc.,

- it supports all data types.

**syntax**-> COUNTA(<COLUMN>)

return value

it returns a whole number.

note:

When the function does not find any rows to count, the function returns a blank. When there are rows, but none of them meet the specified criteria, then the function returns 0.

**COUNTAX**

It counts nonblank results when evaluating an expression over a table, it just works like countax function. but when counting the non-blank cells the empty cells are also counted.

**syntax** -> COUNTAX(<table>,<expression>)

return value

It returns the whole number.

note:

1. it supports the boolean values.

**COUNTX**

Counts the number of rows that contains a number or expression evaluates to a number over a table.

**syntax** ->COUNTX(<TABLE>,<EXPRESSION>)

return value

it returns a whole number.

note:

1. it does not support for the boolean values.

2. parameters that are logical or text cannot be counted.

**COUNTBLANK**

Counts the no of blank cells in a column.

**syntax**-> COUNTBLANK(<COLUMN>)

Return value

a whole number.

**COUNTROWS**

IT IS USED TO COUNT NO OF ROWS IN A TABLE OR EXPRESSION THAT GIVES A TABLE.

**syntax** -> COUNTROWS(<TABLE>)

RETURN VALUE

- it returns a whole number.

**CROSSJOIN**

it is used to create single table from combining different tables together.

**syntax** ->CROSSJOIN(<TABLE1>,<TABLE2>,<TABLE3>...)

return value 

- a table containing all columns of combining parameter tables.

**DISTINCTCOUNT**

It counts the distinct values from column.

**syntax** -> DISTINCTCOUNT(<COLUMN>)

return value

it returns the whole number.




## References

Here are some related projects

- [ADDCOLUMNS](https://www.tutorialspoint.com/dax_functions/dax_addcolumns_function.htm)
- [AVERAGE](https://www.tutorialspoint.com/dax_functions/dax_average_function.htm)
- [AVERAGEA](https://www.tutorialspoint.com/dax_functions/dax_averagea_function.htm)
- [AVERAGEX](https://www.tutorialspoint.com/dax_functions/dax_averagex_function.htm)
- [COUNT](https://www.tutorialspoint.com/dax_functions/dax_count_function.htm)
- [COUNTA](https://www.tutorialspoint.com/dax_functions/dax_counta_function.htm)
- [COUNTAX](https://www.tutorialspoint.com/dax_functions/dax_countax_function.htm)
- [COUNTBLANK](https://www.tutorialspoint.com/dax_functions/dax_countblank_function.htm)
- [COUNTROWS](https://www.tutorialspoint.com/dax_functions/dax_countrows_function.htm)
- [CROSSJOIN](https://www.tutorialspoint.com/dax_functions/dax_crossjoin_function.htm)
- [DISTINCTCOUNT](https://www.tutorialspoint.com/dax_functions/dax_distinctcount_function.htm)
- [MAX](https://www.tutorialspoint.com/dax_functions/dax_max_function.htm)
- [MAXA](https://www.tutorialspoint.com/dax_functions/dax_maxa_function.htm)
- [MAXX](https://www.tutorialspoint.com/dax_functions/dax_maxx_function.htm)
- [MIN](https://www.tutorialspoint.com/dax_functions/dax_min_function.htm)
- [MINA](https://www.tutorialspoint.com/dax_functions/dax_mina_function.htm)
- [MINX](https://www.tutorialspoint.com/dax_functions/dax_minx_function.htm)
- [PRODUCT](https://www.tutorialspoint.com/dax_functions/dax_product_function.htm)
- [PRODUCTX](https://www.tutorialspoint.com/dax_functions/dax_productx_function.htm)
- [ROW](https://www.tutorialspoint.com/dax_functions/dax_row_function.htm)
- [SELECTCOLUMNS](https://www.tutorialspoint.com/dax_functions/dax_selectcolumns_function.htm)
- [SUM](https://www.tutorialspoint.com/dax_functions/dax_sum_function.htm)
- [SUMX](https://www.tutorialspoint.com/dax_functions/dax_sumx_function.htm)

//filter functions also completed 






