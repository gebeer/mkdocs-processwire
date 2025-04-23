Return the next sibling page
----------------------------

By default, hidden, unpublished and non-viewable pages are excluded. If you want them included, be sure to specify `include=` with hidden, unpublished or all, in your selector.

### Example

    // Get the next sibling
    $sibling = $page->next();
    
    // Get the next newest sibling
    $sibling = $page->next("created>$page->created");
    
    // Get the next sibling, even if it isn't viewable
    $sibling = $page->next("include=all");

### Usage

    // basic usage
    $page = $page->next();
    
    // usage with all arguments
    $page = $page->next($selector = '', PageArray $siblings = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array

Optional selector. When specified, will find nearest next sibling that matches.

`siblings` (optional)

PageArray

Optional siblings to use instead of the default. Avoid using this argument as it forces this method to use the older/slower functions.

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

Returns the next sibling page, or a NullPage if none found.

