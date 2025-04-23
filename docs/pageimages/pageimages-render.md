Render markup for all images here (optionally using a provided markup template string and/or image size options)
----------------------------------------------------------------------------------------------------------------

Given template string can contain any of the placeholders, which will be replaced:

*   `{url}` or `{src}` Image URL (typically used for src attribute)
*   `{httpUrl}` File URL with scheme and hostname (alternate for src attribute)
*   `{URL}` Same as url but with cache busting query string
*   `{HTTPURL}` Same as httpUrl but with cache busting query string
*   `{description}` or `{alt}` Image description (typically used in alt attribute)
*   `{tags}` File tags (might be useful in class attribute)
*   `{width}` Width of image
*   `{height}` Height of image
*   `{hidpiWidth}` HiDPI width of image
*   `{hidpiHeight}` HiDPI height of image
*   `{ext}` File extension
*   `{original.name}` Replace “name” with any of the properties above to refer to original/full-size image. If there is no original image then these just refer back to the current image.

Available since version **3.0.126**.

### Example

    // default output
    echo $page->images->render();
    
    // custom output
    echo $page->images->render("<img class='pw-image' src='{url}' alt='{alt}'>");
    
    // custom output with options
    echo $page->images->render("<img src='{url}' alt='{alt}'>", [ 'width' => 300 ]);
    
    // options can go in first argument if you prefer
    echo $page->images->render([ 'width' => 300, 'height' => 200 ]);
    
    // if only width/height are needed, they can also be specified as a string (1st or 2nd arg)
    echo $page->images->render('300x200');
    
    // custom output with link to original/full-size and square crop of 300x300 for thumbnails
    echo "<ul>" . $page->images->render([
      'markup' => "<li><a href='{original.url}'><img src='{url}' alt='{alt}'></a></li>",
      'width' => 300,
      'height' => 300
    ]) . "</ul>";

### Usage

    // basic usage
    $string = $pageimages->render();
    
    // usage with all arguments
    $string = $pageimages->render($markup = '', $options = []);

### Arguments

Name

Type(s)

Description

`markup` (optional)

string, array

Markup template string or optional $options array if you do not want the template string here.

`options` (optional)

array, string

Optionally resize image with these options sent to size() method:

*   `width` (int): Target width or 0 for current image size (or proportional if height specified).
*   `height` (int): Target height or 0 for current image size (or proportional if width specified).
*   `markup` (string): Markup template string (same as $markup argument), or omit for default (same as $markup argument).
*   `link` (bool): Link image to original size? Though you may prefer to do this with your own $markup (see examples). (default=false)
*   `limit` (int): Render no more than this many images (default=0, no limit).
*   Plus any option available to the $options argument on the [`Pageimage::size()`](/api/ref/pageimage/size/) method.
*   If you only need width and/or height, you can specify a width x height string, i.e. 123x456 (use 0 for proportional).

### Return value

`string`

