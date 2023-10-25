Removes all spaces from text except for single spaces between words.
TRIM(<text>)
text	The text from which you want spaces removed, or a column that contains text.
Use TRIM on text that you have received from another application that may have irregular spacing.

The TRIM function was originally designed to trim the 7-bit ASCII space character (value 32) from text. 
In the Unicode character set, there is an additional space character called the nonbreaking space character that has a decimal value of 160. 
This character is commonly used in Web pages as the HTML entity, &nbsp;. By itself, the TRIM function does not remove this nonbreaking space character. 
For an example of how to trim both space characters from text, see Remove spaces and nonprinting characters from text.

EXAMPLE:
FullName = TRIM(DimCustomer[Title] & " "& DimCustomer[FirstName] & " "& DimCustomer[MiddleName] & " "& DimCustomer[LastName])
