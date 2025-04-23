Return all parents from current page till the one matched by $selector
----------------------------------------------------------------------

This duplicates the jQuery parentsUntil() function in ProcessWire.

### Usage

    // basic usage
    $items = $page->parentsUntil();
    
    // usage with all arguments
    $items = $page->parentsUntil($selector = '', $filter = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, Page, array

May either be a selector sor Page to stop at. Results will not include this.

`filter` (optional)

string, array

Optional selector to filter matched pages by

### Return value

[`PageArray`](/api/ref/page-array/)

