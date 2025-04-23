Get all fulltext stopwords for database engine
----------------------------------------------

### Usage

    // basic usage
    $array = $database->getStopwords();
    
    // usage with all arguments
    $array = $database->getStopwords(string $engine = '', bool $flip = false);

### Arguments

Name

Type(s)

Description

`engine` (optional)

string

Specify DB engine of "myisam" or "innodb" or omit for current DB engine

`flip` (optional)

bool

Return flipped array where stopwords are array keys rather than values? for isset() use (default=false)

### Return value

`array`

