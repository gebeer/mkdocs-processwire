Rename a table column without changing type
-------------------------------------------

Available since version **3.0.185**.

### Usage

    $bool = $database->renameColumn(string $table, string $oldName, string $newName);

### Arguments

Name

Type(s)

Description

`table`

string

`oldName`

string

`newName`

string

### Return value

`bool`

### Exceptions

Method can throw exceptions on error:

*   **`\PDOException`**
    

