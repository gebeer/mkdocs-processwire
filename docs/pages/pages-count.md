Count and return how many pages will match the given selector.
--------------------------------------------------------------

If no selector provided, it returns count of all pages in site.

### Example

    // Return count of how may pages in the site use the blog-post template
    $numBlogPosts = $pages->count("template=blog-post");

### Usage

    // basic usage
    $int = $pages->count();
    
    // usage with all arguments
    $int = $pages->count($selector = '', $options = []);

### Arguments

Name

Type(s)

Description

`selector` (optional)

string, array, Selectors

Specify selector, or omit to retrieve a site-wide count.

`options` (optional)

array, string

See $options for $pages->find().

### Return value

`int`

### See Also

*   [Pages::find()](/api/ref/pages/find/)

