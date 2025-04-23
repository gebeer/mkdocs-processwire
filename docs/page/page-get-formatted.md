Get the formatted value of a field, regardless of output formatting state
-------------------------------------------------------------------------

When a page's output formatting state is on, `$page->get('property')` or `$page->property` will produce the same result as this method call.

### Example

    // Get the formatted 'body' field (text formatters applied)
    $body = $page->getFormatted('body');

### Usage

    $mixed = $page->getFormatted(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Field or property name to retrieve

### Return value

`mixed`

### See Also

*   [Page::getUnformatted()](/api/ref/page/get-unformatted/)
*   [Page::of()](/api/ref/page/of/)

