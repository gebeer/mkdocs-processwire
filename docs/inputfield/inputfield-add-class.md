Add a class or classes to this Inputfield (or a wrapping element)
-----------------------------------------------------------------

If given a class name that’s already present, it won’t be added again.

**Formatted string option (3.0.204+):**  
Classes can be added by formatted string that dictates what Inputfield element they should be added to, in the format `element:classNames` like in this example below:

Each line represents a group containing an element name and one or more space-separated classes. Groups may be separated by newline (like above) or with a comma. The element name may be any one of the following:

*   `wrap`: The .Inputfield element that wraps the header and content
*   `header`: The .InputfieldHeader element, typically a `<label>`.
*   `content`: The .InputfieldContent element that wraps the input(s), typically a `<div>`.
*   `input`: The primary `<input>` element(s) that accept input for the Inputfield.
*   `class`: This is the same as the 'input' type, just an alias.

Class names prefixed with a minus sign i.e. `-class` will be removed rather than added.

### Examples

    // Add class "foobar" to input element
    $inputfield->addClass('foobar');
    
    // Add three classes to input element
    $inputfield->addClass('foo bar baz');
    
    // Add class "foobar" to .Inputfield wrapping element
    $inputfield->addClass('foobar', 'wrapClass');
    
    // Add classes while specifying Inputfield element (3.0.204+)
    $inputfield->addClass('wrap:card, header:card-header, content:card-body'); 

    wrap:card card-default
    header:card-header
    content:card-body
    input:form-input input-checkbox

### Usage

    // basic usage
    $inputfield->addClass($class);
    
    // usage with all arguments
    $inputfield->addClass($class, string $property = 'class');

### Arguments

Name

Type(s)

Description

`class`

string, array

Specify one of the following:

*   Class name you want to add.
*   Multiple space-separated class names you want to add.
*   Array of class names you want to add (since 3.0.16).
*   Formatted string of classes as described in method description (since 3.0.204+).

`property` (optional)

string

Optionally specify the type of class you want to add:

*   Omit for the default (which is "class").
*   `class` (string): Add class to the input element (or whatever the Inputfield default is).
*   `wrapClass` (string): Add class to ".Inputfield" wrapping element, the most outer level element used for this Inputfield.
*   `headerClass` (string): Add class to ".InputfieldHeader" label element.
*   `contentClass` (string): Add class to ".InputfieldContent" wrapping element.
*   Or some other named class attribute designated by a descending Inputfield.
*   You can optionally omit the `Class` suffix in 3.0.204+, i.e. `wrap` rather than `wrapClass`.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### See Also

*   [Inputfield::hasClass()](/api/ref/inputfield/has-class/)
*   [Inputfield::removeClass()](/api/ref/inputfield/remove-class/)

