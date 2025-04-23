Delete this page from the database
----------------------------------

This is the same as calling `$pages->delete($page)`.

### Examples

    // Delete pages named "delete-me" that don't have children
    $items = $pages->find("name=delete-me, numChildren=0");
    foreach($items as $item) {
      $item->delete();
    }

    // Delete a page and recursively all of its children, grandchildren, etc. 
    $item = $pages->get('/some-page/');
    $item->delete(true);

### Usage

    // basic usage
    $bool = $page->delete();
    
    // usage with all arguments
    $bool = $page->delete(bool $recursive = false);

### Arguments

Name

Type(s)

Description

`recursive` (optional)

bool

If set to true, then this will attempt to delete all children too.

### Return value

`bool` `int`

True on success, false on failure, or int quantity of pages deleted when recursive option is true.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - when attempting to delete a page with children and $recursive option is not specified.
    

### See Also

*   [Pages::delete()](/api/ref/pages/delete/)

