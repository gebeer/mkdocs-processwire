Process input for this Inputfield directly from the POST (or GET) variables
---------------------------------------------------------------------------

This method should pull the value from the given [`$input`](/api/ref/input/) argument, sanitize/validate it, and populate it to the `value` attribute of this Inputfield.

Inputfield modules should implement this method if the built-in one here doesn't solve their need. If this one does solve their need, then they should add any additional sanitization or validation to the [`Inputfield::setAttribute('value', $value)`](/api/ref/inputfield/set-attribute/) method to occur when given the `value` attribute.

### Usage

    $inputfield->processInput(WireInputData $input);

### Arguments

Name

Type(s)

Description

`input`

WireInputData

User input where value should be pulled from (typically [`$input->post`](/api/ref/input/post/))

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

