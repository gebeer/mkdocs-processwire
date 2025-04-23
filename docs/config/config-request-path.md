Current unsanitized request path (URL sans ProcessWire installation subdirectory, if present)
---------------------------------------------------------------------------------------------

This excludes any subdirectories leading to ProcessWire installation root, if present. Useful if you need to know request path from /site/config.php or other boot file.

Available since version **3.0.175**.

### Example

    if(strpos($config->requestPath(), '/processwire/') === 0) {
      // current request path starts with “/processwire/”
    }
    if($config->requestPath('/processwire/')) {
      // the text “/processwire/” appears somewhere in current request path
    }
    if($config->requestPath([ 'foo', 'bar', 'baz' ])) {
      // current request has one or more of 'foo', 'bar', 'baz' in the path
    }

### Usage

    // basic usage
    $string = $config->requestPath();
    
    // usage with all arguments
    $string = $config->requestPath($match = '');

### Arguments

Name

Type(s)

Description

`match` (optional)

string, array

Optionally return path only if some part matches given string(s) (default='')

### Return value

`string`

Returns path string or blank string if $match argument used and doesn’t match.

