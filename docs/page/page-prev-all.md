Return all sibling pages before this one, optionally matching a selector
------------------------------------------------------------------------

### Usage

    // basic usage
    $page = $page->prevAll();
    
    // usage with all arguments
    $page = $page->prevAll($selector = '', $getQty = false);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array, bool

Optional selector. When specified, will filter the found siblings.

`getQty` (optional)

bool, PageArray

Return a count instead of PageArray? (boolean)

*   If no $selector argument is needed, this may be specified as the first argument.
*   Legacy support: You may specify a PageArray of siblings to use instead of the default (deprecated, avoid it).

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/) `int`

Returns all matching pages before this one, or integer if $getQty requested.

