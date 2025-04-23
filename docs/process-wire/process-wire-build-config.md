Static method to build a Config object for booting ProcessWire
--------------------------------------------------------------

### Usage

    // basic usage
    $config = $wire::buildConfig();
    
    // usage with all arguments
    $config = $wire::buildConfig(string $rootPath = '', string $rootURL = null, array $options = []);

### Arguments

Name

Type(s)

Description

`rootPath` (optional)

string

Path to root of installation where ProcessWire's index.php file is located.

`rootURL` (optional)

string

Should be specified only for secondary ProcessWire instances. May also include scheme & hostname, i.e. "[http://hostname.com/url](http://hostname.com/url)" to force use of scheme+host.

`options` (optional)

array

Options to modify default behaviors (experimental):

*   `siteDir` (string): Name of "site" directory in $rootPath that contains site's config.php, no slashes (default="site").

### Return value

[`Config`](/api/ref/config/)

