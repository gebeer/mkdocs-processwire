Return array of all field names referenced in all of the Selector objects here
------------------------------------------------------------------------------

### Usage

    // basic usage
    $array = $selectors->getAllFields();
    
    // usage with all arguments
    $array = $selectors->getAllFields(bool $subfields = true);

### Arguments

Name

Type(s)

Description

`subfields` (optional)

bool

Default is to allow "field.subfield" fields, or specify false to convert them to just "field".

### Return value

`array`

Returned array has both keys and values as field names (same)

