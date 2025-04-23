Shortcut for getting or setting “value” attribute
-------------------------------------------------

When setting a value, it returns $this (for fluent interface).

### Example

    $value = $inputfield->val(); * // Getting
    $inputfield->val('foo'); * // Setting

### Usage

    // basic usage
    $mixed = $inputfield->val();
    
    // usage with all arguments
    $mixed = $inputfield->val($value = null);

### Arguments

Name

Type(s)

Description

`value` (optional)

string, null

### Return value

`mixed`

