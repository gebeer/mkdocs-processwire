Returns the basename of this Pagefile (name and extension, without disk path).
------------------------------------------------------------------------------

### Usage

    // basic usage
    $string = $pagefile->basename();
    
    // usage with all arguments
    $string = $pagefile->basename(bool $ext = true);

### Arguments

Name

Type(s)

Description

`ext` (optional)

bool

Specify false to exclude the extension (default=true)

### Return value

`string`

