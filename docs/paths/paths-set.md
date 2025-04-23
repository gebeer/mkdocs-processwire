Set a new path/URL location
---------------------------

### Example

    // Set a value for a property
    $item->set('foo', 'bar');
    
    // Set a property value directly
    $item->foo = 'bar';
    
    // Set a property using array access
    $item['foo'] = 'bar';

### Usage

    $paths = $urls->set(string $key, mixed $value);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property you want to set

`value`

mixed

If the first character of the provided path is a slash, then that specific path will be used without modification. If the first character is anything other than a slash, then the 'root' variable will be prepended to the path.

### Return value

[`Paths`](/api/ref/paths/) [`WireData`](/api/ref/wire-data/)

Object instance it was called from (method supports fluent interface).

### See Also

*   [WireData::setQuietly()](/api/ref/wire-data/set-quietly/)
*   [WireData::get()](/api/ref/wire-data/get/)

