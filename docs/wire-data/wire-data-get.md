Retrieve the value for a previously set property, or retrieve an API variable
-----------------------------------------------------------------------------

*   If the given $key is an object, it will cast it to a string.
*   If the given $key is a string with "|" pipe characters in it, it will try all till it finds a non-empty value.
*   If given an API variable name, it will return that API variable unless the class has direct access API variables disabled.

### Example

    // Retrieve the value of a property
    $value = $item->get("some_property");
    
    // Retrieve the value of the first non-empty property:
    $value = $item->get("property1|property2|property2");
    
    // Retrieve a value using array access
    $value = $item["some_property"];

### Usage

    $mixed = $wireData->get($key);

### Arguments

Name

Type(s)

Description

`key`

string, object

Name of property you want to retrieve.

### Return value

`mixed` `null`

Returns value of requested property, or null if the property was not found.

### See Also

*   [WireData::set()](/api/ref/wire-data/set/)

