Sanitize to a bit, returning only integer 0 or 1
------------------------------------------------

This works the same as the bool sanitizer except that it returns 0 or 1 rather than false or true.

Available since version **3.0.125**.

### Usage

    $int = $sanitizer->bit($value);

### Arguments

Name

Type(s)

Description

`value`

string, int, array

### Return value

`int`

### See Also

*   [Sanitizer::bool()](/api/ref/sanitizer/bool/)

