Is this Inputfield empty? (Value attribute reflects an empty state)
-------------------------------------------------------------------

Return true if this field is empty (no value or blank value), or false if it’s not empty.

Used by the 'required' check to see if the field is populated, and descending Inputfields may override this according to their own definition of 'empty'.

### Usage

    $bool = $inputfield->isEmpty();

### Return value

`bool`

