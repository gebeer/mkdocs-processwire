Find one descendant page matching given selector
------------------------------------------------

This is the same as `Pages::findOne()` except that the match is always a descendant of page it is called on.

Available since version **3.0.116**.

### Example

    // Find the most recently modified descendant page
    $item = $page->findOne("sort=-modified");

### Usage

    // basic usage
    $page = $page->findOne();
    
    // usage with all arguments
    $page = $page->findOne($selector = '', array $options = []);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array

Selector string or array

`options` (optional)

array

Optional options to modify default bheavior, see options for `Pages::find()`.

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

Returns Page when found, or NullPage when nothing found.

### See Also

*   [Pages::findOne()](/api/ref/pages/find-one/)
*   [Page::child()](/api/ref/page/child/)

