Return the markup value for a given field name or {tag} string
--------------------------------------------------------------

1.  If given a field name (or `name.subname` or `name1|name2|name3`) it will return the markup value as defined by the fieldtype.
2.  If given a string with field names referenced in `{tags}`, it will populate those tags and return the populated string.

### Usage

    $string = $page->getMarkup(string $key);

### Arguments

Name

Type(s)

Description

`key`

string

Field name or markup string with field {name} tags in it

### Return value

`string`

