Save the entire page to the database, or just a field from it
-------------------------------------------------------------

This is the same as calling `$pages->save($page);` or `$pages->saveField($page, $field)`, but calling directly on the $page like this may be more convenient in many instances.

If you want to hook into the save operation, hook into one of the many Pages class hooks referenced in the 'See Also' section.

### Example

    // Save the page
    $page->save();
    
    // Save just the 'title' field from the page
    $page->save('title');

### Usage

    // basic usage
    $bool = $page->save();
    
    // usage with all arguments
    $bool = $page->save($field = null, array $options = []);

### Arguments

Name

Type(s)

Description

`field` (optional)

Field, string

Optional field to save (name of field or Field object)

`options` (optional)

array

See Pages::save() documentation for options. You may also specify $options as the first argument if no $field is needed.

### Return value

`bool`

Returns true on success false on fail

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - on database error
    

### See Also

*   [Pages::save()](/api/ref/pages/save/)
*   [Pages::saveField()](/api/ref/pages/save-field/)
*   [Pages::saveReady()](/api/ref/pages/save-ready/)
*   [Pages::saveFieldReady()](/api/ref/pages/save-field-ready/)
*   [Pages::saved()](/api/ref/pages/saved/)
*   [Pages::fieldSaved()](/api/ref/pages/field-saved/)

