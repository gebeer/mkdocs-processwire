Retrieve a named COOKIE variable value or all COOKIE variables
--------------------------------------------------------------

Please see the [cookie API reference page](https://processwire.com/api/ref/wire-input-data-cookie/) for additional documentation on how to get and set cookies and cookie options.

Cookies are a form of user input, so always sanitize (and validate where appropriate) any values.

The following optional features are available in ProcessWire version 3.0.125 and newer:

*   Provide a sanitization method as the 2nd argument to include sanitization.
*   Provide an array of valid values as the 2nd argument to limit input to those values.
*   Provide a callback function that receives the value and returns a validated value.
*   Provide a fallback value as the 3rd argument to use if value not present or invalid.
*   Append “\[\]” to the 1st argument to always force return value to be an array, i.e “colors\[\]”.

Note that the `$valid` and `$fallback` arguments are only applicable if a `$key` argument is provided. See the `WireInput::get()` method for usage examples (get method works the same as cookie method).

### Example

    // setting cookies
    $input->cookie->foo = 'bar'; // set with default options (expires with session)
    $input->cookie->set('foo', 'bar'); // same as above
    $input->cookie->set('foo', 'bar', 86400); // expire after 86400 seconds (1 day)
    $input->cookie->set('foo', 'bar', [ 'age' => 86400, 'path' => $page->url ]);
    
    // getting cookies
    $val = $input->cookie->foo;
    $val = $input->cookie->get('foo'); // same as above
    $val = $input->cookie->text('foo'); // get and use text sanitizer
    
    // removing cookies
    $input->cookie->remove('foo');
    
    // getting cookie options
    $array = $input->cookie->options();
    print_r($array); // see all options
    
    // setting cookie options (to use in next $input->cookie->set call)
    $input->cookie->options('age', 86400); // set default age to 1 day
    $input->cookie->options([ // set multiple options
      'age' => 86400,
      'path' => $page->url,
      'domain' => 'www.domain.com',
    ]);
    
    // setting default options (in /site/config.php):
    $config->cookieOptions = [
      'age' => 604800, // 1 week
      'httponly' => true, // make visible to PHP but not JS
       // and so on
    ]; 

### Usage

    // basic usage
    $mixed = $input->cookie();
    
    // usage with all arguments
    $mixed = $input->cookie(string $key = '', $valid = null, $fallback = null);

### Arguments

Name

Type(s)

Description

`key` (optional)

string

Name of the COOKIE variable you want to retrieve.

*   If populated, returns the value corresponding to the key or NULL if it doesn't exist.
*   If blank, returns reference to the WireDataInput containing all COOKIE vars.

`valid` (optional)

array, string, int, callable, null

Omit for no validation/sanitization, or provide one of the following:

*   String name of Sanitizer method to to sanitize value with before returning it.
*   CSV string of multiple sanitizer names to process the value, in order.
*   Array of allowed values (aka whitelist), where input value must be one of these, otherwise null (or fallback value) will returned. Values in the array may be any string or integer.
*   Callback function to sanitize and validate the value.
*   Integer if a specific number is the only allowed value other than fallback value (i.e. like a checkbox toggle).

`fallback` (optional)

### Return value

`null` `mixed` `WireInputData`

Returns one of the following:

*   If given no `$key` argument, returns `WireInputData` with all unsanitized COOKIE vars.
*   If given no `$valid` argument, returns unsanitized value or NULL if not present.
*   If given a Sanitizer name for `$valid` argument, returns value sanitized with that Sanitizer method (3.0.125+).
*   If given an array of allowed values for `$valid` argument, returns value from that array if it was in the input, or null if not (3.0.125+).
*   If given a callable function for `$valid` argument, returns the value returned by that function (3.0.125+).
*   If given a `$fallback` argument, returns that value when it would otherwise return null (3.0.125+).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given unknown Sanitizer method for $valid argument
    

