Get array of all tables in this database.
-----------------------------------------

Note that this method caches its result unless you specify boolean false for the $allowCache argument.

### Usage

    // basic usage
    $array = $database->getTables();
    
    // usage with all arguments
    $array = $database->getTables(bool $allowCache = true);

### Arguments

Name

Type(s)

Description

`allowCache` (optional)

bool

Specify false if you don't want result to be cached or pulled from cache (default=true)

### Return value

`array`

Returns array of table names

