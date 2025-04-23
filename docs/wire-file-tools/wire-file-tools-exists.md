Does the given file/link/dir exist?
-----------------------------------

Thie method accepts an `$options` argument that can be specified as an array or a string (space or comma separated). The examples here demonstrate usage as a string since it is the simplest for readability.

*   This function may return false for symlinks pointing to non-existing files, unless you specify `link` as the `type`.
*   Specifying `false` for the `readable` or `writable` argument disables the option from being used, it doesn’t perform a NOT condition.
*   The `writable` option may also be written as `writeable`, if preferred.

Available since version **3.0.180**.

### Example

    // 1. check if exists
    $exists = $files->exists('/path/file.ext');
    
    // 2. check if exists and is readable (or writable)
    $exists = $files->exists('/path/file.ext', 'readable');
    $exists = $files->exists('/path/file.ext', 'writable');
    
    // 3. check if exists and is file, link or dir
    $exists = $files->exists('/path/file.ext', 'file');
    $exists = $files->exists('/path/file.ext', 'link');
    $exists = $files->exists('/path/file.ext', 'dir');
    
    // 4. check if exists and is writable file or dir
    $exists = $files->exists('/path/file.ext', 'writable file');
    $exists = $files->exists('/path/dir/', 'writable dir');
    
    // 5. check if exists and is readable and writable file
    $exists = $files->exists('/path/file.ext', 'readable writable file');

### Usage

    // basic usage
    $bool = $files->exists(string $filename);
    
    // usage with all arguments
    $bool = $files->exists(string $filename, $options = '');

### Arguments

Name

Type(s)

Description

`filename`

string

`options` (optional)

array, string

Can be specified as array or string:

*   `type` (string): Verify it is of type: 'file', 'link', 'dir' (default='')
*   `readable` (bool): Verify it is readable? (default=false)
*   `writable` (bool): Also verify the file is writable? (default=false)
*   `writeable` (bool): Alias of writable (default=false)
*   When specified as string, you can use any combination of the words: `readable, writable, file, link, dir` (separated by space or comma).

### Return value

`bool`

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given invalid or unrecognized $options
    

