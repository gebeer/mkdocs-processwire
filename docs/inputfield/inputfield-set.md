Set a property or attribute to the Inputfield
---------------------------------------------

*   Use this for setting properties like parent, collapsed, required, columnWidth, etc.
*   You can also set properties directly via `$inputfield->property = $value`.
*   If setting an attribute (like name, id, etc.) this will work, but it is preferable to use the [`Inputfield::attr()`](/api/ref/inputfield/attr/) method.
*   If setting any kind of "class" it is preferable to use the [`Inputfield::addClass()`](/api/ref/inputfield/add-class/) method.

### Example

    // Set a value for a property
    $item->set('foo', 'bar');
    
    // Set a property value directly
    $item->foo = 'bar';
    
    // Set a property using array access
    $item['foo'] = 'bar';

### Usage

    $inputfield = $inputfield->set(string $key, mixed $value);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property to set

`value`

mixed

Value of property

### Return value

[`Inputfield`](/api/ref/inputfield/) [`WireData`](/api/ref/wire-data/)

Object instance it was called from (method supports fluent interface).

### See Also

*   [WireData::setQuietly()](/api/ref/wire-data/set-quietly/)
*   [WireData::get()](/api/ref/wire-data/get/)

