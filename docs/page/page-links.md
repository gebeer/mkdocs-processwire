Return pages linking to this one (in Textarea/HTML fields)
----------------------------------------------------------

Applies only to Textarea fields with “html” content-type and link abstraction enabled.

Available since version **3.0.107**.

### Usage

    // basic usage
    $items = $page->links();
    
    // usage with all arguments
    $items = $page->links($selector = '', $field = '');

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, bool

Optional selector to filter by or boolean true for “include=all”. (default='')

`field` (optional)

string, Field

Optionally limit results to specified field. (default=all applicable Textarea fields)

### Return value

[`PageArray`](/api/ref/page-array/)

