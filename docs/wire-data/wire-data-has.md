Does this object have the given property?
-----------------------------------------

### Example

    if($item->has('some_property')) {
      // the item has some_property
    }

### Usage

    $bool = $wireData->has(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property you want to check.

### Return value

`bool`

True if it has the property, false if not.

