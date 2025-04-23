Current unsanitized request URL
-------------------------------

*   This is an alternative to [`$input->url()`](/api/ref/input/url/) that’s available prior to API ready state.
*   Useful if you need to know request URL from /site/config.php or other boot file.
*   Returned value does not include query string, if present.
*   Returned value includes installation subdirectory, if present.

Available since version **3.0.175**.

### Example

    if($config->requestUrl() === '/products/2021/') {
      // current request URL is exactly “/products/2021/”
    }
    if($config->requestUrl('/products/2021/')) {
      // current request matches “/products/2021/” somewhere in URL
    }
    if($config->requestUrl([ 'foo', 'bar', 'baz' ])) {
      // current request has one or more of 'foo', 'bar', 'baz' in the URL
    }

### Usage

    // basic usage
    $string = $config->requestUrl();
    
    // usage with all arguments
    $string = $config->requestUrl($match = '', string $get = '');

### Arguments

Name

Type(s)

Description

`match` (optional)

string, array

Optionally return URL only if some part matches given string(s) (default='')

`get` (optional)

string

Specify 'path' to get and/or match path, 'query' to get and/or match query string, or omit for URL (default='')

### Return value

`string`

Returns URL string or blank string if $match argument used and doesn’t match.

