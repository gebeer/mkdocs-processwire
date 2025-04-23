Get the field(s) of this Selector
---------------------------------

Note that if calling this as a property (rather than a method) it can return either a string or an array.

Available since version **3.0.42**. _Prior versions only supported the 'field' property._

### Usage

    // basic usage
    $string = $selector->field();
    
    // usage with all arguments
    $string = $selector->field($forceString = true);

### Arguments

Name

Type(s)

Description

`forceString` (optional)

bool, int

Specify one of the following:

*   `true` (bool): to only return a string, where multiple-fields will be split by pipe "|". (default)
*   `false` (bool): to return string if 1 field, or array of multiple fields (same behavior as field property).
*   `1` (int): to return only the first value (string).

### Return value

`string` `array` `null`

### See Also

*   [Selector::fields()](/api/ref/selector/fields/)

