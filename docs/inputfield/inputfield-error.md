Record an error for this Inputfield
-----------------------------------

The error message will be placed in the context of this Inputfield. See the [`Wire::error()`](/api/ref/wire/error/) method for full details on arguments and options.

### Example

    $this->error("This is the notice text"); 
    $this->error("This notice is also logged", true);
    $this->error("This notice is only shown in debug mode", Notice::debug);
    $this->error("This notice allows <em>markup</em>", Notice::allowMarkup);
    $this->error("Notice using multiple flags", Notice::debug | Notice::logOnly);

### Usage

    // basic usage
    $inputfield->error(string $text);
    
    // usage with all arguments
    $inputfield->error(string $text, int $flags = 0);

### Arguments

Name

Type(s)

Description

`text`

string

Text of error message

`flags` (optional)

int

Optional flags

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### See Also

*   [Wire::errors()](/api/ref/wire/errors/)
*   [Wire::message()](/api/ref/wire/message/)
*   [Wire::warning()](/api/ref/wire/warning/)

