Does current user have edit access for page fields in given language?
---------------------------------------------------------------------

### Usage

    $bool = $languages->editable($language);

### Arguments

Name

Type(s)

Description

`language`

Language, int, string

Language id, name or object, or string "none" to refer to non-multi-language fields

### Return value

`bool`

True if editable, false if not

