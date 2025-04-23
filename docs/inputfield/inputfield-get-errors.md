Return array of strings containing errors that occurred during input processing
-------------------------------------------------------------------------------

Note that this is different from [`Wire::errors()`](/api/ref/wire/errors/) in that it retrieves errors from the session rather than just the current run.

### Usage

    // basic usage
    $array = $inputfield->getErrors();
    
    // usage with all arguments
    $array = $inputfield->getErrors(bool $clear = false);

### Arguments

Name

Type(s)

Description

`clear` (optional)

bool

Optionally clear the errors after getting them (Default=false).

### Return value

`array`

