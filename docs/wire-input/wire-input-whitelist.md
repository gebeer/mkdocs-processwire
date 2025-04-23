Get or set a whitelist variable
-------------------------------

Whitelist variables are used by modules and templates and assumed to be sanitized. Only place variables in the whitelist that you have already sanitized.

The whitelist is a list of variables specifically set by the application as sanitized for use elsewhere in the application. This whitelist is not specifically used by ProcessWire unless you populate it from your templates or the API. When populated, it is used by the MarkupPagerNav module (for instance) to ensure that sanitized query string (GET) variables are maintained across paginations.

### Examples

    // Retrieve a GET variable, sanitize/validate it, and populate to whitelist
    $limit = (int) $input->get('limit');
    if($limit < 10 || $limit > 100) $limit = 25; // validate
    $input->whitelist('limit', $limit); 

    // Retrieve a variable from the whitelist
    $limit = $input->whitelist('limit'); 

### Usage

    // basic usage
    $mixed = $input->whitelist();
    
    // usage with all arguments
    $mixed = $input->whitelist(string $key = '', mixed $value = null);

### Arguments

Name

Type(s)

Description

`key` (optional)

string

Whitelist variable name that you want to get or set.

*   If $key is blank, it assumes you are asking to return the entire whitelist.
*   If $key and $value are populated, it adds the value to the whitelist.
*   If $key is an array, it adds all the values present in the array to the whitelist.
*   If $value is omitted, it assumes you are asking for a value with $key, in which case it returns it.

`value` (optional)

mixed

Value you want to set (if setting a value). See explanation for the $key param.

### Return value

`null` `mixed` `WireInputData`

Returns whitelist variable value if getting a value (null if it doesn't exist).

