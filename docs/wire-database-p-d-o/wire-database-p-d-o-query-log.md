Log a query, start/stop query logging, or return logged queries
---------------------------------------------------------------

*   To log a query, provide the $sql argument containing the query (string).
*   To retrieve the query log, call this method with no arguments.
*   Note the core only populates the query log when [`$config->debug`](/api/ref/config/debug/) mode is active.
*   Specify boolean true for $sql argument to reset and start query logging (3.0.173+)
*   Specify boolean false for $sql argument to stop query logging (3.0.173+)

### Usage

    // basic usage
    $array = $database->queryLog();
    
    // usage with all arguments
    $array = $database->queryLog($sql = '', string $note = '');

### Arguments

Name

Type(s)

Description

`sql` (optional)

string, bool

Query (string) to log, boolean true to reset/start query logging, boolean false to stop query logging

`note` (optional)

string

Any additional debugging notes about the query

### Return value

`array` `bool`

Returns query log array, boolean true on success, boolean false if not

