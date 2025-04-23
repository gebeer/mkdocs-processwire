Returns whether this page has the given access role
---------------------------------------------------

Given access role may be a role name, role ID or Role object.

### Usage

    // basic usage
    $bool = $page->hasAccessRole($role);
    
    // usage with all arguments
    $bool = $page->hasAccessRole($role, string $type = 'view');

### Arguments

Name

Type(s)

Description

`role`

string, int, Role

`type` (optional)

string

May be 'view', 'edit', 'create' or 'add' (default is 'view')

### Return value

`bool`

