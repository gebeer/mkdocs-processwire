Get a CSRF Token name and value
-------------------------------

### Usage

    // basic usage
    $array = $sessionCSRF->getToken();
    
    // usage with all arguments
    $array = $sessionCSRF->getToken($id = '');

### Arguments

Name

Type(s)

Description

`id` (optional)

int, string, null

Optional unique ID for this token

### Return value

`array`

("name" => "token name", "value" => "token value", "time" => created timestamp)

