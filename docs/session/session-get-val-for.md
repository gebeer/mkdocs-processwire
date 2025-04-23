Get a session variable or return $val argument if session value not present
---------------------------------------------------------------------------

This is the same as get() except that it lets you specify a fallback return value in the method call. For a namespace version use `Session::getValFor()` instead.

Available since version **3.0.133**.

### Usage

    // basic usage
    $mixed = $session->getValFor($ns, string $key);
    
    // usage with all arguments
    $mixed = $session->getValFor($ns, string $key, mixed $val = null);

### Arguments

Name

Type(s)

Description

`ns`

string, object

Namespace string or object

`key`

string

Specify variable name to retrieve

`val` (optional)

mixed

Fallback value if session does not have one

### Return value

`mixed`

