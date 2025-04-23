Return the index/position of this page relative to siblings.
------------------------------------------------------------

If given a hidden or unpublished page, that page would not usually be part of the group of siblings. As a result, such pages will return what the value would be if they were visible (as of 3.0.121). This may overlap with the index of other pages, since indexes are relative to visible pages, unless you specify an include mode (see next paragraph).

If you want this method to include hidden/unpublished pages as part of the index numbers, then specify boolean true for the $selector argument (which implies "include=all") OR specify a selector of "include=hidden", "include=unpublished" or "include=all".

Available since version **3.0.24**.

### Example

    $i = $page->index();
    $n = $page->parent->numChildren();
    echo "This page is $i out of $n total pages";

### Usage

    // basic usage
    $int = $page->index();
    
    // usage with all arguments
    $int = $page->index($selector = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

### Return value

`int`

Returns index number (zero-based)

