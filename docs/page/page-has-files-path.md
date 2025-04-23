Does the page have a files path for storing files?
--------------------------------------------------

This will only check if files path exists, it will not create the path if it’s not already present.

Available since version **3.0.138**. _Earlier versions must use the more verbose PagefilesManager::hasPath($page)_

### Usage

    $bool = $page->hasFilesPath();

### Return value

`bool`

