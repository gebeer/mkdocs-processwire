Add a new Pageimage item, or create one from given filename and add it.
-----------------------------------------------------------------------

If give a filename (string) it will create the new [`Pagefile`](/api/ref/pagefile/) item from it and add it.

### Example

    $items->add($item); 

### Usage

    $pageimages = $pageimages->add($item);

### Arguments

Name

Type(s)

Description

`item`

Pageimage, string

If item is a string (filename) then the Pageimage instance will be created automatically.

### Return value

[`Pageimages`](/api/ref/pageimages/) [`Pagefiles`](/api/ref/pagefiles/)

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If given an item that can't be stored by this WireArray.
    

### See Also

*   [WireArray::prepend()](/api/ref/wire-array/prepend/)
*   [WireArray::append()](/api/ref/wire-array/append/)

