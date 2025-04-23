Get size of file or directory (in bytes)
----------------------------------------

Available since version **3.0.214**.

### Usage

    // basic usage
    $int = $files->size(string $path);
    
    // usage with all arguments
    $int = $files->size(string $path, $options = []);

### Arguments

Name

Type(s)

Description

`path`

string

File or directory path

`options` (optional)

array, bool

Options array, or boolean true for getString option:

*   `getString` (bool): Get string that summarizes bytes, kB, MB, etc.? (default=false)

### Return value

`int` `string`

