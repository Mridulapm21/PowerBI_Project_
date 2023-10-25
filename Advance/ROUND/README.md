Rounds a number to the specified number of digits.
To always round up (away from zero), use the ROUNDUP function.
To always round down (toward zero), use the ROUNDDOWN function.
To round a number to a specific multiple (for example, to round to the nearest multiple of 0.5), use the MROUND function.
Use the functions TRUNC and INT to obtain the integer portion of the number.
If num_digits is greater than 0 (zero), then number is rounded to the specified number of decimal places.
If num_digits is 0, the number is rounded to the nearest integer.
If num_digits is less than 0, the number is rounded to the left of the decimal point.
I created a new table called IncomePerPerson and I used DAX formula 
=ROUND(DimCustomer[YearlyIncome]\DimCustomer[NumberPeople]),-3 
-3 will round to the nearest multiple of 1000


MROUND
Return value
A decimal number.
MROUND rounds up, away from zero, if the remainder of dividing number by the specified multiple is greater than or equal to half the value of multiple.
Example: Decimal Places
The following expression rounds 1.3 to the nearest multiple of .2. The expected result is 1.4.
DAX
= MROUND(1.3,0.2)  

Negative Numbers
The following expression rounds -10 to the nearest multiple of -3. The expected result is -9.
DAX
= MROUND(-10,-3)  
