Title: $files->find() method - ProcessWire API

URL Source: https://processwire.com/api/ref/wire-file-tools/find/

Markdown Content:
Find all files in the given $path recursively, and return a flat array of all found filenames
---------------------------------------------------------------------------------------------

Available since version **3.0.96**.

### Usage

```
// basic usage
$array = $files->find(string $path);

// usage with all arguments
$array = $files->find(string $path, array $options = []);
```

### Arguments

| Name | Type(s) | Description |
| --- | --- | --- |
| `path` | string | Path to start from (required).
 |
| `options` (optional) | array | Options to affect what is returned (optional):

*   `recursive` (int|bool): How many levels of subdirectories this method should descend into beyond the 1 given. Specify 1 to remain at the one directory level given, or 2+ to descend into subdirectories. (default=10) In 3.0.180+ you may also specify true for no limit, or false to disable descending into any subdirectories.
*   `extensions` (array|string): Only include files having these extensions, or omit to include all (default=\[\]). In 3.0.180+ the extensions argument may also be a string (space or comma separated).
*   `excludeDirNames` (array): Do not descend into directories having these names (default=\[\]).
*   `excludeHidden` (bool): Exclude hidden files? (default=false).
*   `allowDirs` (bool): Allow directories in returned files (except for '.' and '..')? Note that returned directories have a trailing slash. (default=false) 3.0.180+
*   `returnRelative` (bool): Make returned array have filenames relative to given start $path? (default=false)

 |

### Return value

`array`

Flat array of filenames

* * *

[$files methods and properties](https://processwire.com/api/ref/wire-file-tools/)

API reference based on ProcessWire core version 3.0.244
