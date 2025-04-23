Set the 'from' name
-------------------

It is preferable to do this with the from() method, but this is provided to ensure that all properties can be set with direct access, i.e. $mailer->fromName = 'User Name';

### Usage

    $m->fromName(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

The 'from' name

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

