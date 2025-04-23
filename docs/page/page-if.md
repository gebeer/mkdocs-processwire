If value is available for $key return or call $yes condition (with optional $no condition)
------------------------------------------------------------------------------------------

This merges the capabilities of an if() statement, get() and getMarkup() methods in one, plus some useful PW type-specific logic, providing a useful output shortcut. It many situations it enables you to accomplish on one-line of code what might have otherwise taken multiple lines of code. Use this when looking for a useful shortcut and this one fits your need, otherwise use a regular PHP if() statement.

This function is primarily intended for conditionally outputting some formatted string value or markup, however its use is not limited to that, as you can specify whatever you’d like for the $yes and $no conditions. The examples section best describes potential usages of this method, so I recommend looking at those before reading all the details of this method.

Note that the logic is a little bit smarter for PW than a regular PHP if() statement in these ways:

*   If value resolves to any kind of _empty_ [`WireArray`](/api/ref/wire-array/) (like a [`PageArray`](/api/ref/page-array/)) the NO condition is used. If the WireArray is populated with at least one item then the YES condition is used. So this if() method (unlike PHP if) requires that not only is the value present, but it is also populated.
    
*   If value resolves to a [`NullPage`](/api/ref/null-page/) the NO condition is used.
    

The `$key` argument may be any of the following:

*   A field name, in which case we will use the value of that field on this page. If the value is empty the NO condition will be used, otherwise the YES condition will be used. You can use any format for the field name that the [`Page::get()`](/api/ref/page/get/) method accepts, so subfields and OR field statements are also okay, i.e. `categories.count`, \`field1|field2|field3', etc.
    
*   A selector string that must match this page in order to return the YES condition. If it does not match then the NO condition will be used.
    
*   A boolean, integer, digit string or PHP array. If considered empty by PHP it will return the NO condition, otherwise it will return the YES condition.
    

The `$yes` and `$no` arguments (the conditional actions) may be any of the following:

*   Any string value that you’d like (HTML markup is fine too).
    
*   A field name that is present on this page, or optionally the word “value” to refer to the field specified in the `$key` argument. Either way, makes this method return the actual field value as it exists on the page, rather than a string/markup version of it. Note that if this word (“value”) is used for the argument then of course the `$key` argument must be a field name (not a selector string).
    
*   Any callable inline function that returns the value you want this function to return.
    
*   A string containing one or more `{field}` placeholders, where you replace “field” with a field name. These are in turn populated by the [`Page::getMarkup()`](/api/ref/page/get-markup/) method. You can also use `{field.subfield}` and `{field1|field2|field3}` type placeholder strings.
    
*   A string containing `{val}` or `{value}` where they will be replaced with the markup value of the field name given in the $key argument.
    
*   If you omit the `$no` argument an empty string is assumed.
    
*   If you omit both the `$yes` and `$no` arguments, then boolean is assumed (true for yes, false for no), which makes this method likewise return a boolean. The only real reason to do this would be to take advantage of the method’s slightly different behavior than regular PHP if() statements (i.e. treating empty WireArray or NullPage objects as false conditions).
    

Available since version **3.0.126**.

### Example

    // if summary is populated, output it in an paragraph
    echo $page->if("summary", "<p class='summary'>{summary}</p>");
    
    // same as above, but shows you can specify {value} to assume field in $key arg
    echo $page->if("summary", "<p class='summary'>{value}</p>");
    
    // if price is populated, format for output, otherwise ask them to call for price
    echo $page->if("price", function($val) { return '$' . number_format($val); }, "Please call");
    
    // you can also use selector strings
    echo $page->if("inventory>10", "In stock", "Limited availability");
    
    // output an <img> tag for the first image on the page, or blank if none
    echo $page->if("images", function($val) { return "<img src='{$val->first->url}'>"; });

### Usage

    // basic usage
    $mixed = $page->if($key);
    
    // usage with all arguments
    $mixed = $page->if($key, $yes = '', $no = '');

### Arguments

Name

Type(s)

Description

`key`

string, bool, int

Name of field to check, selector string to evaluate, or boolean/int to evalute

`yes` (optional)

string, callable, mixed

If value for $key is present, return or call this

`no` (optional)

string, callable, mixed

If value for $key is empty, return or call this

### Return value

`mixed` `string` `bool`

