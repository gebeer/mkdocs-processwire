Clone the given Template
------------------------

Note that this also clones the Fieldgroup if the template being cloned has its own named fieldgroup.

### Usage

    // basic usage
    $bool = $templates->clone($item);
    
    // usage with all arguments
    $bool = $templates->clone($item, string $name = '');

### Arguments

Name

Type(s)

Description

`item`

Template, Saveable

Template to clone

`name` (optional)

string

Name of new template that will be created, or omit to auto-assign.

### Return value

`bool` [`Template`](/api/ref/template/)

$item Returns the new Template on success, or false on failure

