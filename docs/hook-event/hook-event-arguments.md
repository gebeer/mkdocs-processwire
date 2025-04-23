Retrieve or set a hooked function argument
------------------------------------------

### Example

    // Retrieve first argument by index (0=first)
    $page = $event->arguments(0);
    
    // Retrieve array of all arguments
    $arguments = $event->arguments();
    
    // Retrieve argument by name
    $page = $event->arguments('page');
    
    // Set first argument by index
    $event->arguments(0, $page);
    
    // Set first argument by name
    $event->arguments('page', $page); 

### Usage

    // basic usage
    $array = $event->arguments();
    
    // usage with all arguments
    $array = $event->arguments(int $n = null, mixed $value = null);

### Arguments

Name

Type(s)

Description

`n` (optional)

int

Zero based number of the argument you want to retrieve, where 0 is the first. May also be a string containing the argument name. Omit to return array of all arguments.

`value` (optional)

mixed

Value that you want to set to this argument, or omit to only return the argument.

### Return value

`array` `null` `mixed`

