Render given $fieldName using site/templates/fields/ markup file
----------------------------------------------------------------

Shorter aliases of this method include:

*   `$page->render('fieldName', $file);`
*   `$page->render->fieldName;`
*   `$page->_fieldName_;`

This method expects that there is a file in `/site/templates/fields/` to render the field with:

*   `/site/templates/fields/fieldName.php`
*   `/site/templates/fields/fieldName.templateName.php`
*   `/site/templates/fields/fieldName/$file.php` (using $file argument)
*   `/site/templates/fields/$file.php` (using $file argument)
*   `/site/templates/fields/$file/fieldName.php` (using $file argument, must have trailing slash)
*   `/site/templates/fields/$file.fieldName.php` (using $file argument, must have trailing period)

Note that the examples above showing $file require that the `$file` argument is specified.

### Example

    // Render output for the 'images' field (assumes you have implemented an output file)
    echo $page->renderField('images');

### Usage

    // basic usage
    $mixed = $page->renderField(string $fieldName);
    
    // usage with all arguments
    $mixed = $page->renderField(string $fieldName, string $file = '', $value = null);

### Arguments

Name

Type(s)

Description

`fieldName`

string

May be any custom field name or native page property.

`file` (optional)

string

Optionally specify file (in site/templates/fields/) to render with (may omit .php extension).

`value` (optional)

mixed, null

Optionally specify value to render, otherwise it will be pulled from this $page.

### Return value

`mixed` `string`

Returns the rendered value of the field

