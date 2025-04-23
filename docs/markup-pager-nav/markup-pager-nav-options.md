Get all options or set options
------------------------------

*   See the main [`MarkupPagerNav`](/api/ref/markup-pager-nav/) documentation for a list of all available options.
*   When used to set options this method should be called before the [`MarkupPagerNav::render()`](/api/ref/markup-pager-nav/render/) method.
*   Options can also be set as a 2nd argument to the [`MarkupPagerNav::render()`](/api/ref/markup-pager-nav/render/) method.

Available since version **3.0.44**.

### Example

    // Getting options
    echo "<pre>" . print_r($pager->options(), true) . "</pre>";
    
    // Setting options
    $pager->options([ 'numPageLinks' => 5 ]);
    echo $pager->render($items);
    
    // Alternative that does the same as above
    echo $pager->render($items, [ 'numPageLinks' => 5 ]); 

### Usage

    // basic usage
    $array = $pager->options();
    
    // usage with all arguments
    $array = $pager->options(array $options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

array

Associative array of options you want to set, or omit to just return all available/current options.

### Return value

`array`

Returns associative array if options with all current values.

