Evaluates an expression against a list of values and returns one of multiple possible result expressions. This function can be used to avoid having multiple nested IF statements.
synatx:
SWITCH(<expression>, <value>, <result>[, <value>, <result>]…[, <else>])
expression:	Any DAX expression that returns a single scalar value where the expression is to be evaluated multiple times (for each row/context).
value	:A constant value to be matched with the results of expression.
result:	Any scalar expression to be evaluated if the results of expression match the corresponding value.
else:	Any scalar expression to be evaluated if the result of expression doesn't match any of the value arguments.

Return value
If there’s a match with a value, a scalar value from the corresponding result is returned. 
If there isn’t a match with a value, a value from else is returned. If none of the values match and else isn’t specified, BLANK is returned.

The expression to be evaluated can be a constant value or an expression. A common use of this function is to set the first parameter to TRUE. 
All result expressions and the else expression must be of the same data type.
The order of conditions matters. As soon as one value matches, the corresponding result is returned, and other subsequent values aren’t evaluated. 
Make sure the most restrictive values to be evaluated are specified before less restrictive values. 
