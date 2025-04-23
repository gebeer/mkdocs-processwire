Move this page to the trash
---------------------------

This is the same as calling `$pages->trash($page)`.

### Example

    // Trash a page
    $item = $pages->get('/some-page/');
    $item->trash();

### Usage

    $bool = $page->trash();

### Return value

`bool`

True on success, false on failure

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

