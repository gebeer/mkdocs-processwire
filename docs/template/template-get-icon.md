Return the icon name used by this template
------------------------------------------

### Usage

    // basic usage
    $string = $template->getIcon();
    
    // usage with all arguments
    $string = $template->getIcon(bool $prefix = false);

### Arguments

Name

Type(s)

Description

`prefix` (optional)

bool

Specify true if you want the icon prefix (icon- or fa-) to be included (default=false).

### Return value

`string`

Returns a font-awesome icon name

