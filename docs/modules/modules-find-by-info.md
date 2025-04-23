Find modules by matching a property or properties in their module info
----------------------------------------------------------------------

### Usage

    // basic usage
    $array = $modules->findByInfo($selector);
    
    // usage with all arguments
    $array = $modules->findByInfo($selector, $load = false);

### Arguments

Name

Type(s)

Description

`selector`

string, array

Specify one of the following:

*   Selector string to match module info.
*   Array of \[ 'property' => 'value' \] to match in module info (this is not a selector array).
*   Name of property that will match module if not empty in module info.

`load` (optional)

bool, int

Specify one of the following:

*   Boolean true to return array of instantiated modules.
*   Boolean false to return array of module names (default).
*   Integer 1 to return array of module info for each matching module.
*   Integer 2 to return array of verbose module info for each matching module.

### Return value

`array`

Array of modules, module names or module info arrays, indexed by module name.

