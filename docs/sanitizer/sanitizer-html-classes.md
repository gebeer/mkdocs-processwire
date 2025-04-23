Sanitize string to ASCII-only space-separated HTML class attribute values with no duplicates
--------------------------------------------------------------------------------------------

See additional notes in `Sanitizer::htmlClass()` method.

Available since version **3.0.212**.

### Usage

    // basic usage
    $string = $sanitizer->htmlClasses($value);
    
    // usage with all arguments
    $string = $sanitizer->htmlClasses($value, bool $getArray = false);

### Arguments

Name

Type(s)

Description

`value`

string, array

`getArray` (optional)

bool

Get array rather than string? (default=false)

### Return value

`string` `array`

