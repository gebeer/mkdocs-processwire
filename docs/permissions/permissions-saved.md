Hook called when a permission is saved
--------------------------------------

Available since version **3.0.128**.

### Usage

    // basic usage
    $permissions->saved(Page $page);
    
    // usage with all arguments
    $permissions->saved(Page $page, array $changes = [], array $values = []);

### Arguments

Name

Type(s)

Description

`page`

Page

Page that was saved

`changes` (optional)

array

Array of changed field names

`values` (optional)

array

Array of changed field values indexed by name (when enabled)

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

