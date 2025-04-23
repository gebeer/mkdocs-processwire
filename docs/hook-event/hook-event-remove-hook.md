Remove a hook by ID
-------------------

To remove the hook that this event is for, call it with the $hookId argument as null or blank.

### Example

    // Remove this hook event, preventing it from executing again
    $event->removeHook(null); 

### Usage

    $hookEvent = $event->removeHook($hookId);

### Arguments

Name

Type(s)

Description

`hookId`

string, HookEvent, null

ID of hook to remove (ID is returned by the addHook() methods) Since 3.0.137 it may also be an array or CSV string of hook IDs to remove.

### Return value

[`HookEvent`](/api/ref/hook-event/) [`WireData`](/api/ref/wire-data/)

$this

