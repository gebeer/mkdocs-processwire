Get a session variable or return $val argument if session value not present
---------------------------------------------------------------------------

This is the same as get() except that it lets you specify a fallback return value in the method call. For a namespace version use `Session::getValFor()` instead.

Available since version **3.0.133**.

### Usage

    // basic usage
    $mixed = $session->getVal(string $key);
    
    // usage with all arguments
    $mixed = $session->getVal(string $key, mixed $val = null);

### Arguments

Name

Type(s)

Description

`key`

string

Name of session variable to retrieve.

`val` (optional)

mixed

Fallback value to return if session does not have it.

### Return value

`mixed`

Returns value of seession variable, or NULL if not found.

