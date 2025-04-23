Duplicate the Pagefile and add to this Pagefiles instance
---------------------------------------------------------

After duplicating a file, you must follow up with a save of the page containing it. Otherwise the file is marked for deletion.

### Usage

    // basic usage
    $pagefile = $pagefiles->clone(Pagefile $item);
    
    // usage with all arguments
    $pagefile = $pagefiles->clone(Pagefile $item, array $options = []);

### Arguments

Name

Type(s)

Description

`item`

Pagefile

Pagefile item to duplicate

`options` (optional)

array

Options to modify default behavior:

*   `action` (string): Specify "append", "prepend", "after", "before" or blank to only return Pagefile. (default="after")
*   `pagefiles` (Pagefiles): Pagefiles instance file should be duplicated to. (default=$this)

### Return value

[`Pagefile`](/api/ref/pagefile/) `bool`

Returns new Pagefile or boolean false on fail

