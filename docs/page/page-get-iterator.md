Enables iteration of the page's properties and fields with PHP’s foreach()
--------------------------------------------------------------------------

This fulfills PHP's IteratorAggregate interface, enabling you to interate all of the page's properties and fields.

### Example

    // List all properties and fields from the page
    foreach($page as $name => $value) {
      echo "<h3>$name</h3>";
      echo "<p>$value</p>";
    }

### Usage

    $arrayObject = $page->getIterator();

### Return value

`ArrayObject`

