Get the current language or optionally a specific named language
----------------------------------------------------------------

*   This method is not entirely necessary but is here to accompany the setLanguage() method for syntax convenience.
*   If you specify a `$name` argument, this method works the same as the [`$languages->get($name)`](/api/ref/languages/get/) method.
*   If you call with no arguments, it returns the current user language, same as [`$user->language`](/api/ref/user/language/), but using this method may be preferable in some contexts, depending on how your IDE understands API calls.

Available since version **3.0.127**.

### Usage

    // basic usage
    $language = $languages->getLanguage();
    
    // usage with all arguments
    $language = $languages->getLanguage($name = '');

### Arguments

Name

Type(s)

Description

`name` (optional)

string, int

Specify language name (or ID) to get a specific language, or omit to get current language

### Return value

`Language` [`NullPage`](/api/ref/null-page/) `null`

