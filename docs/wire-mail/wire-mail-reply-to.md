Set the 'reply-to' email address and optionally name (where supported)
----------------------------------------------------------------------

### Usage

    // basic usage
    $m->replyTo(string $email);
    
    // usage with all arguments
    $m->replyTo(string $email, $name = null);

### Arguments

Name

Type(s)

Description

`email`

string

Must be a single email address or "User Name <user

`name` (optional)

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if provided email was invalid or in blacklist
    

