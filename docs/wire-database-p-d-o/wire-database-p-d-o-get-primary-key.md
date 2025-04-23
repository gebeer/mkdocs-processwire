Get column(s) or info for given table’s primary key/index
---------------------------------------------------------

By default it returns a string with the column name compromising the primary key, i.e. `col1`. If the primary key is multiple columns then it returns a CSV string, like `col1,col2,col3`.

If you specify boolean `true` for the verbose option then it returns an simplified array of information about the primary key. If you specify integer `2` then it returns an array of raw MySQL SHOW INDEX information.

Available since version **3.0.182**.

### Usage

    // basic usage
    $string = $database->getPrimaryKey(string $table);
    
    // usage with all arguments
    $string = $database->getPrimaryKey(string $table, $verbose = false);

### Arguments

Name

Type(s)

Description

`table`

string

`verbose` (optional)

bool, int

Get array of info rather than column(s) string? (default=false)

### Return value

`string` `array`

