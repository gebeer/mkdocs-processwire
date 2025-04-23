Set a new API variable
----------------------

Alias of $this->wire(), but for setting only, for syntactic convenience. i.e. $this->wire()->set($key, $value);

### Usage

    // basic usage
    $wire->set(string $key, $value);
    
    // usage with all arguments
    $wire->set(string $key, $value, bool $lock = false);

### Arguments

Name

Type(s)

Description

`key`

string

API variable name to set

`value`

Wire, mixed

Value of API variable

`lock` (optional)

bool

Whether to lock the value from being overwritten

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

