Clears out any tracked changes and turns change tracking ON or OFF
------------------------------------------------------------------

Use this method when you want to clear a list of tracked changes on the page. Note that any changes are still present, but ProcessWire no longer knows they had been changed. Meaning, the changes won't be available to the `$page->isChanged()` and `$page->getChanges()` methods, and the changes might be skipped over if/when the page is saved.

### Example

    // Clear any changes that have been tracked and start fresh
    $page->resetTrackChanges();

### Usage

    // basic usage
    $page->resetTrackChanges();
    
    // usage with all arguments
    $page->resetTrackChanges(bool $trackChanges = true);

### Arguments

Name

Type(s)

Description

`trackChanges` (optional)

bool

True to turn change tracking ON, or false to turn OFF. Default of true is assumed.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### See Also

*   [Page::isChanged()](/api/ref/page/is-changed/)
*   [Page::getChanges()](/api/ref/page/get-changes/)
*   [Page::trackChanges()](/api/ref/page/track-changes/)

