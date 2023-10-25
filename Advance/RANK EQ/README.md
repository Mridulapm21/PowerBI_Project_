The RANK.EQ function in Power BI returns the rank of a number in a column of numbers.
RANK.EQ(<value>, <columnName>[, <order>])  Syntax
value: Any DAX expression that returns a single scalar value whose rank is to be found. 
The expression is to be evaluated exactly once, before the function is evaluated, and it's value passed to the argument list.
columnName:	The name of an existing column against which ranks will be determined. 
It cannot be an expression or a column created using these functions: ADDCOLUMNS, ROW or SUMMARIZE.
order:	(Optional) A value that specifies how to rank number, low to high or high to low:

0 (zero)	FALSE	Ranks in descending order of columnName. If value is equal to the highest number in columnName then RANK.EQ is 1.
1	TRUE	Ranks in ascending order of columnName. If value is equal to the lowest number in columnName then RANK.EQ is 1.

A number indicating the rank of value among the numbers in columnName.

columnName cannot refer to any column created using these functions: ADDCOLUMNS, ROW or SUMMARIZE.I

If value is not in columnName or value is a blank, then RANK.EQ returns a blank value.

Duplicate values of value receive the same rank value; the next rank value assigned will be the rank value plus the number of duplicate values. 
For example if five (5) values are tied with a rank of 11 then the next value will receive a rank of 16 (11 + 5).

This function is not supported for use in DirectQuery mode when used in calculated columns or row-level security (RLS) rules.
Example :
RankEQ = RANK.EQ(DimCustomer[IncomePerPerson],DimCustomer[IncomePerPerson],DESC)


