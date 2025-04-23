Return the number of pages in this type matching the given selector string
--------------------------------------------------------------------------

### Usage

    // basic usage
    $int = $pagesType->count();
    
    // usage with all arguments
    $int = $pagesType->count(string $selectorString = '', array $options = []);

### Arguments

Name

Type(s)

Description

`selectorString` (optional)

string

Optional, if omitted then returns count of all pages of this type

`options` (optional)

array

Options to modify default behavior (see $pages->count method for details)

### Return value

`int`

### See Also

*   [Pages::count()](/api/ref/pages/count/)

