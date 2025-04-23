Retrieve a named GET variable value, or all GET variables (from URL query string)
---------------------------------------------------------------------------------

Always sanitize (and validate where appropriate) any values from user input.

The following optional features are available in ProcessWire version 3.0.125 and newer:

*   Provide a sanitization method as the 2nd argument to include sanitization.
*   Provide an array of valid values as the 2nd argument to limit input to those values.
*   Provide a callback function that receives the value and returns a validated value.
*   Provide a fallback value as the 3rd argument to use if value not present or invalid.
*   Append “\[\]” to the 1st argument to always force return value to be an array, i.e “colors\[\]”.

Note that the `$valid` and `$fallback` arguments are only applicable if a `$key` argument is provided.

### Example

    // Retrieve a "q" GET variable, sanitize and output
    // Example request URL: domain.com/path/to/page/?q=TEST
    $q = $input->get('q'); // retrieve value
    $q = $sanitizer->text($q); // sanitize input as 1-line text
    echo $sanitizer->entities($q); // sanitize for output, outputs "TEST"
    
    // You can also combine $input and one $sanitizer call, replacing
    // the "text" method call with any $sanitizer method:
    $q = $input->get->text('q');
    
    // like the previous example, but specify sanitizer method as second argument (3.0.125+):
    $q = $input->get('q', 'text');
    
    // if you want more than one sanitizer, specify multiple in a CSV string (3.0.125+):
    $q = $input->get('q', 'text,entities');
    
    // you can provide a whitelist array of allowed values instead of a sanitizer method (3.0.125+):
    $color = $input->get('color', [ 'red', 'blue', 'green' ]);
    
    // an optional 3rd argument lets you specify a fallback value to use if valid value not present or
    // empty in input, and it will return this value rather than null/empty (3.0.125+):
    $qty = $input->get('qty', 'int', 1); // return 1 if no qty provided
    $color = $input->get('color', [ 'red', 'blue', 'green' ], 'red'); // return red if no color selected
    
    // you may optionally provide a callback function to sanitize/validate with (3.0.125+):
    $isActive = $input->get('active', function($val) { return $val ? true : false; }); 

### Usage

    // basic usage
    $mixed = $input->get();
    
    // usage with all arguments
    $mixed = $input->get(string $key = '', $valid = null, $fallback = null);

### Arguments

Name

Type(s)

Description

`key` (optional)

string

Name of GET variable you want to retrieve.

*   If populated, returns the value corresponding to the key or NULL if it doesn’t exist.
*   If blank, returns reference to the WireDataInput containing all GET vars.

`valid` (optional)

array, string, int, callable, null

Omit for no validation/sanitization, or provide one of the following (3.0.125+ only):

*   String name of Sanitizer method to to sanitize value with before returning it.
*   CSV string of multiple sanitizer names to process the value, in order.
*   Array of allowed values (aka whitelist), where input value must be one of these, otherwise null (or fallback value) will returned. Values in the array may be any string or integer.
*   Callback function to sanitize and validate the value.
*   Integer if a specific number is the only allowed value other than fallback value (i.e. like a checkbox toggle).

`fallback` (optional)

### Return value

`null` `mixed` `WireInputData`

Returns one of the following:

*   If given no `$key` argument, returns `WireInputData` with all unsanitized GET vars.
*   If given no `$valid` argument, returns unsanitized value or NULL if not present.
*   If given a Sanitizer name for `$valid` argument, returns value sanitized with that Sanitizer method (3.0.125+).
*   If given an array of allowed values for `$valid` argument, returns value from that array if it was in the input, or null if not (3.0.125+).
*   If given a callable function for `$valid` argument, returns the value returned by that function (3.0.125+).
*   If given a `$fallback` argument, returns that value when it would otherwise return null (3.0.125+).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given unknown Sanitizer method for $valid argument
    

