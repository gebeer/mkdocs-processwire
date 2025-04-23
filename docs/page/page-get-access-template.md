Returns the template from which role/access settings are inherited from
-----------------------------------------------------------------------

### Usage

    // basic usage
    $template = $page->getAccessTemplate();
    
    // usage with all arguments
    $template = $page->getAccessTemplate(string $type = 'view');

### Arguments

Name

Type(s)

Description

`type` (optional)

string

Optionally specify one of 'view', 'edit', 'add', or 'create' (default='view')

### Return value

[`Template`](/api/ref/template/) `null`

Returns Template object or NULL if none

