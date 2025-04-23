Return the field name by which children are sorted
--------------------------------------------------

*   If sort is descending, then field name is prepended with a "-".
*   Returns the value "sort" if pages are unsorted or sorted manually.
*   Note the return value from this method may be different from the [`Page::sortfield`](/api/ref/page/sortfield/) (lowercase) property, as this method considers the sort field specified with the template as well.

### Usage

    $string = $page->sortfield();

### Return value

`string`

