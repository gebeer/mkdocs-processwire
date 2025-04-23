Return the height of this image OR return an image sized with a given height (and proportional width).
------------------------------------------------------------------------------------------------------

*   If given a height, it'll return a new Pageimage object sized to that height.
*   If not given a height, it'll return the height of this Pageimage.

### Example

    // Get height of image
    $px = $image->height();
    
    // Create a new variation at 200px height
    $thumb = $image->height(200);

### Usage

    // basic usage
    $int = $pageimage->height();
    
    // usage with all arguments
    $int = $pageimage->height(int $n = 0, $options = []);

### Arguments

Name

Type(s)

Description

`n` (optional)

int

Optional height if you are creating a new size.

`options` (optional)

array, string, int, bool

See [`Pageimage::size()`](/api/ref/pageimage/size/) $options argument for details.

### Return value

`int` [`Pageimage`](/api/ref/pageimage/)

Returns height (in px) when given no arguments, or Pageimage when given a height argument.

