Get the first selector that uses given field name
-------------------------------------------------

This is useful for quickly retrieving values of reserved properties like "include", "limit", "start", etc.

Using **$or:** By default this excludes selectors that have fields in an OR expression, like "a|b|c". So if you specified field "a" it would not be matched. If you wanted it to still match, specify true for the $or argument.

Using **$all:** By default only the first matching selector is returned. If you want it to return all matching selectors in an array, then specify true for the $all argument. This changes the return value to always be an array of Selector objects, or a blank array if no match.

### Usage

    // basic usage
    $selector = $selectors->getSelectorByField(string $fieldName);
    
    // usage with all arguments
    $selector = $selectors->getSelectorByField(string $fieldName, bool $or = false, bool $all = false);

### Arguments

Name

Type(s)

Description

`fieldName`

string

Name of field to return value for (i.e. "include", "limit", etc.)

`or` (optional)

bool

Allow fields that appear in OR expressions? (default=false)

`all` (optional)

bool

Return an array of all matching Selector objects? (default=false)

### Return value

[`Selector`](/api/ref/selector/) `array` `null`

Returns null if field not present in selectors (or blank array if $all mode)

