Add Role to this user
---------------------

This is the same as `$user->roles->add($role)` except this one will also accept ID or name.

### Example

    // Add the "editor" role to the $user
    $user->addRole('editor');
    $user->save();

### Usage

    $bool = $user->addRole($role);

### Arguments

Name

Type(s)

Description

`role`

string, int, Role

May be Role name, object, or ID.

### Return value

`bool`

Returns false if role not recognized, true otherwise

