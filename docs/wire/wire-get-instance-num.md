Get this Wire object’s instance number
--------------------------------------

*   This is a unique number among all other Wire (or derived) instances in the system.
*   If this instance ID has not yet been set, this will set it.
*   Note that this is different from the ProcessWire instance ID.

### Usage

    // basic usage
    $int = $wire->getInstanceNum();
    
    // usage with all arguments
    $int = $wire->getInstanceNum(bool $getTotal = false);

### Arguments

Name

Type(s)

Description

`getTotal` (optional)

bool

Specify true to get the total quantity of Wire instances rather than this instance number.

### Return value

`int`

Instance number

