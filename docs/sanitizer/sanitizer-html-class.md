Sanitize string to ASCII-only HTML class attribute value
--------------------------------------------------------

Note that this does not support all possible characters in an HTML class attribute and instead focuses on the most commonly used ones. Characters allowed in HTML class attributes from this method include: \`-\_:

Available since version **3.0.212**.

### Usage

    $string = $sanitizer->htmlClass(string $value);

### Arguments

Name

Type(s)

Description

`value`

string

### Return value

`string`

