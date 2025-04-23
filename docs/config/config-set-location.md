Given a directory to a named location, updates $config->paths and $config->urls for it
--------------------------------------------------------------------------------------

*   Paths relative to PW installation root should omit the leading slash, i.e. use `site/templates/` and NOT `/site/templates/`.
    
*   If specifying just the `$dir` argument, it updates both [`$config->paths`](/api/ref/config/paths/) and [`$config->urls`](/api/ref/config/urls/) for it.
    
*   If specifying both `$dir` and `$url` arguments, then `$dir` refers to [`$config->paths`](/api/ref/config/paths/) and `$url` refers to [`$config->urls`](/api/ref/config/urls/).
    
*   The `$for` argument can be: `cache`, `logs`, `files`, `tmp`, `templates`, or one of your own. Other named locations may also work, but since they can potentially be used before PW’s “ready” state, they may not be reliable.
    
*   **Warning:** anything that changes a system URL may make the URL no longer have the protection of the root .htaccess file. As a result, if you modify system URLs for anything on a live server, you should also update your .htaccess file to reflect your changes (while leaving existing rules for original URL in place).
    

The following example would be in /site/init.php or /site/ready.php (or equivalent module method). In this example we are changing the location (path and URL) of our /site/templates/ to use a new version of the files in /site/dev-templates/ so that we can test them out with user 'karen', while all other users on the site get our regular templates.

Available since version **3.0.141**.

### Example

    // change templates path and URL to /site/dev-templates/ when user name is 'karen'
    if($user->name == 'karen') {
      $config->setLocation('templates', 'site/dev-templates/');
    }

### Usage

    // basic usage
    $self = $config->setLocation(string $for, string $dir);
    
    // usage with all arguments
    $self = $config->setLocation(string $for, string $dir, $url = '');

### Arguments

Name

Type(s)

Description

`for`

string

Named location from [`$config->paths`](/api/ref/config/paths/) or [`$config->urls`](/api/ref/config/urls/), one of: `cache`, `logs`, `files`, `tmp`, `templates`, or your own.

`dir`

string

Directory or URL to the location. Should be either a path or URL relative to current installation root (recommended), or an absolute disk path that resolves somewhere in current installation root. If specifying an absolute path outside of the installation root, then you’ll also want to provide the $url argument since PW won’t know it. You may also specify a blank string for this argument if you only want to set the $url argument.

`url` (optional)

string, bool

If the $dir argument represents both the path and URL relative to site root, you can omit this argument. If path and URL cannot be derived from one another, or you only want to modify the $url (leaving $dir blank), you can specify the URL in this argument. Specify boolean false if you only want to set the $dir (path) and not detect the $url from it.

### Return value

`self`

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If request cannot be accommodated
    

