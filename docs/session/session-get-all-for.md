Get all session variables for given namespace and return associative array
--------------------------------------------------------------------------

Available since version **3.0.141**. _Method added for consistency, but any version can do this with $session->getFor($ns, '');_

### Usage

    $array = $session->getAllFor($ns);

### Arguments

Name

Type(s)

Description

`ns`

string, Wire

### Return value

`array`

