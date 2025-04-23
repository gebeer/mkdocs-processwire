Return the actual current PDO connection instance
-------------------------------------------------

If connection is lost, this will restore it automatically.

### Usage

    // basic usage
    $pDO = $database->pdo();
    
    // usage with all arguments
    $pDO = $database->pdo($type = null);

### Arguments

Name

Type(s)

Description

`type` (optional)

### Return value

`PDO`

