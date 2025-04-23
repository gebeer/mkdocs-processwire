Does the user have the given permission?
----------------------------------------

*   Optionally accepts a [`Page`](/api/ref/page/) or [`Template`](/api/ref/template/) context for the permission.
*   This method accounts for the user's permissions across all their roles.

### Example

    if($user->hasPermission('page-publish')) {
      // user has the page-publish permission in one of their roles
    }
    if($user->hasPermission('page-publish', $page)) {
      // user has page-publish permission for $page
    }

### Usage

    // basic usage
    $bool = $user->hasPermission($name);
    
    // usage with all arguments
    $bool = $user->hasPermission($name, $context = null);

### Arguments

Name

Type(s)

Description

`name`

string, Permission

Permission name, object or id.

`context` (optional)

Page, Template, bool, string

Page or Template...

*   or specify boolean true to return if user has permission OR if it was added at any template
*   or specify string "templates" to return array of Template objects where user has permission

### Return value

`bool` `array`

