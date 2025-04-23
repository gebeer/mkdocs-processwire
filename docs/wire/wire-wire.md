Get an API variable, create an API variable, or inject dependencies.
--------------------------------------------------------------------

This method provides the following:

*   Access to API variables:  
    `$pages = $this->wire('pages');`
    
*   Access to current ProcessWire instance:  
    `$wire = $this->wire();`
    
*   Creating new API variables:  
    `$this->wire('widgets', $widgets);`
    
*   Injection of dependencies to Wire derived objects:  
    `$this->wire($widgets);`
    

Most Wire derived objects also support access to API variables directly via `$this->apiVar`.

There is also the `wire()` procedural function, which provides the same access to get API variables. Note however the procedural version does not support creating API variables or injection of dependencies.

### Example

    // Get the 'pages' API variable
    $pages = $this->wire('pages');
    
    // Get the 'pages' API variable using alternate syntax
    $pages = $this->wire()->pages;
    
    // Get all API variables (returns a Fuel object)
    $all = $this->wire('all');
    
    // Get the current ProcessWire instance (no arguments)
    $wire = $this->wire();
    
    // Create a new API variable named 'widgets'
    $this->wire('widgets', $widgets);
    
    // Create new API variable and lock it so nothing can overwrite
    $this->wire('widgets', $widgets, true);
    
    // Alternate syntax for the two above
    $this->wire()->set('widgets', $widgets);
    $this->wire()->set('widgets', $widgets, true); // lock
    
    // Inject dependencies into Wire derived object
    $this->wire($widgets);
    
    // Inject dependencies during construct
    $newPage = $this->wire(new Page());

### Usage

    // basic usage
    $mixed = $wire->wire();
    
    // usage with all arguments
    $mixed = $wire->wire($name = '', $value = null, bool $lock = false);

### Arguments

Name

Type(s)

Description

`name` (optional)

string, object

Name of API variable to retrieve, set, or omit to retrieve the master ProcessWire object.

`value` (optional)

null, mixed

Value to set if using this as a setter, otherwise omit.

`lock` (optional)

bool

When using as a setter, specify true if you want to lock the value from future changes (default=false).

### Return value

`mixed`

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

