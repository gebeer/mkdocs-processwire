Find descendant pages matching given selector
---------------------------------------------

This is the same as `Pages::find()` except that the results are limited to descendents of this Page.

### Example

    // Find all unpublished pages underneath the current page
    $items = $page->find("status=unpublished"); 

### Usage

    // basic usage
    $items = $page->find();
    
    // usage with all arguments
    $items = $page->find($selector = '', array $options = []);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array

Selector string or array

`options` (optional)

array

Same as the $options array passed to $pages->find().

### Return value

[`PageArray`](/api/ref/page-array/)

### See Also

*   [Pages::find()](/api/ref/pages/find/)

