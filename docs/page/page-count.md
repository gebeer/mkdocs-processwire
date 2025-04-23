Returns number of children page has, affected by output formatting mode.
------------------------------------------------------------------------

*   When output formatting is on, returns only number of visible children, making the return value the same as the [`Page::hasChildren()`](/api/ref/page/has-children/) method.
    
*   When output formatting is off, returns number of all children without exclusion, making the return value the same as the [`Page::numChildren()`](/api/ref/page/num-children/) method.
    

### Example

    // Get number of visible children, like $page->hasChildren()
    $page->of(true); // enable output formatting
    $numVisible = $page->count();
    
    // Get number of all children, like $page->numChildren()
    $page->of(false); // disable output formatting
    $numTotal = $page->count();

### Usage

    $int = $page->count();

### Return value

`int`

Quantity of children

### See Also

*   [Page::hasChildren()](/api/ref/page/has-children/)
*   [Page::numChildren()](/api/ref/page/num-children/)

