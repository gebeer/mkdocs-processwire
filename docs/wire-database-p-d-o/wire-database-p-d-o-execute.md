Title: $database->execute() method - ProcessWire API

URL Source: https://processwire.com/api/ref/wire-database-p-d-o/execute/

Markdown Content:
Execute a PDO statement, with retry and error handling
------------------------------------------------------

Given a PDOStatement ($query) this method will execute the statement and return true or false as to whether it was successful.

Unlike other PDO methods, this one (native to ProcessWire) will retry queries if they failed due to a lost connection. By default it will retry up to 3 times, but you can adjust this number as needed in the arguments.

### Example

```
// prepare the query
$query = $database->prepare("SELECT id, name FROM pages LIMIT 10");
// you can do the following, rather than native PDO $query->execute();
$database->execute($query);
```

### Usage

```
// basic usage
$bool = $database->execute(\PDOStatement $query);

// usage with all arguments
$bool = $database->execute(\PDOStatement $query, bool $throw = true, int $maxTries = 3);
```

### Arguments

| Name | Type(s) | Description |
| --- | --- | --- |
| `query` | \\PDOStatement |  |
| `throw` (optional) | bool | Whether or not to throw exception on query error (default=true)
 |
| `maxTries` (optional) | int | Max number of times it will attempt to retry query on lost connection error

 |

### Return value

`bool`

True on success, false on failure. Note if you want this, specify $throw=false in your arguments.

### Exceptions

Method can throw exceptions on error:

*   **`\PDOException`**
    

* * *

[$database methods and properties](https://processwire.com/api/ref/wire-database-p-d-o/)

API reference based on ProcessWire core version 3.0.244
