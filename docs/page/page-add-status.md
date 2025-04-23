Add the specified status to this page
-------------------------------------

This is the preferred way to add a new status to a page. There is also a corresponding [`Page::removeStatus()`](/api/ref/page/remove-status/) method.

### Example

    // Add hidden status to the page using status name
    $page->addStatus('hidden');
    
    // Add hidden status to the page using status constant
    $page->addStatus(Page::statusHidden); 

### Usage

    $page->addStatus($statusFlag);

### Arguments

Name

Type(s)

Description

`statusFlag`

int, string

Status flag constant or string representation (hidden, locked, unpublished, etc.)

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### See Also

*   [Page::removeStatus()](/api/ref/page/remove-status/)
*   [Page::hasStatus()](/api/ref/page/has-status/)

