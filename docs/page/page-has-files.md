Does the page have a files path and one or more files present in it?
--------------------------------------------------------------------

This will only check if files exist, it will not create the directory if it’s not already present.

Available since version **3.0.138**. _Earlier versions must use the more verbose PagefilesManager::hasFiles($page)_

### Usage

    $bool = $page->hasFiles();

### Return value

`bool`

