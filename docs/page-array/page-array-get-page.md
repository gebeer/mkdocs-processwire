Like the base get() method but can only return Page objects (whether Page or NullPage)
--------------------------------------------------------------------------------------

Available since version **3.0.162**.

### Usage

    $page = $pageArray->getPage($key);

### Arguments

Name

Type(s)

Description

`key`

int, string, array

Provide any of the following:

*   Key of Page to retrieve.
*   A selector string or selector array, to return the first item that matches the selector.
*   A string containing the "name" property of any Page, and the matching Page will be returned.

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

### See Also

*   [WireArray::get()](/api/ref/wire-array/get/)

