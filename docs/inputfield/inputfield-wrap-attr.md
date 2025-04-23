Get or set attribute for the element wrapping this Inputfield
-------------------------------------------------------------

Use this method when you need to assign some attribute to the outer wrapper of the Inputfield.

### Usage

    // basic usage
    $inputfield = $inputfield->wrapAttr();
    
    // usage with all arguments
    $inputfield = $inputfield->wrapAttr($key = null, $value = null);

### Arguments

Name

Type(s)

Description

`key` (optional)

string, null, bool

Specify one of the following for $key:

*   Specify string containing name of attribute to set.
*   Omit (or null or true) to get all wrap attributes as associative array.

`value` (optional)

string, null, bool

Specify one of the following for $value:

*   Omit if getting an attribute.
*   Value to set for $key of setting.
*   Boolean false to remove the attribute specified for $key.

### Return value

[`Inputfield`](/api/ref/inputfield/) `string` `array` `null`

Returns one of the following:

*   If getting, returns attribute value of NULL if not present.
*   If setting, returns $this.

### See Also

*   [Inputfield::attr()](/api/ref/inputfield/attr/)
*   [Inputfield::addClass()](/api/ref/inputfield/add-class/)

