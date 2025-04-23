Return the previous sibling page
--------------------------------

### Example

    // Get the previous sibling
    $sibling = $page->prev();
    
    // Get the previous sibling having field "featured" with value of "1"
    $sibling = $page->prev("featured=1"); 

### Usage

    // basic usage
    $page = $page->prev();
    
    // usage with all arguments
    $page = $page->prev($selector = '', $siblings = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array

Optional selector. When specified, will find nearest previous sibling that matches.

`siblings` (optional)

PageArray, null

Optional siblings to use instead of the default.

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

Returns the previous sibling page, or a NullPage if none found.

