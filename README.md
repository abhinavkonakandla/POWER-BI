
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





**FILTER FUNCTIONS**

**ALL**

It returns all the rows in a table or all the values in a column. basically it removes filters for complete table or given column. used when we want to apply filters on complete table we use this function.

**syntax** -> ALL(<TABLE> | <COLUMN>).

The argument of the above syntax should not be an expression.

return type

returns a table or column with filters removed.

**ALLEXCEPT**

It removes all filters except for mentioned columns.

**syntax** ->ALLEXCEPT(<TABLE>,<COLUMN>).

return value

a table with all filters removed except for the filters on the specified columns.

Note:

1. we can use ALLEXCEPT function when we want to remove all filters on all rows except one or two then ALLEXCEPT can be used.

**ALLNONBLANKROW**

It returns a table or column that all filters ae removed along with blank rows.

**syntax**-> ALLNONBLANKROW(<TABLE> | <COLUMN>).

return value

it returns a table by removing any filters on it and empty rows are also removed.

Note:

1. The main difference between ALL and ALLNONBLANKROW is 

        ALL -->  It removes all filters on a table or column that you specify.

        ALLNONBLANKROW --> it removes all filters along with blank-rows.

**CALCULATE**

It is used to evaluate an expression by applying filters.

**syntax** -> CALCULATE(<EXPRESSION>,<FILTER>).

return value

result of that expression.


**CALCULATETABLE**

It evaluates a table expression by applying some filters.

**syntax**-> CALCULATETABLE(<EXPRESSION>,<FILTER>).

return value

a table of values.

**DISTINCT**

It gives a column of unique values.

**syntax**-> DISTINCT(<COLUMN>).

return value

a single column table with unique values..

**EARLIER**

returns the current value of the column in an outer evaluation passes.

**syntax** -> EARLIER(<COLUMN>,<NUMBER>).

return value

It returns the current row value from the given column at number of outer evaluation passes.

Note:
1. EARLIER is used for nested calculations.

2. here, it stores a value in a variable to make calculation with other values.

**FILTER**

It returns a table based on the filters.

**syntax**-> FILTER(<TABLE>,<EXPRESSION>).

return value

a table containing filtered rows.

Note:

1. FILTER function is used to reduce number of rows working with and use only specific data in 
calculations.

2. DAX FILTER is not independent function.(table is giving as an argument).

**FILTERS**

It returns the values directly applied to the column
(In simple words it shows how many filters are applied to a column)

**syntax**-> FILTERS(<COLUMNNAME>).

return value

the values that are directly applied as filters to column name.

**HASONEFILTER**

returns true if there are one and only direct filters on a column otherwise it returns false.

**syntax**-> HASONEFILTER(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**HASONEVALUE**

Returns TRUE when the context for columnName has been filtered down to one distinct value only. Otherwise, returns FALSE.

**syntax**->HASONEVALUE(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**ISCROSSFILTERED**

returns true when column name or another column in same or related table being filtered.

**syntax**->ISCROSSFILTERED(<COLUMNNAME>).

return value

TRUE (or) FALSE.

Note:
1. A column column name is said to be cross-filtered when a filter applied to another column in the same table or related table affects the column name by filtering it.

**ISFILTERED**
returns true when column name is directly filtered. 

If there is no filter on the column or if the filtering happens because a different column in the same table or in a related table is being filtered, then the DAX ISFILTERED function returns FALSE.

**syntax**->ISFILTERED(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**KEEPFILTERS**
it allows to maintain existing filters on a column or table while additional filters in your calculations.

**syntax**-> KEEPFILTERS(<EXPRESSION>).

return value

NO RETURN VALUE

Note:

1. KEEPFILTERS IS MOSTLY USED IN CALCULATE AND CALCULATETABLE functions to modify the filters.






//FILTERS FUNCTIONS COMPLETED



**FILTER FUNCTIONS**

**ALL**

It returns all the rows in a table or all the values in a column. basically it removes filters for complete table or given column. used when we want to apply filters on complete table we use this function.

**syntax** -> ALL(<TABLE> | <COLUMN>).

The argument of the above syntax should not be an expression.

return type

returns a table or column with filters removed.

**ALLEXCEPT**

It removes all filters except for mentioned columns.

**syntax** ->ALLEXCEPT(<TABLE>,<COLUMN>).

return value

a table with all filters removed except for the filters on the specified columns.

Note:

1. we can use ALLEXCEPT function when we want to remove all filters on all rows except one or two then ALLEXCEPT can be used.

**ALLNONBLANKROW**

It returns a table or column that all filters ae removed along with blank rows.

**syntax**-> ALLNONBLANKROW(<TABLE> | <COLUMN>).

return value

it returns a table by removing any filters on it and empty rows are also removed.

Note:

1. The main difference between ALL and ALLNONBLANKROW is 

        ALL -->  It removes all filters on a table or column that you specify.

        ALLNONBLANKROW --> it removes all filters along with blank-rows.

**CALCULATE**

It is used to evaluate an expression by applying filters.

**syntax** -> CALCULATE(<EXPRESSION>,<FILTER>).

return value

result of that expression.


**CALCULATETABLE**

It evaluates a table expression by applying some filters.

**syntax**-> CALCULATETABLE(<EXPRESSION>,<FILTER>).

return value

a table of values.

**DISTINCT**

It gives a column of unique values.

**syntax**-> DISTINCT(<COLUMN>).

return value

a single column table with unique values..

**EARLIER**

returns the current value of the column in an outer evaluation passes.

**syntax** -> EARLIER(<COLUMN>,<NUMBER>).

return value

It returns the current row value from the given column at number of outer evaluation passes.

Note:
1. EARLIER is used for nested calculations.

2. here, it stores a value in a variable to make calculation with other values.

**FILTER**

It returns a table based on the filters.

**syntax**-> FILTER(<TABLE>,<EXPRESSION>).

return value

a table containing filtered rows.

Note:

1. FILTER function is used to reduce number of rows working with and use only specific data in 
calculations.

2. DAX FILTER is not independent function.(table is giving as an argument).

**FILTERS**

It returns the values directly applied to the column
(In simple words it shows how many filters are applied to a column)

**syntax**-> FILTERS(<COLUMNNAME>).

return value

the values that are directly applied as filters to column name.

**HASONEFILTER**

returns true if there are one and only direct filters on a column otherwise it returns false.

**syntax**-> HASONEFILTER(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**HASONEVALUE**

Returns TRUE when the context for columnName has been filtered down to one distinct value only. Otherwise, returns FALSE.

**syntax**->HASONEVALUE(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**ISCROSSFILTERED**

returns true when column name or another column in same or related table being filtered.

**syntax**->ISCROSSFILTERED(<COLUMNNAME>).

return value

TRUE (or) FALSE.

Note:
1. A column column name is said to be cross-filtered when a filter applied to another column in the same table or related table affects the column name by filtering it.

**ISFILTERED**
returns true when column name is directly filtered. 

If there is no filter on the column or if the filtering happens because a different column in the same table or in a related table is being filtered, then the DAX ISFILTERED function returns FALSE.

**syntax**->ISFILTERED(<COLUMNNAME>).

return value

TRUE (or) FALSE.

**KEEPFILTERS**
it allows to maintain existing filters on a column or table while additional filters in your calculations.

**syntax**-> KEEPFILTERS(<EXPRESSION>).

return value

NO RETURN VALUE

Note:

1. KEEPFILTERS IS MOSTLY USED IN CALCULATE AND CALCULATETABLE functions to modify the filters.






//FILTERS FUNCTIONS COMPLETED

## References


- [ALL](https://www.tutorialspoint.com/dax_functions/dax_all_function.htm)
- [ALLEXCEPT](https://www.tutorialspoint.com/dax_functions/dax_allexcept_function.htm)
- [ALLNONBLANKROW](https://www.tutorialspoint.com/dax_functions/dax_allnoblankrow_function.htm)
- [CALCULATE](https://www.tutorialspoint.com/dax_functions/dax_calculate_function.htm)
- [CALCULATETABLE](https://www.tutorialspoint.com/dax_functions/dax_calculatetable_function.htm)
- [DISTINCT](https://www.tutorialspoint.com/dax_functions/dax_distinct_function.htm)
- [EARLIER](https://www.tutorialspoint.com/dax_functions/dax_earlier_function.htm)
- [FILTER](https://www.tutorialspoint.com/dax_functions/dax_filter_function.htm)
- [FILTERS](https://www.tutorialspoint.com/dax_functions/dax_filters_function.htm)
- [HASONEFILTER](https://www.tutorialspoint.com/dax_functions/dax_hasonefilter_function.htm)
- [HASONEVALUE](https://www.tutorialspoint.com/dax_functions/dax_hasonevalue_function.htm)
- [ISCROSSFILTERED](https://www.tutorialspoint.com/dax_functions/dax_iscrossfiltered_function.htm)
- [ISFILTERED](https://www.tutorialspoint.com/dax_functions/dax_isfiltered_function.htm)
- [KEEPFILTERS](https://www.tutorialspoint.com/dax_functions/dax_keepfilters_function.htm)

//filter functions also completed 








