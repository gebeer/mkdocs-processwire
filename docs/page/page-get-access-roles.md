Return Roles (PageArray) that have access to this page
------------------------------------------------------

This is determined from the page's template. If the page's template has roles turned off, then it will go down the tree till it finds usable roles to use and inherit from.

### Usage

    // basic usage
    $items = $page->getAccessRoles();
    
    // usage with all arguments
    $items = $page->getAccessRoles(string $type = 'view');

### Arguments

Name

Type(s)

Description

`type` (optional)

string

May be 'view', 'edit', 'create' or 'add' (default='view')

### Return value

[`PageArray`](/api/ref/page-array/)

of Role objects

