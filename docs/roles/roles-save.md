Save a Role
-----------

*   This is the same as calling $page->save()
*   If the page is new, it will be inserted. If existing, it will be updated.
*   If you want to just save a particular field in a Page, use `$page->save($fieldName)` instead.

Hook note:  
If you want to hook this method, please hook the `saveReady`, `saved`, or one of the `Pages::save*` methods instead, as hooking this method will not hook relevant pages saved directly through $pages->save().

### Usage

    $bool = $roles->save($page);

### Arguments

Name

Type(s)

Description

`page`

Role, Page

### Return value

`bool`

True on success, false on failure

### Exceptions

Method can throw exceptions on error:

*   **`WireException`**
    

