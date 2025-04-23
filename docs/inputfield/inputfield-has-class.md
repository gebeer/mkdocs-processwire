Does this Inputfield have the given class name (or names)?
----------------------------------------------------------

### Example

    if($inputfield->hasClass('foo')) {
      // This Inputfield has a class attribute with "foo"
    }
    
    if($inputfield->hasClass('bar', 'wrapClass')) {
      // This .Inputfield wrapper has a class attribute with "bar"
    }
    
    if($inputfield->hasClass('foo bar')) {
      // This Inputfield has both "foo" and "bar" classes (Since 3.0.16)
    }

### Usage

    // basic usage
    $bool = $inputfield->hasClass($class);
    
    // usage with all arguments
    $bool = $inputfield->hasClass($class, string $property = 'class');

### Arguments

Name

Type(s)

Description

`class`

string, array

Specify class name or one of the following:

*   String containing name of class you want to check (string).
*   String containing Space separated string class names you want to check, all must be present for this method to return true. (Since 3.0.16)
*   Array of class names you want to check, all must be present for this method to return true. (Since 3.0.16)

`property` (optional)

string

Optionally specify property you want to pull class from:

*   `class` (string): Default setting. Class for the input element (or whatever the Inputfield default is).
*   `wrapClass` (string): Class for the ".Inputfield" wrapping element, the most outer level element used for this Inputfield.
*   `headerClass` (string): Class for the ".InputfieldHeader" label element.
*   `contentClass` (string): Class for the ".InputfieldContent" wrapping element.
*   Or some other class property defined by a descending Inputfield class.

### Return value

`bool`

### See Also

*   [Inputfield::addClass()](/api/ref/inputfield/add-class/)
*   [Inputfield::removeClass()](/api/ref/inputfield/remove-class/)

