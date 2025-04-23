Get a CSRF Token name and value that can only be used once
----------------------------------------------------------

Note that a single call to hasValidToken($id) or validate($id) will invalidate the single use token. So call them once and store your result if you need the result multiple times.

### Usage

    // basic usage
    $array = $sessionCSRF->getSingleUseToken();
    
    // usage with all arguments
    $array = $sessionCSRF->getSingleUseToken($id = '');

### Arguments

Name

Type(s)

Description

`id` (optional)

int, string

Optional unique ID/name for this token (of omitted one is generated automatically)

### Return value

`array`

("id' => "token ID", "name" => "token name", "value" => "token value", "time" => created timestamp)

