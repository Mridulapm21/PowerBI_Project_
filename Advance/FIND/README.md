Returns the starting position of one text string within another text string. FIND is case-sensitive.
FIND(<find_text>, <within_text>[, [<start_num>][, <NotFoundValue>]])
find_text	:The text you want to find. Use double quotes (empty text) to match the first character in within_text.
within_text	:The text containing the text you want to find.
start_num	:(optional) The character at which to start the search; if omitted, start_num = 1. The first character in within_text is character number 1.
NotFoundValue:	(optional, but strongly recommended) The value that should be returned when the operation does not find a matching substring, typically 0, -1, or BLANK(). 
If not specified, an error is returned.

Whereas Microsoft Excel has multiple versions of the FIND function to accommodate single-byte character set (SBCS) and double-byte character set (DBCS) languages, 
DAX uses Unicode and counts each character the same way; therefore, you do not need to use a different version depending on the character type.

This function is not supported for use in DirectQuery mode when used in calculated columns or row-level security (RLS) rules.

FIND does not support wildcards. To use wildcards, use SEARCH.

