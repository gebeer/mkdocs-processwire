Adds a new page with the given $name and returns it
---------------------------------------------------

*   If the page has any other fields, they will not be populated, only the name will.
*   Returns a [`NullPage`](/api/ref/null-page/) on error, such as when a page of this type already exists with the same name/parent.

Hook note: If you want to hook this method, please hook the `addReady`, `Pages::add`, or `Pages::addReady` method instead, as hooking this method will not hook relevant pages added directly through $pages->add().

### Usage

    $page = $pagesType->add(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Name to use for the new page

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

