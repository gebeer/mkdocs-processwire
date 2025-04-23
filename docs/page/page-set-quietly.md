Quietly set the value of a page property.
-----------------------------------------

Set a value to a page without tracking changes and without exceptions. Otherwise same as set().

### Usage

    $page->setQuietly(string $key, mixed $value);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property you want to set

`value`

mixed

Value of property

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### See Also

*   [Wire::trackChanges()](/api/ref/wire/track-changes/)
*   [WireData::set()](/api/ref/wire-data/set/)

