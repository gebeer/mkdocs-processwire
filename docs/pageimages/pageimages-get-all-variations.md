Get an array of all image variations on this field indexed by original file name.
---------------------------------------------------------------------------------

More information on any variation filename can be retrieved from [`Pageimage::isVariation()`](/api/ref/pageimage/is-variation/).

### Example

    $variations = $page->images->getAllVariations();
    print_r($variations);
    // Example output:
    // array(
    //   'foo.jpg' => array(
    //      'foo.100x100.jpg',
    //      'foo.200x200.jpg'
    //   ),
    //   'bar.jpg' => array(
    //      'bar.300x300.jpg'
    //   )
    // );

### Usage

    $array = $pageimages->getAllVariations();

### Return value

`array`

Array indexed by file name, each containing array of variation file names

### See Also

*   [Pageimage::isVariation()](/api/ref/pageimage/is-variation/)

