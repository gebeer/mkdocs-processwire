Return number of parents (depth relative to homepage) that this page has, optionally filtered by a selector
-----------------------------------------------------------------------------------------------------------

For example, homepage has 0 parents and root level pages have 1 parent (which is the homepage), and the number increases the deeper the page is in the pages structure.

### Usage

    // basic usage
    $int = $page->numParents();
    
    // usage with all arguments
    $int = $page->numParents(string $selector = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

string

Optional selector to filter by (default='')

### Return value

`int`

Number of parents

