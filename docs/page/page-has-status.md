Does this page have the given status?
-------------------------------------

This method is the preferred way to check if a page has a particular status. The status may be specified as one of the [`Page::status`](/api/ref/page/status/) constants or a string representing one of the constants, i.e. `hidden`, `unpublished`, `locked`, and so on.

### Example

    // check if page has hidden status using status name
    if($page->hasStatus('hidden')) { ... }
    
    // check if page has hidden status using status constant
    if($page->hasStatus(Page::statusHidden)) { ... }
    
    // There are also method shortcuts, i.e.
    if($page->isHidden()) { ... }
    if($page->isUnpublished()) { ... }
    if($page->isLocked()) { ... }

### Usage

    $bool = $page->hasStatus($status);

### Arguments

Name

Type(s)

Description

`status`

int, string

Status flag constant or string representation (hidden, locked, unpublished, etc.)

### Return value

`bool`

Returns true if page has the given status, or false if it doesn't.

### See Also

*   [Page::addStatus()](/api/ref/page/add-status/)
*   [Page::removeStatus()](/api/ref/page/remove-status/)
*   [Page::isHidden()](/api/ref/page/is-hidden/)
*   [Page::isUnpublished()](/api/ref/page/is-unpublished/)
*   [Page::isLocked()](/api/ref/page/is-locked/)

