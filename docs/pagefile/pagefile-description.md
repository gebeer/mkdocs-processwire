Get or set the file’s description (with multi-language support).
----------------------------------------------------------------

When not in a multi-language environment, you can still use this method but we recommend using the simpler method of just getting/seting the `Pagefile::$description` property directly instead.

### Example

    // Get a Pagefile to work with
    $pagefile = $page->files->first();
    
    // Setting description
    $pagefile->description('en', 'Setting English description');
    $pagefile->description('de', 'Setting German description');
    
    // Getting description for current language (whatever it happens to be)
    echo $pagefile->description();
    
    // Getting description for language "de"
    echo $pagefile->description('de');

### Usage

    // basic usage
    $string = $pagefile->description();
    
    // usage with all arguments
    $string = $pagefile->description($language = null, $value = null);

### Arguments

Name

Type(s)

Description

`language` (optional)

`value` (optional)

null, string

Specify only when you are setting (single language) rather than getting a value.

### Return value

`string` `array`

