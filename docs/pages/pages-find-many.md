Like find(), but with “lazy loading” to support giant result sets without running out of memory.
------------------------------------------------------------------------------------------------

When using this method, you can retrieve tens of thousands, or hundreds of thousands of pages or more, without needing a pagination "limit" in your selector. Individual pages are loaded and unloaded in chunks as you iterate them, making it possible to iterate all pages without running out of memory. This is useful for performing some kind of calculation on all pages or other tasks like that. Note however that if you are building something from the result set that consumes more memory for each page iterated (like concatening a string of page titles or something), then you could still run out of memory there.

The example below demonstrates use of this method. Note that attempting to do the same using the regular `$pages->find()` would run out of memory, as it's unlikely the server would have enough memory to store 20k pages in memory at once.

Available since version **3.0.19**.

### Example

    // Calculating a total from 20000 pages
    $totalCost = 0;
    $items = $pages->findMany("template=foo"); // 20000 pages
    foreach($items as $item) {
      $totalCost += $item->cost;
    }
    echo "Total cost is: $totalCost";

### Usage

    // basic usage
    $items = $pages->findMany($selector);
    
    // usage with all arguments
    $items = $pages->findMany($selector, array $options = []);

### Arguments

Name

Type(s)

Description

`selector`

string, array, Selectors

Selector to find pages

`options` (optional)

array

Options to modify behavior. See `Pages::find()` $options argument for details.

### Return value

[`PageArray`](/api/ref/page-array/)

### See Also

*   [Pages::find()](/api/ref/pages/find/)
*   [Pages::findOne()](/api/ref/pages/find-one/)

