Does the system have a permission with the given name?
------------------------------------------------------

### Example

    // Check if page-publish permission is available
    if($permissions->has('page-publish')) {
      // system has the page-publish permission installed
    }

### Usage

    $bool = $permissions->has(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Name of permission

### Return value

`bool`

True if system has a permission with this name, or false if not.

