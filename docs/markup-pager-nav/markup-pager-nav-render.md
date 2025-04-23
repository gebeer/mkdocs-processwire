Render pagination markup
------------------------

### Example

    $items = $pages->find("id>0, limit=10"); // replace id>0 with your selector
    if($items->count()) {
      echo "<ul>" . $items->each("<li>{title}</li>") . "</ul>";
      $pager = $modules->get("MarkupPagerNav");
      $options = [ 'numPageLinks' => 5 ];
      echo $pager->render($items, $options); // render the pagination navigation
    } else {
      echo "<p>Sorry there were no items found</p>";
    }

### Usage

    // basic usage
    $string = $pager->render($items);
    
    // usage with all arguments
    $string = $pager->render($items, array $options = []);

### Arguments

Name

Type(s)

Description

`items`

WirePaginatable, PageArray, PaginatedArray

Items used in the pagination that have had a "limit=n" selector applied when they were loaded.

`options` (optional)

array

Any options to override the defaults. See the [`MarkupPagerNav`](/api/ref/markup-pager-nav/) reference for all options.

### Return value

`string`

