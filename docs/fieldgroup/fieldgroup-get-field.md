Get a field that is part of this fieldgroup
-------------------------------------------

Same as [`Fieldgroup::get()`](/api/ref/fieldgroup/get/) except that it only checks fields, not other properties of a fieldgroup. Meaning, this is the preferred way to retrieve a Field from a Fieldgroup.

### Usage

    // basic usage
    $field = $fieldgroup->getField($key);
    
    // usage with all arguments
    $field = $fieldgroup->getField($key, $useFieldgroupContext = false);

### Arguments

Name

Type(s)

Description

`key`

string, int, Field

Field object, name or id.

`useFieldgroupContext` (optional)

bool, string

Optionally specify one of the following (default=false):

*   `true` (boolean) Returned Field will be a clone of the original with context data set.
*   Specify a namespace (string) to retrieve context within that namespace.

### Return value

[`Field`](/api/ref/field/) `null`

Field object when present in this Fieldgroup, or null if not.

