Find pages and specify which fields to join (overriding configured autojoin settings)
-------------------------------------------------------------------------------------

This is a useful optimization when you know exactly which fields you will be using from the returned pages and you want to have their values joined into the page loading query to reduce overhead. Note that this overrides the configured autojoin settings in ProcessWire fields.

If a particular page in the returned set of pages was already loaded before this method call, then the one already in memory will be used rather than this method loading another copy of it.

Available since version **3.0.172**.

### Example

    // 1. Example of loading blog posts where we want to join title, date, summary:
    $posts = $pages->findJoin("template=blog-post", [ 'title', 'date', 'summary' ]);
    
    // 2. You can also specify the join fields as a CSV string:
    $posts = $pages->findJoin("template=blog-post", 'title, date, summary');
    
    // 3. You can also use the join functionality on a regular $pages->find() by specifying
    // property 'join' or 'field' in the selector. The words 'join' and 'field' are aliases
    // of each other here, just in case you have an existing field with one of those names.
    // Otherwise, use whichever makes more sense to you. The following examples demonstrate
    // this and all do exactly the same thing as examples 1 and 2 above:
    $posts = $pages->find("template=blog-post, join=title|date|summary");
    $posts = $pages->find("template=blog-post, field=title|date|summary");
    $posts = $pages->find("template=blog-post, join=title, join=date, join=summary");
    $posts = $pages->find("template=blog-post, field=title, field=date, field=summary");
    
    // 4. Let’s say you want to load pages with NO autojoin fields, here is how.
    // The following loads all blog-post pages and prevents ANY fields from being joined,
    // even if they are configured to be autojoin in ProcessWire:
    $posts = $pages->findJoin("template=blog-post", false);
    $posts = $pages->find("template=blog-post, join=none"); // same as above

### Usage

    // basic usage
    $items = $pages->findJoin($selector, $joinFields);
    
    // usage with all arguments
    $items = $pages->findJoin($selector, $joinFields, array $options = []);

### Arguments

Name

Type(s)

Description

`selector`

string, array, Selectors

`joinFields`

array, string, bool

Array or CSV string of field names to autojoin, or false to join none.

`options` (optional)

array

### Return value

[`PageArray`](/api/ref/page-array/)

