Execute an SQL statement string
-------------------------------

If given a PDOStatement, this method behaves the same as the execute() method.

### Usage

    // basic usage
    $bool = $database->exec($statement);
    
    // usage with all arguments
    $bool = $database->exec($statement, string $note = '');

### Arguments

Name

Type(s)

Description

`statement`

string, \\PDOStatement

`note` (optional)

string

### Return value

`bool` `int`

### Exceptions

Method can throw exceptions on error:

*   **`\PDOException`**
    

