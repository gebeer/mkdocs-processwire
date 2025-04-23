Render given $value using /site/templates/fields/ markup file
-------------------------------------------------------------

See the documentation for the [`Page::renderField()`](/api/ref/page/render-field/) method for information about the `$file` argument.

### Example

    // Render a value using site/templates/fields/my-images.php custom output template
    $images = $page->images;
    echo $page->renderValue($images, 'my-images'); 

### Usage

    // basic usage
    $mixed = $page->renderValue(mixed $value);
    
    // usage with all arguments
    $mixed = $page->renderValue(mixed $value, string $file = '');

### Arguments

Name

Type(s)

Description

`value`

mixed

Value to render

`file` (optional)

string

Optionally specify file (in site/templates/fields/) to render with (may omit .php extension)

### Return value

`mixed` `string`

Returns rendered value

