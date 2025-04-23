Add a new Role with the given name and return it
------------------------------------------------

*   If the page has any other fields, they will not be populated, only the name will.
*   Returns a [`NullPage`](/api/ref/null-page/) on error, such as when a page of this type already exists with the same name/parent.

Hook note: If you want to hook this method, please hook the `addReady`, `Pages::add`, or `Pages::addReady` method instead, as hooking this method will not hook relevant pages added directly through $pages->add().

### Usage

    $role = $roles->add(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Name of role you want to add, i.e. "hello-world"

### Return value

[`Role`](/api/ref/role/) [`NullPage`](/api/ref/null-page/)

Returns a Role page on success, or a NullPage on error

