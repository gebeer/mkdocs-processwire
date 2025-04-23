Get current date/time ISO-8601 string or UNIX timestamp according to database
-----------------------------------------------------------------------------

Available since version **3.0.183**.

### Usage

    // basic usage
    $string = $database->getTime();
    
    // usage with all arguments
    $string = $database->getTime(bool $getTimestamp = false);

### Arguments

Name

Type(s)

Description

`getTimestamp` (optional)

bool

Get unix timestamp rather than ISO-8601 string? (default=false)

### Return value

`string` `int`

