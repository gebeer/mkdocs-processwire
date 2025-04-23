Take the current item and append the given item(s), returning a new WireArray
-----------------------------------------------------------------------------

This is for syntactic convenience in fluent interfaces.

### Example

    if($page->and($page->parents)->has("featured=1")) { 
       // page or one of its parents has a featured property with value of 1
    }

### Usage

    // basic usage
    $items = $wireData->and();
    
    // usage with all arguments
    $items = $wireData->and($items = null);

### Arguments

Name

Type(s)

Description

`items` (optional)

WireArray, WireData, string, null

May be any of the following:

*   [`WireData`](/api/ref/wire-data/) object (or derivative)
*   [`WireArray`](/api/ref/wire-array/) object (or derivative)
*   Name of any property from this object that returns one of the above.
*   Omit argument to simply return this object in a WireArray

### Return value

[`WireArray`](/api/ref/wire-array/)

Returns a WireArray of this object _and_ the one(s) given.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If invalid argument supplied.
    

