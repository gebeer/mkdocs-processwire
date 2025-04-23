Get classes in array for given class property
---------------------------------------------

Available since version **3.0.204**.

### Usage

    // basic usage
    $array = $inputfield->getClassArray();
    
    // usage with all arguments
    $array = $inputfield->getClassArray(string $property = 'class', bool $assoc = false);

### Arguments

Name

Type(s)

Description

`property` (optional)

string

One of 'wrap', 'header', 'content' or 'input' (or alias 'class')

`assoc` (optional)

bool

Return as associative array where both keys and values are class names? (default=false)

### Return value

`array`

