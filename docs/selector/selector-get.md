Get a property
--------------

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

    $array = $selector->get(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Property name

### Return value

`array` `mixed` `null` `string`

Property value

### See Also

*   [WireData::set()](/api/ref/wire-data/set/)

