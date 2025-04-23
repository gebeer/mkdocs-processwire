Get SQL mode, set SQL mode, add to existing SQL mode, or remove from existing SQL mode
--------------------------------------------------------------------------------------

### Example

    // Get SQL mode
    $mode = $database->sqlMode();
    
    // Add an SQL mode
    $database->sqlMode('add', 'STRICT_TRANS_TABLES');
    
    // Remove SQL mode if version at least 5.7.0
    $database->sqlMode('remove', 'ONLY_FULL_GROUP_BY', '5.7.0');

### Usage

    // basic usage
    $string = $database->sqlMode();
    
    // usage with all arguments
    $string = $database->sqlMode(string $action = 'get', string $mode = '', string $minVersion = '', $pdo = null);

### Arguments

Name

Type(s)

Description

`action` (optional)

string

Specify "get", "set", "add" or "remove". (default="get")

`mode` (optional)

string

Mode string or CSV string with SQL mode(s), i.e. "STRICT\_TRANS\_TABLES,ONLY\_FULL\_GROUP\_BY". This argument should be omitted when using the "get" action.

`minVersion` (optional)

string

Make the given action only apply if MySQL version is at least $minVersion, i.e. "5.7.0".

`pdo` (optional)

### Return value

`string` `bool`

Returns string in "get" action, boolean false if required version not present, or true otherwise.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If given an invalid $action
    

