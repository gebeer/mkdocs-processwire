Redirect this session to another URL.
-------------------------------------

Execution halts within this function after redirect has been issued.

### Example

    // redirect to homepage
    $session->redirect('/'); 

### Usage

    // basic usage
    $session->redirect(string $url);
    
    // usage with all arguments
    $session->redirect(string $url, $status = 301);

### Arguments

Name

Type(s)

Description

`url`

string

URL to redirect to

`status` (optional)

bool, int

One of the following (or omit for 301):

*   `true` (bool): Permanent redirect (same as 301).
*   `false` (bool): Temporary redirect (same as 302).
*   `301` (int): Permanent redirect using GET. (3.0.166+)
*   `302` (int): “Found”, Temporary redirect using GET. (3.0.166+)
*   `303` (int): “See other”, Temporary redirect using GET. (3.0.166+)
*   `307` (int): Temporary redirect using current request method such as POST (repeat that request). (3.0.166+)

