Set any email header
--------------------

*   Multiple calls will append existing headers.
*   To remove an existing header, specify NULL as the value.

### Usage

    $m->header($key, string $value);

### Arguments

Name

Type(s)

Description

`key`

string, array

Header name

`value`

string

Header value or specify null to unset

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

