Get the path + filename (or optionally URL) for this module
-----------------------------------------------------------

### Usage

    // basic usage
    $bool = $modules->getModuleFile($class);
    
    // usage with all arguments
    $bool = $modules->getModuleFile($class, $options = []);

### Arguments

Name

Type(s)

Description

`class`

string, Module

Module class name or object instance

`options` (optional)

array, bool

Options to modify default behavior:

*   `getURL` (bool): Specify true if you want to get the URL rather than file path (default=false).
*   `fast` (bool): Specify true to omit file\_exists() checks (default=false).
*   `guess` (bool): Manufacture/guess a module location if one cannot be found (default=false) 3.0.170+
*   Note: If you specify a boolean for the $options argument, it is assumed to be the $getURL property.

### Return value

`bool` `string`

Returns string of module file, or false on failure.

