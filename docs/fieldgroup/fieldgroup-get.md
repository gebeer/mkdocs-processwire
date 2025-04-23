Get a Fieldgroup property or a Field.
-------------------------------------

It is preferable to use [`Fieldgroup::getField()`](/api/ref/fieldgroup/get-field/) to retrieve fields from the Fieldgroup because the scope of this `get()` method means it can return more than just Field object.

### Usage

    $field = $fieldgroup->get($key);

### Arguments

Name

Type(s)

Description

`key`

string, int

Property name to retrieve, or Field name

### Return value

[`Field`](/api/ref/field/) `string` `int` `null` `array`

Value of item requested, or null if it doesn't exist.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

