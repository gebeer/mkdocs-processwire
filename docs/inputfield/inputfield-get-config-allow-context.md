Return a list of config property names allowed for fieldgroup/template context
------------------------------------------------------------------------------

These should be the names of Inputfields returned by [`Inputfield::getConfigInputfields()`](/api/ref/inputfield/get-config-inputfields/) or [`Inputfield::getConfigArray()`](/api/ref/inputfield/get-config-array/) that are allowed in fieldgroup/template context.

The config property names specified here are allowed to be configured within the context of a given [`Fieldgroup`](/api/ref/fieldgroup/), enabling the user to configure them independently per template in the admin.

This is the equivalent to the \[`Fieldtype::getConfigAllowContext()`\](/api/ref/fieldtype/get-config-allow-con`Fieldtype::getConfigAllowContext()`/) method, but for the "Input" tab rather than the "Details" tab.

### Usage

    $array = $inputfield->getConfigAllowContext(Field $field);

### Arguments

Name

Type(s)

Description

`field`

Field

### Return value

`array`

of Inputfield names

