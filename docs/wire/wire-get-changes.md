Return an array of properties that have changed while change tracking was on.
-----------------------------------------------------------------------------

### Example

    // Get an array of changed field names
    $changes = $page->getChanges();

### Usage

    // basic usage
    $array = $wire->getChanges();
    
    // usage with all arguments
    $array = $wire->getChanges(bool $getValues = false);

### Arguments

Name

Type(s)

Description

`getValues` (optional)

bool

Specify one of the following, or omit for default setting.

*   `false` (bool): return array of changed property names (default setting).
*   `true` (bool): return an associative array containing an array of previous values, indexed by property name, oldest to newest. Requires Wire::trackChangesValues mode to be enabled.
*   `2` (int): Return array where both keys and values are changed property names.

### Return value

`array`

