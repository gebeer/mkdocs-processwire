Return number of all children, optionally with conditions
---------------------------------------------------------

Use this over the `$page->numChildren` property when you want to specify a selector, or when you want the result to include only visible children. See the options for the $selector argument.

When you want to retrieve all children with no exclusions or conditions, use the `$page->numChildren` property instead.

### Example

    // Find how many children were modified in the last week
    $qty = $page->numChildren("modified>='-1 WEEK'");

### Usage

    // basic usage
    $int = $page->numChildren();
    
    // usage with all arguments
    $int = $page->numChildren($selector = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

bool, string, array

*   When not specified, result includes all children without conditions, same as $page->numChildren property.
*   When a string or array, a selector is assumed and quantity will be counted based on selector.
*   When boolean true, number includes only visible children (excludes unpublished, hidden, no-access, etc.)
*   When boolean false, number includes all children without conditions, including unpublished, hidden, no-access, etc.

### Return value

`int`

Number of children

### See Also

*   [Page::hasChildren()](/api/ref/page/has-children/)
*   [Page::children()](/api/ref/page/children/)
*   [Page::child()](/api/ref/page/child/)

