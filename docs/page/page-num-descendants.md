Return number of descendants (children, grandchildren, great-grandchildren, …), optionally with conditions
----------------------------------------------------------------------------------------------------------

Use this over the `$page->numDescendants` property when you want to specify a selector or apply some other filter to the result (see options for `$selector` argument). If you want to include only visible descendants specify a selector (string or array) or boolean true for the `$selector` argument, if you don’t need a selector.

If you want to find descendant pages (rather than count), use the [`Page::find()`](/api/ref/page/find/) method.

### Example

    // Find how many descendants were modified in the last week
    $qty = $page->numDescendants("modified>='-1 WEEK'");

### Usage

    // basic usage
    $int = $page->numDescendants();
    
    // usage with all arguments
    $int = $page->numDescendants($selector = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

### Return value

`int`

Number of descendants

### See Also

*   [Page::numChildren()](/api/ref/page/num-children/)
*   [Page::find()](/api/ref/page/find/)

