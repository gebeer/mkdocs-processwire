Remove the specified status from this page
------------------------------------------

This is the preferred way to remove a status from a page. There is also a corresponding [`Page::addStatus()`](/api/ref/page/add-status/) method.

### Example

    // Remove hidden status from the page using status name
    $page->removeStatus('hidden');
    
    // Remove hidden status from the page using status constant
    $page->removeStatus(Page::statusHidden);

### Usage

    $page->removeStatus($statusFlag);

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

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If you attempt to remove [`Page::statusSystem`](/api/ref/page/status-system/) or [`Page::statusSystemID`](/api/ref/page/status-system-i-d/) statuses without first adding [`Page::statusSystemOverride`](/api/ref/page/status-system-override/) status.
    

### See Also

*   [Page::addStatus()](/api/ref/page/add-status/)
*   [Page::hasStatus()](/api/ref/page/has-status/)

