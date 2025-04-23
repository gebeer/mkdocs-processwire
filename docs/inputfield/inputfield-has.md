Does this Inputfield have the requested property or attribute?
--------------------------------------------------------------

### Example

    if($item->has('some_property')) {
      // the item has some_property
    }

### Usage

    $bool = $inputfield->has(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Requested property or attribute.

### Return value

`bool`

True if it has it, false if it doesn't

