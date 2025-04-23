Return this page’s parent pages, or the parent pages matching the given selector.
---------------------------------------------------------------------------------

This method returns all parents of this page, in order. If a selector is specified, they will be filtered by the selector. By default, parents are returned in breadcrumb order. In 3.0.158+ if you specify boolean true for selector argument, then it will return parents in reverse order (closest to furthest).

### Examples

    // Render breadcrumbs 
    foreach($page->parents() as $parent) {
      echo "<li><a href='$parent->url'>$parent->title</a></li>";
    }

    // Return all parents, excluding the homepage
    $parents = $page->parents("template!=home"); 

    // Return parents in reverse order (closest to furthest, 3.0.158+)
    $parents = $page->parents(true); 

### Usage

    // basic usage
    $items = $page->parents();
    
    // usage with all arguments
    $items = $page->parents($selector = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array, bool

Optional selector string to filter parents by or boolean true for reverse order

### Return value

[`PageArray`](/api/ref/page-array/)

All parent pages, or those matching the given selector.

