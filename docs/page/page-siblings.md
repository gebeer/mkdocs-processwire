Return this Page’s sibling pages, optionally filtered by a selector.
--------------------------------------------------------------------

To exclude the current page in list of siblings, specify boolean false for first or second argument.

### Example

    // Get all sibling pages 
    $siblings = $page->siblings();
    
    // Get all sibling pages, and exclude current page from the returned value
    $siblings = $page->siblings(false);
    
    // Get all siblings having the "product-featured" template, sorted by name
    $featured = $page->siblings("template=product-featured, sort=name");
    
    // Same as above, while excluding current page
    $featured = $page->siblings("template=product-featured, sort=name", false);

### Usage

    // basic usage
    $items = $page->siblings();
    
    // usage with all arguments
    $items = $page->siblings($selector = '', bool $includeCurrent = true);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array, bool

Optional selector to filter siblings by, or omit for all siblings.

`includeCurrent` (optional)

bool

Specify false to exclude current page in the returned siblings (default=true). If no $selector argument is given, this argument may optionally be specified as the first argument.

### Return value

[`PageArray`](/api/ref/page-array/)

