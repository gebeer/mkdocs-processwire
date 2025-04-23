Get MySQL/MariaDB version
-------------------------

Example return values:

*   5.7.23
*   10.1.34-MariaDB

Available since version **3.0.166**.

### Usage

    // basic usage
    $string = $database->getVersion();
    
    // usage with all arguments
    $string = $database->getVersion(bool $getNumberOnly = false);

### Arguments

Name

Type(s)

Description

`getNumberOnly` (optional)

bool

Get only version number, exclude any vendor specific suffixes? (default=false) 3.0.185+

### Return value

`string`

