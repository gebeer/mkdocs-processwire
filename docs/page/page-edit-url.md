Return the URL necessary to edit this page
------------------------------------------

*   We recommend checking that the page is editable before outputting the editUrl().
*   If user opens URL in their browser and is not logged in, they must login to account with edit permission.
*   This method can also be accessed by property at `$page->editUrl` (without parenthesis).

### Example

    if($page->editable()) {
      echo "<a href='$page->editUrl'>Edit this page</a>";
    }

### Usage

    // basic usage
    $string = $page->editUrl();
    
    // usage with all arguments
    $string = $page->editUrl($options = []);

### Arguments

Name

Type(s)

Description

`options` (optional)

array, bool, string

Specify true for http option, specify name of field to find (3.0.151+), or use $options array:

*   `http` (bool): True to force scheme and hostname in URL (default=auto detect).
*   `language` (Language|bool): Optionally specify Language to start editor in, or boolean true to force current user language.
*   `find` (string): Name of field to find in the editor (3.0.151+)

### Return value

`string`

URL for editing this page

