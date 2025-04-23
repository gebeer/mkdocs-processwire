Returns the URL to the page, including scheme and hostname
----------------------------------------------------------

*   This method is just like the `$page->url()` method except that it also includes scheme and hostname.
    
*   This method can also be accessed at the property `$page->httpUrl` (without parenthesis).
    
*   It is desirable to use this method when some page templates require https while others don't.  
    This ensures local links will always point to pages with the proper scheme. For other cases, it may be preferable to use `$page->url()` since it produces shorter output.
    

### Example

    // Generating a link to this page using httpUrl
    echo "<a href='$page->httpUrl'>$page->title</a>"; 

### Usage

    // basic usage
    $string = $page->httpUrl();
    
    // usage with all arguments
    $string = $page->httpUrl(array $options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

array

For details on usage see [`Page::url()`](/api/ref/page/url/) options argument.

### Return value

`string`

Returns full URL to page, for example: `https://processwire.com/about/`

### See Also

*   [Page::url()](/api/ref/page/url/)
*   [Page::localHttpUrl()](/api/ref/page/local-http-url/)

