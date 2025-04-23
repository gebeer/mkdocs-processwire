Delete a Field from the database
--------------------------------

This method will throw a WireException if you attempt to delete a field that is currently in use (i.e. assigned to one or more fieldgroups).

### Usage

    $bool = $fields->delete($item);

### Arguments

Name

Type(s)

Description

`item`

Field, Saveable

Field to delete

### Return value

`bool`

True on success, false on failure

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

