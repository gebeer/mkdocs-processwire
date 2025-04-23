Set the unformatted value of a field, regardless of current output formatting state
-----------------------------------------------------------------------------------

Use this when setting an unformatted value to a page that has (or might have) output formatting enabled. This will save you the steps of checking the output formatting state, turning it off, setting the value, and turning it back on again (if it was on). Note that the output formatting distinction matters for some field types and not others, just depending on the case—this method is safe to use either way.

Make sure you do not use this to set an already formatted value to a Page (like some text that has been entity encoded). This method skips over some of the checks that might otherwise flag the page as corrupted.

Available since version **3.0.169**.

### Example

    // good usage
    $page->setUnformatted('title', 'This & That');
    
    // bad usage
    $page->setUnformatted('title', 'This &amp; That'); 

### Usage

    $self = $page->setUnformatted(string $key, mixed $value);

### Arguments

Name

Type(s)

Description

`key`

string

`value`

mixed

### Return value

`self`

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given an object value that indicates it is already formatted.
    

### See Also

*   [Page::getUnformatted()](/api/ref/page/get-unformatted/)
*   [Page::of()](/api/ref/page/of/)
*   [Page::setOutputFormatting()](/api/ref/page/set-output-formatting/)
*   [Page::outputFormatting()](/api/ref/page/output-formatting/)

