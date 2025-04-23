Are transactions available with current DB engine (or table)?
-------------------------------------------------------------

### Usage

    // basic usage
    $bool = $database->supportsTransaction();
    
    // usage with all arguments
    $bool = $database->supportsTransaction(string $table = '');

### Arguments

Name

Type(s)

Description

`table` (optional)

string

Optionally specify a table to specifically check to that table

### Return value

`bool`

