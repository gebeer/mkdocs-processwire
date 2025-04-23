Set the 'to' name
-----------------

It is preferable to do this with the to() method, but this is provided to ensure that all properties can be set with direct access, i.e. $mailer->toName = 'User Name';

This sets the 'to name' for whatever the last added 'to' email address was.

### Usage

    $m->toName(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

The 'to' name

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if you attempt to set a toName before a to email.
    

