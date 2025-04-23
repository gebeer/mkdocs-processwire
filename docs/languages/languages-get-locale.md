Return the current locale setting
---------------------------------

If using LC\_ALL category and locales change by category, the returned string will be in the format: “category=locale;category=locale”, and so on.

The first and second arguments may optionally be swapped and either can be omitted.

### Usage

    // basic usage
    $string = $languages->getLocale();
    
    // usage with all arguments
    $string = $languages->getLocale($category = 6, $language = null);

### Arguments

Name

Type(s)

Description

`category` (optional)

int, Language, string, null

Optionally specify a PHP LC constant (default=LC\_ALL)

`language` (optional)

Language, string, int, null

Optionally return locale for specific language (default=current locale, regardless of language)

### Return value

`string` `bool`

Locale(s) string or boolean false if not supported by the system.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given a $language argument that is invalid
    

### See Also

*   [Languages::setLocale()](/api/ref/languages/set-locale/)

