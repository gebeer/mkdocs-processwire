Prepare an SQL statement for accepting bound parameters
-------------------------------------------------------

### Usage

    // basic usage
    $pDOStatement = $database->prepare(string $statement);
    
    // usage with all arguments
    $pDOStatement = $database->prepare(string $statement, $driver_options = [], string $note = '');

### Arguments

Name

Type(s)

Description

`statement`

string

`driver_options` (optional)

array, string, bool

Optionally specify one of the following:

*   Boolean true for WireDatabasePDOStatement rather than PDOStatement (also assumed when debug mode is on) 3.0.162+
*   Driver options array
*   or you may specify the $note argument here

`note` (optional)

string

Debug notes to save with query in debug mode

### Return value

`PDOStatement` `WireDatabasePDOStatement`

