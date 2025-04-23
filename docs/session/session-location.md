Perform a temporary redirect
----------------------------

This is an alias of [`$session->redirect($url, false);`](/api/ref/session/redirect/) that sends only the location header, which translates to a 302 redirect.

Available since version **3.0.166**.

### Usage

    // basic usage
    $session->location(string $url);
    
    // usage with all arguments
    $session->location(string $url, int $status = 302);

### Arguments

Name

Type(s)

Description

`url`

string

`status` (optional)

int

One of the following HTTP status codes, or omit for 302 (added 3.0.192):

*   `302` (int): “Found”, Temporary redirect using GET. (default)
*   `303` (int): “See other”, Temporary redirect using GET.
*   `307` (int): Temporary redirect using current request method such as POST (repeat that request).

### See Also

*   [Session::redirect()](/api/ref/session/redirect/)

