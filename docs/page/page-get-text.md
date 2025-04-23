Same as getMarkup() except returned value is plain text
-------------------------------------------------------

If no `$entities` argument is provided, returned value is entity encoded when output formatting is on, and not entity encoded when output formatting is off.

### Usage

    // basic usage
    $string = $page->getText(string $key);
    
    // usage with all arguments
    $string = $page->getText(string $key, bool $oneLine = false, $entities = null);

### Arguments

Name

Type(s)

Description

`key`

string

Field name or string with field {name} tags in it.

`oneLine` (optional)

bool

Specify true if returned value must be on single line.

`entities` (optional)

bool, null

True to entity encode, false to not. Null for auto, which follows page's outputFormatting state.

### Return value

`string`

### See Also

*   [Page::getMarkup()](/api/ref/page/get-markup/)

