Return the current request method (i.e. GET, POST, etc.) or blank if not known
------------------------------------------------------------------------------

Possible return values are:

*   GET
*   POST
*   HEAD
*   PUT
*   DELETE
*   OPTIONS
*   or blank if not known

Available since version **3.0.39**.

### Usage

    // basic usage
    $string = $input->requestMethod();
    
    // usage with all arguments
    $string = $input->requestMethod(string $method = '');

### Arguments

Name

Type(s)

Description

`method` (optional)

string

Optionally enter the request method to return bool if current method matches

### Return value

`string` `bool`

