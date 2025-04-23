Add the given Permission string, id or object.
----------------------------------------------

This is the same as `$role->permissions->add($permission)` except this one will accept ID or name.

### Usage

    $bool = $role->addPermission($permission);

### Arguments

Name

Type(s)

Description

`permission`

string, int, Permission

Permission object, name or id.

### Return value

`bool`

Returns false if permission not recognized, true otherwise

