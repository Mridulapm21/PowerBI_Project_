Checks a condition, and returns one value when it's TRUE, otherwise it returns a second value.
IF(<logical_test>, <value_if_true>[, <value_if_false>])
logical_test	Any value or expression that can be evaluated to TRUE or FALSE.
value_if_true	The value that's returned if the logical test is TRUE.
value_if_false	(Optional) The value that's returned if the logical test is FALSE. If omitted, BLANK is returned.
Return value:
Either value_if_true, value_if_false, or BLANK.
The IF function can return a variant data type if value_if_true and value_if_false are of different data types, 
but the function attempts to return a single data type if both value_if_true and value_if_false are of numeric data types. 
In the latter case, the IF function will implicitly convert data types to accommodate both values.

For example, the formula IF(<condition>, TRUE(), 0) returns TRUE or 0, but the formula IF(<condition>, 1.0, 0) 
returns only decimal values even though value_if_false is of the whole number data type. To learn more about implicit data type conversion, see Data types.

To execute the branch expressions regardless of the condition expression, use IF.EAGER instead.

EXAMPLE:
HasBothHouseAndCar = 
if(and(DimCustomer[HouseOwnerFlag]>=1, DimCustomer[NumberCarsOwned]>=1), "Yes" ,if(DimCustomer[NumberCarsOwned]>=1, "Car only", if(DimCustomer[HouseOwnerFlag]>=1,"Houseowner","Neither")))
Checks whether both arguments are TRUE, and returns TRUE if both arguments are TRUE. Otherwise returns false.

NoMiddleName = 
if(ISBLANK(DimCustomer[MiddleName]), "No Middle Name",BLANK())
ISBLANK:Checks whether a value is blank, and returns TRUE or FALSE.

AddressStart = 
if(ISERROR(LEFT(DimCustomer[AddressLine1], find(" ",DimCustomer[AddressLine1] &" ")-1)),BLANK(),LEFT(DimCustomer[AddressLine1], find(" ",DimCustomer[AddressLine1] &" ")-1))
ISDERROR:Checks whether a value is an error, and returns TRUE or FALSE.
