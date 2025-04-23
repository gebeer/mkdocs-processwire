Set the value of a page property
--------------------------------

You can set properties to a page using either `$page->set('property', $value);` or `$page->property = $value;`.

### Example

    // Set the page title using set() method
    $page->set('title', 'About Us');
    
    // Set the page title directly (equivalent to the above)
    $page->title = 'About Us';

### Usage

    $page = $page->set(string $key, mixed $value);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property to set

`value`

mixed

Value to set

### Return value

[`Page`](/api/ref/page/) [`WireData`](/api/ref/wire-data/)

Reference to this Page

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

### See Also

*   [WireData::setQuietly()](/api/ref/wire-data/set-quietly/)
*   [WireData::get()](/api/ref/wire-data/get/)

