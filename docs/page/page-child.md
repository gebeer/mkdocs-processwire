Return the page’s first single child that matches the given selector.
---------------------------------------------------------------------

Same as `$page->children()` but returns a single Page object or NullPage (with id=0) rather than a PageArray. Meaning, this method will only ever return one Page.

### Example

    // Get the newest created child page
    $newestChild = $page->child("sort=-created"); 

### Usage

    // basic usage
    $page = $page->child();
    
    // usage with all arguments
    $page = $page->child($selector = '', array $options = []);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array, int

Selector to use, or blank to return the first child.

`options` (optional)

array

Optional options per Pages::find

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

### See Also

*   [Page::children()](/api/ref/page/children/)

