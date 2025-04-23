Given a Selector string, return the Page objects that match in a PageArray.
---------------------------------------------------------------------------

### Usage

    // basic usage
    $items = $pagesType->find(string $selectorString);
    
    // usage with all arguments
    $items = $pagesType->find(string $selectorString, array $options = []);

### Arguments

Name

Type(s)

Description

`selectorString`

string

`options` (optional)

array

Options to modify default behavior:

*   `findOne` (bool): apply optimizations for finding a single page and include pages with 'hidden' status

### Return value

[`PageArray`](/api/ref/page-array/)

### See Also

*   [Pages::find()](/api/ref/pages/find/)

