Does this user have the given Role?
-----------------------------------

### Example

    if($user->hasRole('editor')) {
      // user has the editor role
    }

### Usage

    $bool = $user->hasRole($role);

### Arguments

Name

Type(s)

Description

`role`

string, Role, int

May be Role name, object or ID.

### Return value

`bool`

