Find the closest parent page matching your selector
---------------------------------------------------

This is like `$page->parent()` but includes the current Page in the possible pages that can be matched, and the $selector argument is required.

### Usage

    $page = $page->closest($selector);

### Arguments

Name

Type(s)

Description

`selector`

string, array

Selector string to match.

### Return value

[`Page`](/api/ref/page/) [`NullPage`](/api/ref/null-page/)

$selector Returns the current Page or closest parent matching the selector. Returns NullPage when no match.

