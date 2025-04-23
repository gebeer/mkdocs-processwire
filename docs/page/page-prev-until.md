Return all sibling pages before this one until matching the one specified
-------------------------------------------------------------------------

### Usage

    // basic usage
    $items = $page->prevUntil();
    
    // usage with all arguments
    $items = $page->prevUntil($selector = '', $filter = '', $siblings = null);

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

PageArray, null

Optional PageArray of siblings to use instead of default.

### Return value

[`PageArray`](/api/ref/page-array/)

