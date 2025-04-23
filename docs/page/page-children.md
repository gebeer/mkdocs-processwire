Return this page’s children, optionally filtered by a selector
--------------------------------------------------------------

By default, hidden, unpublished and no-access pages are excluded unless `include=x` (where "x" is desired status) is specified. If a selector isn't needed, children can also be accessed directly by property with `$page->children`.

### Examples

    // Render navigation for all child pages below this one
    foreach($page->children() as $child) {
      echo "<li><a href='$child->url'>$child->title</a></li>";
    }

    // Retrieve just the 3 newest children
    $newest = $page->children("limit=3, sort=-created");

### Usage

    // basic usage
    $items = $page->children();
    
    // usage with all arguments
    $items = $page->children(string $selector = '', array $options = []);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string

Selector to use, or omit to return all children.

`options` (optional)

array

Optional options to modify behavior, the same as those provided to Pages::find.

### Return value

[`PageArray`](/api/ref/page-array/) `array`

Returns PageArray for most cases. Returns regular PHP array if using the findIDs option.

### See Also

*   [Page::child()](/api/ref/page/child/)
*   [Page::find()](/api/ref/page/find/)
*   [Page::numChildren()](/api/ref/page/num-children/)
*   [Page::hasChildren()](/api/ref/page/has-children/)

