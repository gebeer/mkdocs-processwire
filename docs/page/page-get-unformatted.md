Get the unformatted value of a field, regardless of current output formatting state
-----------------------------------------------------------------------------------

When a page’s output formatting state is off, `$page->get('property')` or `$page->property` will produce the same result as this method call.

### Example

    // Get the 'body' field without any text formatters applied
    $body = $page->getUnformatted('body');

### Usage

    $mixed = $page->getUnformatted(string $key);

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

*   [Page::getFormatted()](/api/ref/page/get-formatted/)
*   [Page::of()](/api/ref/page/of/)
*   [Page::setOutputFormatting()](/api/ref/page/set-output-formatting/)
*   [Page::outputFormatting()](/api/ref/page/output-formatting/)

