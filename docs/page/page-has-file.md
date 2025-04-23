Does Page have given filename in its files directory?
-----------------------------------------------------

Available since version **3.0.166**.

### Usage

    // basic usage
    $bool = $page->hasFile(string $file);
    
    // usage with all arguments
    $bool = $page->hasFile(string $file, array $options = []);

### Arguments

Name

Type(s)

Description

`file`

string

File basename or verbose hash

`options` (optional)

array

*   `getPathname` (bool): Get full path + filename when would otherwise return boolean true? (default=false)
*   `getPagefile` (bool): Get Pagefile object when would otherwise return boolean true? (default=false)

### Return value

`bool` `string`

