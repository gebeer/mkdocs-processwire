Given a Selector string, return the Page objects that match in a PageArray.
---------------------------------------------------------------------------

*   This is one of the most commonly used API methods in ProcessWire.
*   If you only need to find one page, use the `Pages::get()` or `Pages::findOne()` method instead (and note the difference).
*   If you need to find a huge quantity of pages (like thousands) without limit or pagination, look at the `Pages::findMany()` method.

### Example

    // Find all pages using template "building" with 25 or more floors
    $skyscrapers = $pages->find("template=building, floors>=25");

### Usage

    // basic usage
    $items = $pages->find($selector);
    
    // usage with all arguments
    $items = $pages->find($selector, $options = []);

### Arguments

Name

Type(s)

Description

`selector`

string, int, array, Selectors

Specify selector (standard usage), but can also accept page ID or array of page IDs.

`options` (optional)

array, string

One or more options that can modify certain behaviors. May be associative array or "key=value" selector string.

*   `findOne` (bool): Apply optimizations for finding a single page (default=false).
*   `findAll` (bool): Find all pages with no exclusions, same as "include=all" option (default=false).
*   `findIDs` (bool|int): 1 to get array of page IDs, true to return verbose array, 2 to return verbose array with all cols in 3.0.153+. (default=false).
*   `getTotal` (bool): Whether to set returning PageArray's "total" property (default=true, except when findOne=true).
*   `loadPages` (bool): Whether to populate the returned PageArray with found pages (default=true). The only reason why you'd want to change this to false would be if you only needed the count details from the PageArray: getTotal(), getStart(), getLimit, etc. This is intended as an optimization for $pages->count(). Does not apply if $selector argument is an array.
*   `cache` (bool): Allow caching of selectors and loaded pages? (default=true). Also sets loadOptions\[cache\].
*   `allowCustom` (boolean): Allow use of \_custom="another selector" in given $selector? For specific uses. (default=false)
*   `caller` (string): Optional name of calling function, for debugging purposes, i.e. "pages.count" (default=blank).
*   `include` (string): Optional inclusion mode of 'hidden', 'unpublished' or 'all'. (default=none). Typically you would specify this directly in the selector string, so the option is mainly useful if your first argument is not a string.
*   `stopBeforeID` (int): Stop loading pages once page matching this ID is found (default=0).
*   `startAfterID` (int): Start loading pages once page matching this ID is found (default=0).
*   `lazy` (bool): Specify true to force lazy loading. This is the same as using the Pages::findMany() method (default=false).
*   `loadOptions` (array): Optional associative array of options to pass to getById() load options.

### Return value

[`PageArray`](/api/ref/page-array/) `array`

PageArray of that matched the given selector, or array of page IDs (if using findIDs option).

Non-visible pages are excluded unless an "include=x" mode is specified in the selector (where "x" is "hidden", "unpublished" or "all"). If "all" is specified, then non-accessible pages (via access control) can also be included.

