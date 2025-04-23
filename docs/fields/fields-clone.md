Create and return a cloned copy of the given Field
--------------------------------------------------

If no name is specified and the new item uses a 'name' field, it will contain a number at the end to make it unique

### Usage

    // basic usage
    $field = $fields->clone($item);
    
    // usage with all arguments
    $field = $fields->clone($item, string $name = '');

### Arguments

Name

Type(s)

Description

`item`

Field, Saveable

Field to clone

`name` (optional)

string

Optionally specify name for new cloned item

### Return value

[`Field`](/api/ref/field/)

$item Returns the new clone on success, or false on failure

