Represents an image item attached to a page, typically via an Image Fieldtype.
------------------------------------------------------------------------------

Pageimage objects are usually contained by a [`Pageimages`](/api/ref/pageimages/) object, which is a type of [`Pagefiles`](/api/ref/pagefiles/) and [`WireArray`](/api/ref/wire-array/). In addition to the methods and properties below, you'll also want to look at [`Pagefile`](/api/ref/pagefile/) which this class inherits several important methods and properties from.

    // Example of outputting a thumbnail gallery of Pageimage objects
    foreach($page->images as $image) {
      // $image and $thumb are both Pageimage objects
      $thumb = $image->size(200, 200);
      echo "<a href='$image->url'>";
      echo "<img src='$thumb->url' alt='$image->description' />";
      echo "</a>";
    }

