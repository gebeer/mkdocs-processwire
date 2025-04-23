Find and return all languages except current user language
----------------------------------------------------------

### Usage

    // basic usage
    $items = $languages->findOther();
    
    // usage with all arguments
    $items = $languages->findOther($selector = '', $excludeLanguage = null);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, Language

Optionally filter by a selector string

`excludeLanguage` (optional)

Language, null

optionally specify language to exclude, if not user language (can also be 1st arg)

### Return value

[`PageArray`](/api/ref/page-array/)

