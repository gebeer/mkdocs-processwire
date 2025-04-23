Record an informational or 'success' message in the message log (messages.txt)
------------------------------------------------------------------------------

### Example

    // Log message to messages.txt log
    $log->message("User updated profile"); 

### Usage

    // basic usage
    $wire = $log->message(string $text);
    
    // usage with all arguments
    $wire = $log->message(string $text, $flags = 0);

### Arguments

Name

Type(s)

Description

`text`

string

Message to log

`flags` (optional)

bool, int

Specify boolean true to also have the message displayed interactively (admin only).

### Return value

[`Wire`](/api/ref/wire/) `WireLog`

