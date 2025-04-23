Entity encode a string with optional Markdown support.
------------------------------------------------------

*   Markdown support provided with second argument.
*   If string is already entity-encoded it will first be decoded.

### Usage

    // basic usage
    $string = $inputfield->entityEncode(string $str);
    
    // usage with all arguments
    $string = $inputfield->entityEncode(string $str, $markdown = false);

### Arguments

Name

Type(s)

Description

`str`

string

String to encode

`markdown` (optional)

bool, int

Optionally specify one of the following:

*   `true` (boolean): To allow Markdown using default "textFormat" setting (which is basic Markdown by default).
*   `false` (boolean): To disallow Markdown support (this is the default when $markdown argument omitted).
*   [`Inputfield::textFormatNone`](/api/ref/inputfield/<code>Inputfield::textFormatNone</code>-format-none/) (constant): Disallow Markdown support (default).
*   [`Inputfield::textFormatBasic`](/api/ref/inputfield/<code>Inputfield::textFormatBasic</code>-format-basic/) (constant): To support basic/inline Markdown.
*   [`Inputfield::textFormatMarkdown`](/api/ref/inputfield/<code>Inputfield::textFormatMarkdown</code>-format-markdown/) (constant): To support full Markdown and HTML.

### Return value

`string`

Entity encoded string or HTML string

