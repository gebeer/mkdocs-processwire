Get the default language
------------------------

The default language can also be accessed from property [`$languages->default`](/api/ref/languages/default/).

### Example

    if($user->language->id == $languages->getDefault()->id) {
      // user has the default language
    }

### Usage

    $language = $languages->getDefault();

### Return value

[`Language`](/api/ref/language/)

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - when default language hasn't yet been set
    

