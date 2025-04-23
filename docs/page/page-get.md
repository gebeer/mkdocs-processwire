Title: $page->get() method - ProcessWire API

URL Source: https://processwire.com/api/ref/page/get/

Markdown Content:
Get the value of a Page property (see details for several options)
------------------------------------------------------------------

This method can accept a simple property name, and also much more:

*   You can retrieve a value using either `$page->get('property');` or `$page->property`.
*   Get the first populated property by specifying multiple properties separated by a pipe, i.e. `headline|title`.
*   Get multiple properties in a string by specifying a string `{property}` tags, i.e. `{title}: {summary}`.
*   Specify a selector string to get the first matching child page, i.e. `created>=today`.
*   This method can also retrieve sub-properties of object properties, i.e. `parent.title`.
*   To get a guaranteed iterable value, append `[]` to the key, i.e. `$page->get('name[]')`. 3.0.205+

### Example

```
// retrieve the title using get…
$title = $page->get('title');

// …or retrieve using direct access
$title = $page->title;

// retrieve headline if populated, otherwise title
$headline = $page->get('headline|title');

// retrieve title, created date, and summary, formatted in a string
$str = $page->get('{createdStr}: {title} - {summary}');

// example of getting a sub-property: title of parent page
$title = $page->get('parent.title');

// all following features are supported in 3.0.205+

// get value guaranteed to be iterable (array, WireArray, or derived)
$images = $page->get('image[]');
$categories = $page->get('category[]');

// get item by position/index, returns 1 item whether field is single or multi value
$file = $page->get('files[0]'); // get first file  (or null if files is empty)
$file = $page->get('files.first); // same as above
$file = $page->get('files.last'); // get last file
$file = $page->get('files[1]'); // get 2nd file (or null if there isn't one)

// get titles from Page reference field categories in an array
$titles = $page->get('categories.title');  // array of titles
$title = $page->get('categories[0].title'); // string of just first title

// you can also use a selector in [brackets] for a filtered value
// example: get categories with titles matching text 'design'
$categories = $page->get('categories[title%=design]'); // PageArray
$category = $page->get('categories[title%=design][0]'); // Page or null
$titles = $page->get('categories[title%=design].title'); // array of strings
$title = $page->get('categories[title%=design].title[0]'); // string or null
```

### Usage

```
$mixed = $page->get(string $key);
```

### Arguments

| Name | Type(s) | Description |
| --- | --- | --- |
| `key` | string | Name of property, format string or selector, per the details above.
 |

### Return value

`mixed`

Value of found property, or NULL if not found.

### See Also

*   [WireData::set()](https://processwire.com/api/ref/wire-data/set/)

* * *

[$page methods and properties](https://processwire.com/api/ref/page/)

API reference based on ProcessWire core version 3.0.244
