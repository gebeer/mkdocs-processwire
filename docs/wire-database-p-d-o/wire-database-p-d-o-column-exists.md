Does the given column exist in given table?
-------------------------------------------

Available since version **3.0.154**.

### Example

    // Standard usage:
    if($database->columnExists('pages', 'name')) {
      echo "The pages table has a 'name' column";
    }
    
    // You can also bundle table and column together:
    if($database->columnExists('pages.name')) {
      echo "The pages table has a 'name' column";
    }
    
    $exists = $database->columnExists('pages', 'name', true);
    if($exists) {
      // associative array with indexes: Name, Type, Null, Key, Default, Extra
      echo "The pages table has a 'name' column and here is verbose info: ";
      print_r($exists);
    }

### Usage

    // basic usage
    $bool = $database->columnExists(string $table);
    
    // usage with all arguments
    $bool = $database->columnExists(string $table, string $column = '', bool $getInfo = false);

### Arguments

Name

Type(s)

Description

`table`

string

Specify table name (or table and column name in format "table.column").

`column` (optional)

string

Specify column name (or omit or blank string if already specified in $table argument).

`getInfo` (optional)

bool

Return array of column info (with type info, etc.) rather than true when exists? (default=false) Note that the returned array is raw MySQL values from a SHOW COLUMNS command.

### Return value

`bool` `array`

### Exceptions

Method can throw exceptions on error:

*   **`WireDatabaseException`**
    

