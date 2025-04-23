Like find() except returns array of IDs rather than Page objects
----------------------------------------------------------------

*   This is a faster method to use when you only need to know the matching page IDs.
*   The default behavior is to simply return a regular PHP array of matching page IDs in order.
*   The alternate behavior (verbose) returns more information for each match, as outlined below.

**Verbose option:**  
When specifying boolean true for the `$options` argument (or using the `verbose` option), the return value is an array of associative arrays, with each of those associative arrays containing `id`, `parent_id` and `templates_id` keys for each page.

Available since version **3.0.46**.

### Example

    // returns array of page IDs (integers) like [ 1234, 1235, 1236 ]
    $a = $pages->findIDs("foo=bar");
    
    // verbose option: returns array of associative arrays, each with id, parent_id and templates_id
    $a = $pages->findIDs("foo=bar", true);

### Usage

    // basic usage
    $array = $pages->findIDs($selector);
    
    // usage with all arguments
    $array = $pages->findIDs($selector, $options = []);

### Arguments

Name

Type(s)

Description

`selector`

string, array, Selectors

Selector to find page IDs.

`options` (optional)

array, bool, int, string

Options to modify behavior.

*   `verbose` (bool|int|string): Specify true to make return value array of associative arrays, each with id, parent\_id, templates\_id. Specify integer `2` or string `*` to return verbose array of associative arrays, each with all columns from pages table.
*   `indexed` (bool): Index by page ID? (default=false) Added 3.0.172
*   The verbose option above can also be specified as alternative to the $options argument.
*   See `Pages::find()` $options argument for additional options.

### Return value

`array`

Array of page IDs, or in verbose mode: array of arrays, each with id, parent\_id and templates\_id keys.

