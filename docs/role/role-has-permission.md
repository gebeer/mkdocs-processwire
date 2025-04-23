Does this role have the given permission name, id or object?
------------------------------------------------------------

### Usage

    // basic usage
    $bool = $role->hasPermission($permission);
    
    // usage with all arguments
    $bool = $role->hasPermission($permission, $context = null);

### Arguments

Name

Type(s)

Description

`permission`

string, int, Permission

Permission object, name, or id.

`context` (optional)

Page, Template, null

Optional Page or Template context.

### Return value

`bool`

### See Also

*   [User::hasPermission()](/api/ref/user/has-permission/)

