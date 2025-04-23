Add a hook to be executed before the hooked method
--------------------------------------------------

*   Use a "before" hook when you have code that should execute before a hookable method executes.
*   One benefit of using a "before" hook is that you can have it modify the arguments that are sent to the hookable method.
*   This type of hook can also completely replace a hookable method if hook populates an `$event->replace` property. See the HookEvent class for details.

### Example

    // Attach hook to a method in current object
    $this->addHookBefore('Page::path', $this, 'yourHookMethodName');
    
    // Attach hook to an inline function
    $this->addHookBefore('Page::path', function($event) { ... });
    
    // Attach hook to a procedural function
    $this->addHookBefore('Page::path', 'your_function_name');
    
    // Attach hook from single object instance ($page) to inline function
    $page->addHookBefore('path', function($event) { ... }); 

### Usage

    // basic usage
    $string = $wire->addHookBefore($method, $toObject);
    
    // usage with all arguments
    $string = $wire->addHookBefore($method, $toObject, $toMethod = null, array $options = []);

### Arguments

Name

Type(s)

Description

`method`

string, array

Method to hook in one of the following formats (please omit 3 leading underscores):

*   `Class::method` - If hooking to _all_ object instances of the class.
*   `method` - If hooking to a single object instance.
*   Since 3.0.137 it may also be multiple methods to hook in CSV string or array.

`toObject`

object, null, callable

Specify one of the following:

*   Object instance to call `$toMethod` from (like `$this`).
*   Inline function (closure) if providing implemention inline.
*   Procedural function name, if hook is implemented by a procedural function.
*   Null if you want to use the 3rd argument and don't need this argument.

`toMethod` (optional)

string, array

Method from $toObject, or function name to call on a hook event. This argument can be sustituted as the 2nd argument when the 2nd argument isn’t needed, or it can be the $options argument.

`options` (optional)

array

Array of options that can modify behavior:

*   `type` (string): May be either 'method' or 'property'. If property, then it will respond to $obj->property rather than $obj->method(). The default type is 'method'.
*   `priority` (int): A number determining the priority of a hook, where lower numbers are executed before higher numbers. The default priority is 100.

### Return value

`string`

A special Hook ID (or CSV string of hook IDs) that should be retained if you need to remove the hook later.

