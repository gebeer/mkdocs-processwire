Sanitize string to contain only ASCII digits (0-9)
--------------------------------------------------

### Usage

    // basic usage
    $string = $sanitizer->digits(string $value);
    
    // usage with all arguments
    $string = $sanitizer->digits(string $value, int $maxLength = 1024);

### Arguments

Name

Type(s)

Description

`value`

string

Value to sanitize

`maxLength` (optional)

int

Maximum length of returned value (default=1024)

### Return value

`string`

