Return or manage messages recorded by just this object or all Wire objects
--------------------------------------------------------------------------

This method returns and manages messages that were previously set by [`Wire::message()`](/api/ref/wire/message/).

### Example

    // Get messages for one object
    $messages = $obj->messages();
    
    // Get first message in object
    $message = $obj->messages('first');
    
    // Get messages for all Wire objects
    $messages = $obj->messages('all');
    
    // Get and clear all messages for all Wire objects
    $messages = $obj->messages('clear all');

### Usage

    // basic usage
    $notices = $wire->messages();
    
    // usage with all arguments
    $notices = $wire->messages($options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

string, array

One or more of array elements or space separated string of:

*   `first` - only first item will be returned
*   `last` - only last item will be returned
*   `all` - include all messages, including those beyond the scope of this object
*   `clear` - clear out all items that are returned from this method
*   `array` - return an array of strings rather than series of Notice objects.
*   `string` - return a newline separated string rather than array/Notice objects.

### Return value

`Notices` `array` `string`

Array of `NoticeMessage` messages, or string if last, first or str option was specified.

