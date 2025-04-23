Return all sibling pages after this one until matching the one specified
------------------------------------------------------------------------

### Usage

    // basic usage
    $items = $page->nextUntil();
    
    // usage with all arguments
    $items = $page->nextUntil($selector = '', $filter = '', PageArray $siblings = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, Page, array

May either be a selector or Page to stop at. Results will not include this.

`filter` (optional)

string, array

Optional selector to filter matched pages by

`siblings` (optional)

PageArray

Optional PageArray of siblings to use instead (avoid).

### Return value

[`PageArray`](/api/ref/page-array/)

