Return all URLs that this page can be accessed from (excluding URL segments and pagination)
-------------------------------------------------------------------------------------------

This includes the current page URL, any other language URLs (for which page is active), and any past (historical) URLs the page was previously available at (which will redirect to it).

*   Returned URLs do not include additional URL segments or pagination numbers.
*   Returned URLs are indexed by language name, i.e. “default”, “fr”, “es”, etc.
*   If multi-language URLs not installed, then index is just “default”.
*   Past URLs are indexed by language; then ISO-8601 date, i.e. “default;2016-08-11T07:44:43-04:00”, where the date represents the last date that URL was considered current.
*   If PagePathHistory core module is not installed then past/historical URLs are excluded.
*   You can disable past/historical or multi-language URLs by using the $options argument.

Available since version **3.0.107**.

### Usage

    // basic usage
    $array = $page->urls();
    
    // usage with all arguments
    $array = $page->urls(array $options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

array

Options to modify default behavior:

*   `http` (bool): Make URLs include current scheme and hostname (default=false).
*   `past` (bool): Include past/historical URLs? (default=true)
*   `languages` (bool): Include other language URLs when supported/available? (default=true).
*   `language` (Language|int|string): Include only URLs for this language (default=null). Note: the `languages` option must be true if using the `language` option.

### Return value

`array`

### See Also

*   [Page::addUrl()](/api/ref/page/add-url/)
*   [page::removeUrl()](/api/ref/page/remove-url/)

