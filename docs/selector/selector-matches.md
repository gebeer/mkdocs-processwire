Does this Selector match the given value?
-----------------------------------------

If the value held by this Selector is an array of values, it will check if any one of them matches the value supplied here.

### Usage

    $bool = $selector->matches($value);

### Arguments

Name

Type(s)

Description

`value`

string, int, Wire, array

If given a Wire, then matches will also operate on OR field=value type selectors, where present

### Return value

`bool`

