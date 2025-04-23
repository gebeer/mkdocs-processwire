Get a property or attribute from the Inputfield
-----------------------------------------------

*   This can also be accessed directly, i.e. `$value = $inputfield->property;`.
    
*   For getting attribute values, this will work, but it is preferable to use the [`Inputfield::attr()`](/api/ref/inputfield/attr/) method.
    
*   For getting non-attribute values that have potential name conflicts with attributes (or just as a reliable alternative), use the [`Inputfield::getSetting()`](/api/ref/inputfield/get-setting/) method instead, which excludes the possibility of overlap with attributes.
    

### Example

    // Retrieve the value of a property
    $value = $item->get("some_property");
    
    // Retrieve the value of the first non-empty property:
    $value = $item->get("property1|property2|property2");
    
    // Retrieve a value using array access
    $value = $item["some_property"];

### Usage

    $mixed = $inputfield->get(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property or attribute to retrieve.

### Return value

`mixed` `null`

Value of property or attribute, or NULL if not found.

### See Also

*   [WireData::set()](/api/ref/wire-data/set/)

