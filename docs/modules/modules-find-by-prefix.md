Find modules matching the given prefix (i.e. “Inputfield”)
----------------------------------------------------------

By default this method returns module class names matching the given prefix. To instead retrieve instantiated (ready-to-use) modules, specify boolean true for the second argument. Regardless of `$load` argument all returned arrays are indexed by module name.

### Example

    // Retrieve array of all Textformatter module names
    $items = $modules->findByPrefix('Textformatter');
    
    // Retrieve array of all Textformatter modules (ready to use)
    $items = $modules->findByPrefix('Textformatter', true); 

### Usage

    // basic usage
    $array = $modules->findByPrefix(string $prefix);
    
    // usage with all arguments
    $array = $modules->findByPrefix(string $prefix, $load = false);

### Arguments

Name

Type(s)

Description

`prefix`

string

Specify prefix, i.e. "Process", "Fieldtype", "Inputfield", etc.

`load` (optional)

bool, int

Specify one of the following (all indexed by module name):

*   Boolean true to return array of instantiated modules.
*   Boolean false to return array of module names (default).
*   Integer 1 to return array of module info for each matching module.
*   Integer 2 to return array of verbose module info for each matching module.
*   Integer 3 to return array of Module or ModulePlaceholder objects (whatever current state is). Added 3.0.146.

### Return value

`array`

Returns array of module class names, module info arrays, or Module objects. In all cases, array indexes are class names.

