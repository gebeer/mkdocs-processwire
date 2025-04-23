Gets a setting (or API variable) from the Inputfield, while ignoring attributes.
--------------------------------------------------------------------------------

This is good to use in cases where there are potential name conflicts, like when there is a field literally named "collapsed" or "required".

### Usage

    $mixed = $inputfield->getSetting(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Name of setting or API variable to retrieve.

### Return value

`mixed`

Value of setting or API variable, or NULL if not found.

