Rename table columns without changing type
------------------------------------------

Available since version **3.0.185**.

### Usage

    $int = $database->renameColumns(string $table, array $columns);

### Arguments

Name

Type(s)

Description

`table`

string

`columns`

array

Associative array with one or more of `[ 'old_name' => 'new_name' ]`

### Return value

`int`

Number of columns renamed

### Exceptions

Method can throw exceptions on error:

*   **`\PDOException`**
    

