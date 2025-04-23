Delete all log files
--------------------

Available since version **3.0.214**.

### Usage

    // basic usage
    $array = $log->deleteAll();
    
    // usage with all arguments
    $array = $log->deleteAll(bool $throw = false);

### Arguments

Name

Type(s)

Description

`throw` (optional)

bool

Throw WireException if any delete fails? (default=false)

### Return value

`array`

Basenames of deleted log files

