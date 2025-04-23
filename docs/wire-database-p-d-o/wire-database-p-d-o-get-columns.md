Get all columns from given table
--------------------------------

By default returns array of column names. If verbose option is true then it returns an array of arrays, each having 'name', 'type', 'null', 'default', and 'extra' keys, indicating the column name, column type, whether it can be null, what it’s default value is, and any extra information, such as whether it is auto\_increment. The verbose option also makes the return value indexed by column name (associative array).

Available since version **3.0.180**.

### Usage

    // basic usage
    $array = $database->getColumns(string $table);
    
    // usage with all arguments
    $array = $database->getColumns(string $table, $verbose = false);

### Arguments

Name

Type(s)

Description

`table`

string

Table name or or `table.column` to get for specific column (when combined with verbose=true)

`verbose` (optional)

bool, int, string

Include array of verbose information for each? (default=false)

*   Omit or false (bool) to just get column names.
*   True (bool) or 1 (int) to get a verbose array of information for each column, indexed by column name.
*   2 (int) to get raw MySQL column information, indexed by column name (added 3.0.182).
*   3 (int) to get column types as used in a CREATE TABLE statement (added 3.0.185).
*   Column name (string) to get verbose array only for only that column (added 3.0.182).

### Return value

`array`

