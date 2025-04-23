Return this object’s class name
-------------------------------

If your Module descends from Wire, or any of it's derivatives (as would usually be the case), then you don't need to implement this method as it's already present.

### Usage

    // basic usage
    $string = $module->className();
    
    // usage with all arguments
    $string = $module->className($options = null);

### Arguments

Name

Type(s)

Description

`options` (optional)

array, bool, null

Optionally an option or boolean for 'namespace' option:

*   `lowercase` (bool): Specify true to make it return hyphenated lowercase version of class name
*   `namespace` (bool): Specify false to omit namespace from returned class name. Default=true.
*   Note: when lowercase=true option is specified, the namespace=false option is required.

### Return value

`string`

### See Also

*   [Wire::className()](/api/ref/wire/class-name/)

