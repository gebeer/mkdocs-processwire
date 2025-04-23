Get a session variable
----------------------

*   This method returns the value of the requested session variable, or NULL if it's not present.
*   You can optionally use a namespace with this method, to avoid collisions with other session variables. But if using namespaces we recommended using the dedicated getFor() and setFor() methods instead.
*   You can also get or set non-namespaced session values directly (see examples).

### Examples

    // Set value "Bob" to session variable named "firstName"
    $session->set('firstName', 'Bob');
    
    // You can retrieve the firstName now, or any later request
    $firstName = $session->get('firstName');
    
    // outputs: Hello Bob
    echo "Hello $firstName"; 

    // Setting and getting a session value directly
    $session->firstName = 'Bob';
    $firstName = $session->firstName;

### Usage

    // basic usage
    $mixed = $session->get($key);
    
    // usage with all arguments
    $mixed = $session->get($key, string $_key = null);

### Arguments

Name

Type(s)

Description

`key`

string, object

Name of session variable to retrieve (or object if using namespaces)

`_key` (optional)

string

Name of session variable to get if first argument is namespace, omit otherwise.

### Return value

`mixed`

Returns value of seession variable, or NULL if not found.

