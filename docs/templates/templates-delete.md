Delete a Template
-----------------

### Usage

    $bool = $templates->delete($item);

### Arguments

Name

Type(s)

Description

`item`

Template, Saveable

Template to delete

### Return value

`bool`

True on success, false on failure

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - Thrown when you attempt to delete a template in use, or a system template.
    

