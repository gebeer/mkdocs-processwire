Returns true if the method or property is hooked, false if it isn’t.
--------------------------------------------------------------------

*   This method checks for both static hooks and local hooks.
*   Accepts a `method()` or `property` name as an argument.
*   Class context is assumed to be the current class this method is called on.
*   Also considers the class parents for hooks.

### Example

    if($pages->hasHook('find()')) {
      // the Pages::find() method is hooked
    }

### Usage

    $bool = $wire->hasHook(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Method() name or property name:

*   If checking for a hooked method, it should be in the form `method()`.
*   If checking for a hooked property, it should be in the form `property`.

### Return value

`bool`

True if this class instance has the hook, false if not.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - When you try to call it with a Class::something() type method, which is not supported.
    

