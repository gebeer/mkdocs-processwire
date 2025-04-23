Returns whether or not given $field name, ID or object is valid for this Page
-----------------------------------------------------------------------------

Note that this only indicates validity, not whether the field is populated.

### Usage

    $bool = $page->hasField($field);

### Arguments

Name

Type(s)

Description

`field`

int, string, Field, array

Field name, object or ID to check.

*   In 3.0.126+ this may also be an array or pipe "|" separated string of field names to check.

### Return value

`bool` `string`

True if valid, false if not.

*   In 3.0.126+ returns first matching field name if given an array of field names or pipe separated string of field names.

