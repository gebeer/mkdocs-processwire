Get value of Inputfield by name
-------------------------------

This traverses all children recursively to find the requested Inputfield, and get the value attribute from it. A value of null is returned if the Inputfield cannot be found.

Available since version **3.0.172**.

### Usage

    $mixed = $inputfieldWrapper->getValueByName(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

### Return value

`mixed`

