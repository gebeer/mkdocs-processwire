Get the Pagefile object containing the given filename.
------------------------------------------------------

### Usage

    $pagefile = $pagefilesManager->getFile(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Name of file to get:

*   If given a URL or path, this will traverse to other pages.
*   If given a basename, it will stay with current page.

### Return value

[`Pagefile`](/api/ref/pagefile/) [`Pageimage`](/api/ref/pageimage/) `null`

Returns Pagefile or Pageimage object if found, or null if not.

