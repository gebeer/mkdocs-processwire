Get contents of file
--------------------

This is the same as PHP’s `file_get_contents()` except that the arguments are simpler and it may be preferable to use this in ProcessWire for future cases where the file system may be abstracted from the installation.

Available since version **3.0.167**.

### Usage

    // basic usage
    $bool = $files->fileGetContents(string $filename);
    
    // usage with all arguments
    $bool = $files->fileGetContents(string $filename, int $offset = 0, int $maxlen = 0);

### Arguments

Name

Type(s)

Description

`filename`

string

Full path and filename to read

`offset` (optional)

int

The offset where the reading starts on the original stream. Negative offsets count from the end of the stream.

`maxlen` (optional)

int

Maximum length of data read. The default is to read until end of file is reached.

### Return value

`bool` `string`

Returns the read data (string) or boolean false on failure.

### See Also

*   [WireFileTools::filePutContents()](/api/ref/wire-file-tools/file-put-contents/)

