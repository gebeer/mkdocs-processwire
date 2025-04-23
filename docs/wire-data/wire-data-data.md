Get or set a low-level data value
---------------------------------

Like get() or set() but will only get/set from the WireData's protected $data array. This is used to bypass any extra logic a class may have added to its get() or set() methods. The benefit of this method over get() is that it excludes API vars and potentially other things (defined by descending classes) that you may not want.

*   To get a value, simply omit the $value argument.
*   To set a value, specify both the $key and $value arguments.
*   If you omit a $key and $value, this method will return the entire data array.

### Example

    // Set a property
    $item->data('some_property', 'some value');
    
    // Get the value of a previously set property
    $value = $item->data('some_property'); 

### Usage

    // basic usage
    $array = $wireData->data();
    
    // usage with all arguments
    $array = $wireData->data($key = null, mixed $value = null);

### Arguments

Name

Type(s)

Description

`key` (optional)

string, array

Property you want to get or set, or associative array of properties you want to set.

`value` (optional)

mixed

Optionally specify a value if you want to set rather than get. Or Specify boolean TRUE if setting an array via $key and you want to overwrite any existing values (rather than merge).

### Return value

`array` [`WireData`](/api/ref/wire-data/) `null`

Returns one of the following:

*   `mixed` - Actual value if getting a previously set value.
*   `null` - If you are attempting to get a value that has not been set.
*   `$this` - If you are setting a value.

