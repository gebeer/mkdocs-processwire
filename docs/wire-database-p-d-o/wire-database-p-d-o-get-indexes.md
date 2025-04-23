Get all indexes from given table
--------------------------------

By default it returns an array of index names. Specify true for the verbose option to get index `name`, `type` and `columns` (array) for each index.

Available since version **3.0.182**.

### Usage

    // basic usage
    $array = $database->getIndexes(string $table);
    
    // usage with all arguments
    $array = $database->getIndexes(string $table, $verbose = false);

### Arguments

Name

Type(s)

Description

`table`

string

Name of table to get indexes for or `table.index` (usually combined with verbose option).

`verbose` (optional)

bool, int, string

Include array of verbose information for each? (default=false)

*   Omit or false (bool) to just get index names.
*   True (bool) or 1 (int) to get a verbose array of information for each index, indexed by index name.
*   2 (int) to get regular PHP array of raw MySQL index information.
*   Index name (string) to get verbose array only for only that index.

### Return value

`array`

