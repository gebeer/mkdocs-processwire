Get URL to edit field in the admin
----------------------------------

Available since version **3.0.151**.

### Usage

    // basic usage
    $string = $field->editUrl();
    
    // usage with all arguments
    $string = $field->editUrl($options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

array, bool, string

Specify array of options, string for find option, or bool for http option.

*   `find` (string): Name of field to find in editor form
*   `http` (bool): True to force inclusion of scheme and hostname

### Return value

`string`

