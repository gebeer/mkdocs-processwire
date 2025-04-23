Hookable method that is called whenever a property has changed while change tracking is enabled.
------------------------------------------------------------------------------------------------

*   Enables hooks to monitor changes to the object.
*   Do not call this method directly, as the [`Wire::trackChange()`](/api/ref/wire/track-change/) method already does so.
*   Descending classes should call `$this->trackChange('name', $oldValue, $newValue);` when a property they are tracking has changed.

### Usage

    // basic usage
    $wire->changed(string $what);
    
    // usage with all arguments
    $wire->changed(string $what, mixed $old = null, mixed $new = null);

### Arguments

Name

Type(s)

Description

`what`

string

Name of property that changed

`old` (optional)

mixed

Previous value before change

`new` (optional)

mixed

New value

