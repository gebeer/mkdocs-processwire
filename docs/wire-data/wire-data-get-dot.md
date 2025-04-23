Get a property via dot syntax: field.subfield.subfield
------------------------------------------------------

Some classes descending WireData may choose to add a call to this as part of their get() method as a syntax convenience.

### Example

    $value = $item->get("parent.title"); 

### Usage

    $mixed = $wireData->getDot(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Name of property you want to retrieve in "a.b" or "a.b.c" format

### Return value

`null` `mixed`

Returns value if found or null if not

