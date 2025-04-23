Get or set editable state for this Inputfield
---------------------------------------------

When set to false, the [`Inputfield::processInput()`](/api/ref/inputfield/process-input/) method won't be called by parent InputfieldWrapper, effectively skipping over input processing entirely for this Inputfield.

### Usage

    // basic usage
    $bool = $inputfield->editable();
    
    // usage with all arguments
    $bool = $inputfield->editable($setEditable = null);

### Arguments

Name

Type(s)

Description

`setEditable` (optional)

bool, null

Specify true or false to set the editable state, or omit just to get the editable state.

### Return value

`bool`

Returns the current editable state.

