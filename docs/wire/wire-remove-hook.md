Given a Hook ID, remove the hook
--------------------------------

Once a hook is removed, it will no longer execute.

### Examples

    // Add a hook
    $hookID = $pages->addHookAfter('find', function($event) {
      // do something
    });
    
    // Remove the hook
    $pages->removeHook($hookID); 

    // Hook function that removes itself
    $hookID = $pages->addHookAfter('find', function($event) {
      // do something
      $event->removeHook(null); // note: calling removeHook on $event
    });

### Usage

    $wire->removeHook($hookId);

### Arguments

Name

Type(s)

Description

`hookId`

string, array, null

ID of hook to remove (ID is returned by the addHook() methods) Since 3.0.137 it may also be an array or CSV string of hook IDs to remove.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

