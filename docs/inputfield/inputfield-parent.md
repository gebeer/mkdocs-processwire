Get or set parent of Inputfield
-------------------------------

This convenience method performs the same thing as getParent() and setParent().

To get parent, specify no arguments. It will return null if no parent assigned, or an InputfieldWrapper instance of the parent.

To set parent, specify an InputfieldWrapper for the $parent argument. The return value is the current Inputfield for fluent interface.

Available since version **3.0.110**.

### Usage

    // basic usage
    $inputfield = $inputfield->parent();
    
    // usage with all arguments
    $inputfield = $inputfield->parent($parent = null);

### Arguments

Name

Type(s)

Description

`parent` (optional)

null, InputfieldWrapper

### Return value

`null` [`Inputfield`](/api/ref/inputfield/) [`InputfieldWrapper`](/api/ref/inputfield-wrapper/)

