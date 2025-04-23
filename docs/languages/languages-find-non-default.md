Find and return all languages except default language
-----------------------------------------------------

### Usage

    // basic usage
    $items = $languages->findNonDefault();
    
    // usage with all arguments
    $items = $languages->findNonDefault(string $selector = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

string

Optionally filter by a selector string

### Return value

[`PageArray`](/api/ref/page-array/)

