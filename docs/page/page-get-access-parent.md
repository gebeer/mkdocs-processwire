Returns the page from which role/access settings are inherited from
-------------------------------------------------------------------

### Usage

    // basic usage
    $page = $page->getAccessParent();
    
    // usage with all arguments
    $page = $page->getAccessParent(string $type = 'view');

### Arguments

Name

Type(s)

Description

`type` (optional)

string

Optionally specify one of 'view', 'edit', 'add', or 'create' (default='view')

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

Returns NullPage if none found

