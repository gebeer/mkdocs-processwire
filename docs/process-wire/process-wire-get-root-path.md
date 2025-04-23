Get root path, check it, and optionally auto-detect it if not provided
----------------------------------------------------------------------

### Usage

    // basic usage
    $string = $wire::getRootPath();
    
    // usage with all arguments
    $string = $wire::getRootPath($rootPath = '');

### Arguments

Name

Type(s)

Description

`rootPath` (optional)

bool, string

Root path if already known, in which case we’ll just modify as needed …or specify boolean true to get absolute root path, which disregards any symbolic links to core.

### Return value

`string`

