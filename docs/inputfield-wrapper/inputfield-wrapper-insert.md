Insert new or existing Inputfield before or after another
---------------------------------------------------------

Available since version **3.0.196**.

### Usage

    // basic usage
    $inputfieldWrapper->insert($item, $existingItem);
    
    // usage with all arguments
    $inputfieldWrapper->insert($item, $existingItem, bool $before = false);

### Arguments

Name

Type(s)

Description

`item`

Inputfield, array, string

New or existing item Inputfield, name, or new item array to insert.

`existingItem`

Inputfield, string

Existing item or item name you want to insert before.

`before` (optional)

bool

True to insert before, false to insert after (default=false).

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

