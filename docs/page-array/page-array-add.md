Add one or more Page objects to this PageArray.
-----------------------------------------------

Please see the [`WireArray::add()`](/api/ref/wire-array/add/) method for more details.

### Example

    // Add one page
    $pageArray->add($page);
    
    // Add multiple pages
    $pageArray->add($pages->find("template=basic-page"));
    
    // Add page by ID
    $pageArray->add(1005); 

### Usage

    $pageArray->add($item);

### Arguments

Name

Type(s)

Description

`item`

Page, PageArray, int

Page object, PageArray object, or Page ID.

*   If given a [`Page`](/api/ref/page/), the Page will be added.
*   If given a [`PageArray`](/api/ref/page-array/), it will do the same thing as the [`WireArray::import()`](/api/ref/wire-array/import/) method and append all the pages.
*   If Page `ID`, the Page identified by that ID will be loaded and added to the PageArray.

### Return value

`$this`

Object instance it was called from (method supports fluent interface).

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - If given an item that can't be stored by this WireArray.
    

### See Also

*   [WireArray::prepend()](/api/ref/wire-array/prepend/)
*   [WireArray::append()](/api/ref/wire-array/append/)

