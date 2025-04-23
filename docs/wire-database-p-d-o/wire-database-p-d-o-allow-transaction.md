Allow a new transaction to begin right now? (i.e. supported and not already in one)
-----------------------------------------------------------------------------------

Returns combined result of supportsTransaction() === true and inTransaction() === false.

Available since version **3.0.140**.

### Usage

    // basic usage
    $bool = $database->allowTransaction();
    
    // usage with all arguments
    $bool = $database->allowTransaction(string $table = '');

### Arguments

Name

Type(s)

Description

`table` (optional)

string

Optional table that transaction will be for

### Return value

`bool`

