Set the system status to one of the ProcessWire::status\* constants
-------------------------------------------------------------------

This also triggers init/ready functions for modules, when applicable.

### Usage

    // basic usage
    $wire->setStatus(int $status);
    
    // usage with all arguments
    $wire->setStatus(int $status, array $data = []);

### Arguments

Name

Type(s)

Description

`status`

int

`data` (optional)

array

Associative array of any extra data to pass along to include files as locally scoped vars (3.0.142+)

