Set the email to address
------------------------

Each added email addresses appends to any addresses already supplied, unless you specify NULL as the email address, in which case it clears them all.

### Usage

    // basic usage
    $m->to();
    
    // usage with all arguments
    $m->to($email = null, string $name = null);

### Arguments

Name

Type(s)

Description

`email` (optional)

string, array, null

Specify any ONE of the following:

*   Single email address or "User Name <user

`name` (optional)

string

Optionally provide a TO name, applicable only when specifying #1 (single email) for the first argument.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if any provided emails were invalid or in blacklist
    

