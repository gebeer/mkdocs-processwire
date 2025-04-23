Turn change tracking ON or OFF
------------------------------

### Example

    // Enable change tracking
    $page->setTrackChanges(true);
    
    // Disable change tracking
    $page->setTrackChanges(false);
    
    // Enable change tracking and remember values
    $page->setTrackChanges(Wire::trackChangesValues);
    $page->setTrackChanges(true);

### Usage

    // basic usage
    $wire->setTrackChanges();
    
    // usage with all arguments
    $wire->setTrackChanges($trackChanges = true);

### Arguments

Name

Type(s)

Description

`trackChanges` (optional)

bool, int

Specify one of the following:

*   `true` (bool): Enables change tracking.
*   `false` (bool): Disables change tracking
*   [`Wire::trackChangesOn`](/api/ref/wire/track-changes-on/) (constant): Enables change tracking (same as specifying boolean true).
*   [`Wire::trackChangesValues`](/api/ref/wire/track-changes-values/) (constant): Enables tracking of changed values when change tracking is already on. This uses more memory since it keeps previous values, so it is not enabled by default. Once enabled, the setting will persist through boolean true|false arguments.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

