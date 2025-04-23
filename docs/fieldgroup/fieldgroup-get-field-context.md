Get a Field that is part of this Fieldgroup, in the context of this Fieldgroup.
-------------------------------------------------------------------------------

Returned Field will be a clone of the original with additional context data already populated to it.

### Usage

    // basic usage
    $field = $fieldgroup->getFieldContext($key);
    
    // usage with all arguments
    $field = $fieldgroup->getFieldContext($key, string $namespace = '');

### Arguments

Name

Type(s)

Description

`key`

string, int, Field

Field object, name or id.

`namespace` (optional)

string

Optional namespace string for context

### Return value

[`Field`](/api/ref/field/) `null`

