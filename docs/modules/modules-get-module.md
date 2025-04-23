Get the requested Module (with options)
---------------------------------------

This is the same as `$modules->get()` except that you can specify additional options to modify default behavior. These are the options you can specify in the `$options` array argument:

*   `noPermissionCheck` (bool): Specify true to disable module permission checks (and resulting exception). (default=false)
*   `noInstall` (bool): Specify true to prevent a non-installed module from installing from this request. (default=false)
*   `noInit` (bool): Specify true to prevent the module from being initialized or configured. (default=false). See `configOnly` as alternative.
*   `noSubstitute` (bool): Specify true to prevent inclusion of a substitute module. (default=false)
*   `noCache` (bool): Specify true to prevent module instance from being cached for later getModule() calls. (default=false)
*   `noThrow` (bool): Specify true to prevent exceptions from being thrown on permission or fatal error. (default=false)
*   `returnError` (bool): Return an error message (string) on error, rather than null. (default=false)
*   `configOnly` (bool): Populate module config data but do not call its init() method. (default=false) 3.0.169+. Alternative to `noInit`.
*   `configData` (array): Associative array of additional config data to populate to module. (default=\[\]) 3.0.169+

If the module is not installed, but is installable, it will be installed, instantiated, and initialized. If you don't want that behavior, call `$modules->isInstalled('ModuleName')` as a condition first, OR specify true for the `noInstall` option in the `$options` argument.

### Usage

    // basic usage
    $module = $modules->getModule($key);
    
    // usage with all arguments
    $module = $modules->getModule($key, array $options = []);

### Arguments

Name

Type(s)

Description

`key`

string, int

Module name or database ID.

`options` (optional)

array

Optional settings to change load behavior, see method description for details.

### Return value

[`Module`](/api/ref/module/) `_Module` `null` `string`

Returns ready-to-use module or NULL|string if not found (string if `returnError` option used).

### Exceptions

Method can throw exceptions on error:

*   **`WirePermissionException` or `\Exception`** - If module requires a particular permission the user does not have
    

### See Also

*   [Modules::get()](/api/ref/modules/get/)

