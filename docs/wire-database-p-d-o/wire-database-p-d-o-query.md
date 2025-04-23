Executes an SQL statement, returning a result set as a PDOStatement object
--------------------------------------------------------------------------

### Usage

    // basic usage
    $pDOStatement = $database->query(string $statement);
    
    // usage with all arguments
    $pDOStatement = $database->query(string $statement, string $note = '');

### Arguments

Name

Type(s)

Description

`statement`

string

`note` (optional)

string

### Return value

`PDOStatement`

