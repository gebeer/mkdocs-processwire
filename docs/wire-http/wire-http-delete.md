Send a DELETE request to a URL
------------------------------

“The HTTP DELETE request method deletes the specified resource.” [More about DELETE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE)

Available since version **3.0.222**.

### Usage

    // basic usage
    $bool = $http->delete(string $url);
    
    // usage with all arguments
    $bool = $http->delete(string $url, $data = [], array $options = []);

### Arguments

Name

Type(s)

Description

`url`

string

URL to send to (including http:// or https://)

`data` (optional)

array, string

Optional associative array of data to send (if not already set before), or raw data to send (such as JSON string)

`options` (optional)

array

Optional options to modify default behavior, see the send() method for details.

### Return value

`bool` `string`

False on failure or string of contents received on success.

