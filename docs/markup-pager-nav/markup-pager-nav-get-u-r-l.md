Get URL for given pagination number
-----------------------------------

Requires that render() method has already started or been previously called.

### Usage

    // basic usage
    $string = $pager->getURL(int $pageNum);
    
    // usage with all arguments
    $string = $pager->getURL(int $pageNum, bool $http = false);

### Arguments

Name

Type(s)

Description

`pageNum`

int

`http` (optional)

bool

Include scheme and hostname?

### Return value

`string`

