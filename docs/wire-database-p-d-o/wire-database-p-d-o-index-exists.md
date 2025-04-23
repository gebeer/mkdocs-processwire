Does table have an index with given name?
-----------------------------------------

Available since version **3.0.182**.

### Example

    // simple index check
    if($database->indexExists('my_table', 'my_index')) {
      // index named my_index exists for my_table
    }
    
    // index check and get array of info if it exists
    $info = $database->indexExists('my_table', 'my_index', true);
    if($info) {
      // info is raw array of information about index from MySQL
    } else {
      // index does not exist
    }

### Usage

    // basic usage
    $bool = $database->indexExists(string $table, string $indexName);
    
    // usage with all arguments
    $bool = $database->indexExists(string $table, string $indexName, bool $getInfo = false);

### Arguments

Name

Type(s)

Description

`table`

string

`indexName`

string

`getInfo` (optional)

bool

Return arrays of index information rather than boolean true? (default=false) Note that the verbose arrays are the raw MySQL return values from a SHOW INDEX command.

### Return value

`bool` `array`

Returns one of the following:

*   `false`: if index does not exist (regardless of $getInfo argument).
*   `true`: if index exists and $getInfo argument is omitted or false.
*   `array`: array of arrays with verbose information if index exists and $getInfo argument is true.

